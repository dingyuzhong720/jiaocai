# 附录A 类模板的分离式编译

原始 PDF 第 500–502 页。

## 附录A 类模板的分离式编译

如果完全在声明中实现类模板，那么正如我们已经看到的，几乎用不到多少语法。事实上，许多类模板就是用这种方式实现的，因为编译器对模板分离式编译的支持从历史上看一直是微弱的，而且是针对特殊的平台的。因此，在许多情况下，整个类及其实现常被放在单独的头文件中。标准库(StandardLibrary)的流行做法也是遵循这种方式来实现类模板的。

图A.1显示的是MemoryCel1类模板的声明。当然，这部分非常简单，因为它只是我们已经看到的整个类模板的一个子集。

```c
#ifndef MEMORY_CELL_H
#define MEMORY_CELL_H

/**
 * 模拟内存单元的类.
 */
template <typename Object>
class MemoryCell
{
    public:
        explicit MemoryCell( const Object & initialValue = Object{ } );
        const Object & read( ) const;
        void write( const Object & x );

    private:
        Object storedValue;
};

#endif
```

图 A.1 MemoryCell 类模板接口

对于它的实现，我们有一组函数模板。这意味着，每个函数必须包含模板声明，并且在使用范围操作符时，其前面的类名必须用模板实参(template argument)实例化。于是，在图A.2中，类名写成MemoryCell&lt;Object&gt;。虽然语法看起来没有问题，但是却可能变得相当烦琐。例如，在规范中定义operator=需要语言精练。然而在实现中，我们却会有如下生硬的代码①:

```cpp
template <typename Object>
const MemoryCell<Object> &
MemoryCell<Object>::operator= ( const MemoryCell<Object> & rhs )
{
    if( this != &rhs )
        storedValue = rhs.storedProcedure;
    return *this;
}
```

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">①注意，MemoryCell&lt;Object&gt;有些(在::后的)出现可以忽略，编译器将把MemoryCell解释成MemoryCell&lt;Object&gt;。</span></small>

---

附录A 类模板的分离式编译

487

即使是这样，但现在问题变成如何组织类模板声明及各成员函数模板的定义了。主要问题在于，图A.2中实现的并不是具体的函数，它们就是一些有待展开的模板。但是，这些模板甚至在MemoryCel1类模板实例化时都不会展开。每个成员函数模板只有当它们被调用的时候才会展开。

## A.1 全部放入头文件

第1种做法是把声明和实现均放入头文件中。但这样并不能使类正常工作，因为如果多个不同的源文件都有处理该头文件的include指令，那么我们就会得到一些重复定义的函数，不过，由于这里每一处都是一个模板，而不是具体的类，所以此时问题并不存在。

使用这种方法，直接让头文件发出include指令(在#endif之前)来自动读入实现文件可能阅读起来更容易些。不过，使用这种方法，存储模板的那些.cpp文件将不会被直接编译。

## A.2 显式实例化

如果使用显式实例化，那么在某些编译器下我们可以获得分离式编译的许多长处。在这种情形下，正如通常对类所做的那样，我们建立.h文件和.cpp文件。这样，图A.1和图A.2恰如当前所示。头文件将不再让include指令去读类的实现。主例程将只有一个头文件的包含指令。图A.3显示一个典型的测试程序。如果同时编译两个.cpp文件，那么我们发现，找不到那些实例化的成员函数。我们通过创建一个分离文件来修正这个程序，其中，该分离文件包含我们所用类型的MemoryCel1的显式实例化。显式实例化的例如图A.4所示。这个文件作为项目的一部分被编译，而模板的实现文件(图A.2)并不作为项目的一部分被编译。我们已经对几种老的编译器使用这种技术获得了成功。不足之处在于，所有的模板展开必须由程序员列出，且当类模板用到其他类模板的时候，那些类模板有时也必须列出。优点在于，若MemoryCel1中成员函数的实现发生改变，则只需对MemoryCellExpand.cpp重新编译即可。

```cpp
#include "MemoryCell.h"

/**
 * 用 initialValue 构造 MemoryCell 对象.
 */
template <typename Object>
MemoryCell<Object>::MemoryCell( const Object & initialValue )
: storedValue{ initialValue }
{
}

/**
 * 返回所存储的值.
 */
template <typename Object>
const Object & MemoryCell<Object>::read( ) const
{
```

图 A.2 MemoryCell 类模板的实现

---

488

数据结构与算法分析—C++语言描述(第四版)

```cpp
return storedValue;
}

/**
 * 存储 x.
 */
template <typename Object>
void MemoryCell<Object>::write( const Object & x )
{
    storedValue = x;
}
```

图 A.2(续) MemoryCell 类模板的实现

```cpp
#include "MemoryCell.h"
#include <iostream>
using namespace std;

int main( )
{
    MemoryCell<int>    m1;
    MemoryCell<double> m2{ 3.14 };

    m1.setValue( 37 );
    m2.setValue( m2.getValue( ) * 2 );

    cout << m1.getValue( ) << endl;
    cout << m2.getValue( ) << endl;

    return 0;
}
```

图 A.3 使用 MemoryCell 类模板

```cpp
#include "MemoryCell.cpp"

template class MemoryCell<int>;
template class MemoryCell<double>;
```

图 A.4 实例化文件 MemoryCellExpand.cpp
