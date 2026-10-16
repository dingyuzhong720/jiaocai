# 第4章 树

原始 PDF 第 114–168 页。

## 第4章 树

对于大量的输入数据，链表的线性访问耗时过多，不便使用。本章讨论一种简单的数据结构，其大部分操作的运行时间平均为 $O(\log N)$ 。我们还要简述对这种数据结构在概念上的简单的修改，它保证在最坏情形下的上述时间界。此外，还将讨论第二种修改，对于长的指令序列它实质上给出每种操作的 $O(\log N)$ 运行时间。

我们涉及到的这种数据结构叫作二叉查找树 (binary search tree)。二叉查找树是两种库集合类 set 和 map 实现的基础，它们用于许多应用之中。总的来说，在计算机科学中树 (tree) 是非常有用的抽象概念，因此，我们将讨论树在其他更一般应用中的使用。在这一章，我们将

- 看到树是如何被用于实现几种流行操作系统的文件系统的。
● 看到树如何能够用来计算算术表达式的值。
- 指出如何利用树来支持以 $O(\log N)$ 平均时间进行的各种搜索操作, 以及如何细化以得到最坏情形时间界 $O(\log N)$ 。我们还将看到当数据被存放在磁盘上时如何来实现这些操作。
- 讨论并使用 set 类和 map 类。

## 4.1 预备知识

树(tree)可以用几种方式定义。定义树的一种自然的方式是递归的方式。一棵树是一些节点(node)的集合。这个集合可以是空集；若不是空集，则树由称做根(root)的节点 $r$ 以及0个或多个非空的(子)树 $T_{1}, T_{2}, \cdots, T_{k}$ 组成，这些子树中每一棵的根都被来自根 $r$ 的一条有向的边(edge)所连接。

每一棵子树的根叫作根 $r$ 的儿子(child)，而 $r$ 是每一棵子树的根的父亲(parent)。图4.1显示了用递归定义的典型的树。

![](../../raw/pages_0097-0128/images/page_113_image_11.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["T1"] --> B["根"]
  B --> C["T2"]
  B --> D["T3"]
  B --> E["T4"]
  B --> F["..."]
  B --> G["TN"]
```
</details>

图4.1 一般的树

从递归定义中我们发现，一棵树是 $N$ 个节点和 $N - 1$ 条边的集合，其中的一个节点叫作根。存在 $N - 1$ 条边的结论是由下面的事实得出的:每条边都将某个节点连接到它的父亲，而除去根节点外每一个节点都有一个父亲(见图4.2)。

在图 4.2 的树中，节点 A 是根。节点 F 有一个父亲 A 并且有儿子 K、L 和 M。每一个节点可以有任意多个儿子，也可能是零个儿子。没有儿子的节点称为树叶 (leaf)，图 4.2 中的树

---

第4章 树

101

叶是 B、C、H、I、P、Q、K、L、M 和 N。具有相同父亲的节点为兄弟(siblings)。因此，K、L 和 M 都是兄弟。用类似的方法可以定义祖父(grandparent)和孙子(grandchild)关系。

![](../../raw/pages_0097-0128/images/page_114_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["A"] --> B["B"]
  A["A"] --> C["C"]
  A["A"] --> D["D"]
  A["A"] --> E["E"]
  A["A"] --> F["F"]
  A["A"] --> G["G"]
  A["A"] --> H["H"]
  A["A"] --> I["I"]
  A["A"] --> J["J"]
  A["A"] --> K["K"]
  A["A"] --> L["L"]
  A["A"] --> M["M"]
  A["A"] --> N["N"]
  A["A"] --> O["P"]
  A["A"] --> P["Q"]
```
</details>

图4.2 一棵树

从节点 $n_1$ 到 $n_k$ 的路径(path)定义为节点 $n_1, n_2, \dots, n_k$ 的一个序列，使得对于 $1 \leqslant i < k$ 的节点 $n_i$ 是 $n_{i+1}$ 的父亲。这条路径的长(length)是该路径上的边的条数，即 $k-1$ 。从每一个节点到它自己有一条长为0的路径。注意，在一棵树中从根到每个节点恰好存在一条路径。

对任意节点 $n_i$，$n_i$ 的深度 (depth) 为从根到 $n_i$ 的唯一路径的长。因此，根的深度为 0。节点 $n_i$ 的高 (height) 是从 $n_i$ 到一片树叶的最长路径的长。因此所有树叶的高都是 0。一棵树的高 (height of a tree) 等于它的根的高。对于图 4.2 中的树，E 的深度为 1 而高为 2；F 的深度为 1 而高也是 1；该树的高为 3。一棵树的深度 (depth of a tree) 等于其最深的树叶的深度，该深度总是等于这棵树的高。

如果存在从 $n_1$ 到 $n_2$ 的一条路径，那么 $n_1$ 是 $n_2$ 的一位祖先 (ancestor)，而 $n_2$ 是 $n_1$ 的一个后裔 (descendant)。如果 $n_1 \neq n_2$，那么 $n_1$ 是 $n_2$ 的真祖先 (proper ancestor)，而 $n_2$ 是 $n_1$ 的真后裔 (proper descendant)。

## 4.1.1 树的实现

实现树的一种方法是在每一个节点除数据外还要有一些链，使得该节点的每一个儿子都被一个链所链接。然而，由于每个节点的儿子数可以变化很大并且事先不知道，因此在数据结构中建立到各(儿)子节点直接的链接是不可行的，因为这样会产生太多浪费的空间。实际上解决方法很简单:将每个节点的所有儿子都放在树节点的链表中。图4.3中的声明就是典型的声明。

图 4.4 指出一棵树是如何用这种实现方法表示的。图中向下的箭头是些指向 firstChild 的链，而从左向右的水平箭头是指向 nextSibling 的链。因为空链 (null link) 太多，所以图中没有把它们画出。

在图 4.4 的树中，节点 E 有一个链指向兄弟 (F)，另一个链指向儿子 (I)，而有的节点这两种链都没有。

```c
struct TreeNode
{
    Object element;
    TreeNode *firstChild;
    TreeNode *nextSibling;
};
```

图 4.3 树节点的声明

![](../../raw/pages_0097-0128/images/page_114_image_14.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> B["B"]
  B --> C["C"]
  C --> D["D"]
  D --> E["E"]
  E --> F["F"]
  F --> G["G"]
  G --> H["H"]
  F --> I["I"]
  I --> J["J"]
  J --> K["K"]
  K --> L["L"]
  L --> M["M"]
  M --> N["N"]
  E --> O["O"]
  O --> P["P"]
  P --> Q["Q"]
```
</details>

图 4.4 图 4.2 所示树的第一儿子/下一兄弟表示法

---

102

数据结构与算法分析——C++语言描述(第四版)

## 4.1.2 树的遍历及应用

树有很多应用。流行的用途之一是许多常用操作系统中的目录结构，包括 UNIX 和 DOS 在内。图 4.5 是 UNIX 文件系统中一个典型的目录。

![](../../raw/pages_0097-0128/images/page_115_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["/usr*"] --> B["mark*"]
  A --> C["alex*"]
  A --> D["bill*"]
  B --> E["book*"]
  B --> F["course*"]
  B --> G["junk"]
  C --> H["junk"]
  D --> I["work*"]
  D --> J["course*"]
  E --> K["ch1.r"]
  E --> L["ch2.r"]
  E --> M["ch3.r"]
  F --> N["cop3530*"]
  G --> O["cop3212*"]
  J --> P["cop3212*"]
  N --> Q["fall*"]
  N --> R["spr*"]
  N --> S["sum*"]
  O --> T["fall*"]
  O --> U["spr*"]
  Q --> V["syl.r"]
  R --> W["syl.r"]
  S --> X["syl.r"]
  T --> Y["grades"]
  U --> Z["prog1.r"]
  U --> AA["prog2.r"]
  U --> AB["prog2.r"]
  U --> AC["prog1.r"]
  U --> AD["grades"]
```
</details>

图4.5 UNIX目录

这个目录的根是/usr。（名字后面的星号指出/usr本身就是一个目录。）/usr有3个儿子:mark、alex和bill，它们本身也都是目录。因此，/usr包含3个目录而且没有正规的文件。文件名/usr/mark/book/ch1.r先后3次通过最左边的子节点而得到。在第一个/后的每个/都表示一条边，结果为一完整路径名(pathname)。这个分级文件系统非常流行，因为它能够使得用户逻辑地组织数据。不仅如此，在不同目录下的两个文件还可以享有相同的名字，因为它们必然有从根开始的不同的路径从而具有不同的路径名。在UNIX文件系统中的目录就是含有它的所有儿子的一个文件，因此，这些目录几乎是完全按照上述的类型声明构造的 $^{①}$ 。事实上，按照UNIX的某些版本，如果将打印一个文件的标准命令应用到一个目录上，那么在该目录中的这些文件名能够在(与其他非ASCII信息一起的)输出中被看到。

设我们想要列出目录中所有文件的名字，输出格式将是:深度为 $d_{i}$ 的文件将被 $d_{i}$ 次跳格(tab)缩进后打印其名。该算法在图4.6中以伪码给出。

```rust
void FileSystem::listAll( int depth = 0 ) const
{
    printName( depth );  // 打印对象的名字
    if( isDirectory( ) )
        for each file c in this directory (for each child)
            c.listAll( depth + 1 );
}
```

图4.6 列出分级文件系统中目录的伪码例程

为了显示根时不进行缩进，这里的递归函数 listAll 需要从深度 0 开始。此处的深度是一个内部簿记变量，而不是主调例程能够期望知道的那种参数。因此，给 depth 提供的默认值为 0。

算法思路简单易懂。文件对象的名字随着适当次数的跳格而被打印出来。如果它是一个目录，那么我们递归地一个一个地处理所有的儿子。这些儿子均处在下一层的深度上，因此需要缩进一个附加的间隔。整个输出显示在图4.7中。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 在 UNIX 文件系统中每个目录还有一项指向该目录本身，以及另一项指向该目录的父目录。因此，从技术上说，UNIX 文件系统不是树，而是类树 (treelike)。</span></small>

---

第4章 树

103

![](../../raw/pages_0097-0128/images/page_116_image_2.jpg)

<details>
<summary>text_image</summary>

/usr
    mark
        book
            ch1.r
            ch2.r
            ch3.r
        course
            cop3530
                fall
                    syl.r
                spr
                    syl.r
                sum
                    syl.r
        junk
alex
    junk
bill
    work
    course
        cop3212
            fall
                grades
                prog1.r
                prog2.r
                spr
                    prog2.r
                    prog1.r
                    grades
</details>

图 4.7 （先序）目录列表

这种遍历策略叫作先序遍历(preorder traversal)。在先序遍历中，对节点的处理工作是在它的诸儿子节点被处理之前(pre)进行的。当该程序运行时，显然第1行对每个节点恰好执行一次，因为每个名字只输出一次。由于第1行对每个节点最多执行一次，因此第2行也必然对每个节点执行一次。不仅如此，对于每个节点的每一个子节点第4行最多只能被执行一次。不过，儿子的个数恰好比节点的个数少1。最后，第4行每执行一次，for循环就迭代一次，每当循环结束时再加上一次。因此，每个节点总的工作量是常数。如果有N个文件名需要输出，则运行时间就是 $O(N)$ 。

另一种遍历树的常用方法是后序遍历(postorder traversal)。在后序遍历中，一个节点处的工作是在它的诸子节点被计算后进行的。例如，图4.8表示的是与前面相同的目录结构，其中圆括号内的数代表每个文件占用的磁盘区块(disk block)的个数。

由于目录本身也是文件，因此它们也有大小。设我们想要计算被该树所有文件占用的磁盘块的总数。最自然的做法是找出含于子目录/usr/mark(30)、/usr/alex(9)和/usr/bill(32)的块的个数。于是，磁盘块的总数就是子目录中的块的总数(71)再加上/usr使用的一个块，共72个块。图4.9中的伪码方法size实现的就是这种遍历策略。

如果当前对象不是一个目录，那么 size 只返回它在当前对象中所占用的块数。否则，被该目录占用的块数将被加到在其所有子节点(递归地)中发现的块数上去。为了区别后序遍历策略和先序遍历策略之间的不同，图 4.10 显示了每个目录或文件的大小是如何由该算法算出的。

---

104

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0097-0128/images/page_117_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["/usr*(1)"] --> B["mark*(1)"]
  A --> C["alex*(1)"]
  A --> D["bill*(1)"]
  B --> E["book*(1)"]
  B --> F["course*(1) junk (6)"]
  B --> G["junk (8)"]
  B --> H["work*(1)"]
  D --> I["course*(1)"]
  E --> J["ch1.r(3) ch2.r(2) ch3.r(4)"]
  F --> K["cop3530*(1)"]
  G --> L["cop3212*(1)"]
  I --> K
  J --> M["fall*(1)"]
  K --> N["spr*(1)"]
  K --> O["sum*(1)"]
  M --> P["syl.r(1)"]
  N --> Q["syl.r(5)"]
  O --> R["syl.r(2) grades(3)"]
  L --> S["fall*(1)"]
  L --> T["spr*(1)"]
  S --> U["prog1.r(4) prog2.r(1)"]
  T --> V["prog2.r(2) prog1.r(7) grades(9)"]
```
</details>

图 4.8 经由后序遍历得到的带有文件大小的 UNIX 目录

```cpp
int FileSystem::size( ) const
{
    int totalSize = sizeofThisFile( );

    if( isDirectory( ) )
        for each file c in this directory (for each child)
            totalSize += c.size( );

    return totalSize;
}
```

图 4.9 计算一个目录大小的伪码例程

```asm
ch1.r                     3
    ch2.r                     2
    ch3.r                     4
    book                    10
        syl.r     1
        fall                 2
            syl.r     5
        spr                   6
            syl.r     2
        sum                   3
    cop3530             12
    course                   13
    junk                   6
mark                            30
    junk                   8
alex                            9
    work                   1
        grades     3
        prog1.r   4
        prog2.r   1
        fall                 9
            prog2.r   2
            prog1.r   7
            grades     9
        spr                   19
    cop3212             29
    course                   30
bill                        32
/usr                         72
```

图 4.10 函数 size 的印迹

---

第4章 树

105

## 4.2 二叉树

二叉树(binary tree)是一棵树，其中每个节点都不能有多于两个的儿子。

图4.11显示，一棵二叉树由一个根和两棵子树 $T_{L}$ 和 $T_{R}$ 组成， $T_{L}$ 和 $T_{R}$ 均可能为空。

二叉树的一个性质是平均二叉树的深度要比节点个数 $N$ 小得多，这个性质有时很重要。分析表明，其平均深度为 $O(\sqrt{N})$ ，而对于特殊类型的二叉树，即二叉查找树(binary search tree)，其深度的平均值是 $O(\log N)$ 。遗憾的是，正如图4.12中的例子所示，这个深度是可以大到 $N - 1$ 的。

![](../../raw/pages_0097-0128/images/page_118_image_6.jpg)

<details>
<summary>text_image</summary>

根
T_L
T_R
</details>

图 4.11 一般二叉树

![](../../raw/pages_0097-0128/images/page_118_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["A"] --> B["B"]
  B --> C["C"]
  C --> D["D"]
  D --> E["E"]
```
</details>

图 4.12 最坏情形的二叉树

## 4.2.1 实现

因为一个二叉树节点最多有两个儿子，所以我们可以保存直接链接到它们的链。树节点的声明在结构上类似于双向链表的声明，因为一个节点就是由 element 的信息加上两个指向其他节点的指针(left 和 right)组成的结构(见图 4.13)。

```c
struct BinaryNode
{
    Object      element;      // 节点上的数据
    BinaryNode *left;          // 左儿子
    BinaryNode *right;       // 右儿子
};
```

图 4.13 二叉树节点类(伪代码)

我们是可以用在画链表时习惯使用的矩形框画出二叉树的，不过，树一般画成圆圈并用一些直线连接起来，因为它们实际上就是图(graph)。当涉及到树时，我们也不显式地画出nullptr链，因为每一棵具有 $N$ 个节点的二叉树都需要 $N + 1$ 个nullptr链。

二叉树有许多与搜索无关的重要应用。二叉树的主要用处之一是在编译器设计领域，我们现在就来探索这个问题。

## 4.2.2 一个例子——表达式树

图 4.14 显示的是一个表达式树 (expression tree) 的例子。表达式树的树叶是操作数 (operand)，如常数或变量名字，而其他的节点为操作符 (operator)。由于这里所有的操作都是二元 (二目) 的，因此这棵特定的树正好是二叉树。虽然这是最简单的情况，但是节点还是有可能含有多于两个的儿子的。一个节点也有可能只有一个儿子，如具有一目减运算符 (unary

---

106

数据结构与算法分析——C++语言描述(第四版)

minus operator)的情形。我们可以将通过递归计算左子树和右子树所得到的值应用在根处的运算符上而算出表达式树 $T$ 的值。在我们的例子中，左子树的值是 $a + (b*c)$，右子树的值是 $((d*e) + f)*g$，因此整个树表示为 $(a + (b*c)) + (((d*e) + f)*g)$。

![](../../raw/pages_0097-0128/images/page_119_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["+"] --> B["a"]
  A --> C["*"]
  A --> D["+"]
  C --> E["b"]
  C --> F["c"]
  D --> G["*"]
  D --> H["g"]
  C --> I["d"]
  C --> J["e"]
  D --> K["+"]
  D --> L["f"]
```
</details>

图4.14 $(a + b*c) + ((d*e + f)*g)$ 的表达式树

我们可以通过递归地产生一个带括号的左表达式，然后打印出在根处的运算符，最后再递归地产生一个带括号的右表达式而得到一个(对两个括号整体进行运算的)中缀表达式(infix expression)。这种一般的方法(左，节点，右)称为中序遍历(inorder traversal)。由于其产生的表达式类型，这种遍历很容易记忆。

另一种遍历策略是递归地打印出左子树、右子树，然后打印运算符。如果应用这种策略于上面的树，则输出将是  $abc*+de*f+g*+$ 。容易看出，它就是 3.6.3 节中的后缀表示法。这种遍历策略一般称为后序遍历(postorder traversal)。我们已在 4.1 节见过这种遍历方法。

第三种遍历策略是先打印出运算符，然后递归地打印出左子树和右子树。此时得到的表达式++a\*bc\*++\*defg 是不太常用的前缀 (prefix) 记法，这种遍历策略为先序遍历 (preorder traversal)，我们也在 4.1 节见过它。以后，我们还要讨论这些遍历方法。

## 构造一棵表达式树

现在给出一种算法来把后缀表达式转变成表达式树。由于已经有了将中缀表达式转变成后缀表达式的算法，因此我们能够从这两种常用类型的输入生成表达式树。这里所描述的方法酷似3.6.3节的后缀求值算法。我们一次一个符号地读入表达式。如果符号是操作数，那么就建立一个单节点树并将指向它的指针推入栈中。如果符号是操作符，那么就从栈中弹出指向两棵树 $T_{1}$ 和 $T_{2}$ （的两个指针） $(T_{1}$ 的先弹出)并形成一棵新的树，该树的根就是操作符，它的左、右儿子分别是 $T_{2}$ 和 $T_{1}$ 。然后将指向这棵新树的指针压入栈中。

来看一个例子。设输入为

$$
\mathrm{a} \mathrm{b} + \mathrm{c} \mathrm{d} \mathrm{e} + * *\left. \right.
$$

前两个符号是操作数，因此创建两棵单节点树并将它们压入栈中。 $^{①}$

![](../../raw/pages_0097-0128/images/page_119_image_13.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Initial State"] --> B["a"]
  B --> C["b"]
```
</details>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 为了方便起见，我们将让图中的栈从左到右增长。</span></small>

---

第4章 树

107

接着，+被读入，因此指向两棵树的指针被弹出，一棵新的树形成，指向新树的指针被压入栈中。

![](../../raw/pages_0097-0128/images/page_120_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A[""] --> B{"+"}
  B --> C["a"]
  B --> D["b"]
```
</details>

然后，c、d 和 e 被读入，在每个单节点树创建后，对应的指向树的指针被压入栈中。

![](../../raw/pages_0097-0128/images/page_120_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A[""] --> B["+"]
  B --> C["c"]
  B --> D["d"]
  B --> E["e"]
  B --> F["a"]
  B --> G["b"]
```
</details>

接下来读入+号，因此右边的两棵树合并。

![](../../raw/pages_0097-0128/images/page_120_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Top Node"] --> B["+"]
  B --> C["a"]
  B --> D["b"]
  B --> E["c"]
  B --> F["d"]
  B --> G["e"]
```
</details>

继续进行，读入\*号，因此，我们弹出两棵树的两个指针并形成一棵新的树，\*号是它的根。

![](../../raw/pages_0097-0128/images/page_120_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A[""] --> B{"+"}
  B -->|a| C["a"]
  B --> D["b"]
  B --> E["*"]
  D --> F["b"]
  E --> G["c"]
  E --> H["d"]
  E --> I["e"]
  G --> J{"+"}
  H --> J
  I --> J
```
</details>

最后，读入最后一个符号，两棵树合并，而指向最后的树的指针被留在栈中。

---

108

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0097-0128/images/page_121_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A[""] --> B["*"]
  B --> C["+"]
  B --> D["*"]
  C --> E["a"]
  C --> F["b"]
  D --> G["c"]
  D --> H["d"]
  D --> I["e"]
```
</details>

## 4.3 查找树 ADT——二叉查找树

二叉树的一个重要的应用是它们在搜索中的使用。假设树中的每个节点存储一项数据。在我们的例子中，虽然任意复杂的项在 $\mathrm{C}++$ 中都容易处理，但为简单起见还是假设它们都是整数。我们还将假设，所有的项彼此互异，以后再处理有重复项的情况。

使二叉树成为二叉查找树的性质是，对于树中的每个节点 $X$ ，它的左子树中所有项的值均小于 $X$ 中的项，而它的右子树中所有项的值均大于 $X$ 中的项。注意，这意味着，该树所有的元素可以用某种一致的方式排序。在图4.15中，左边的树是二叉查找树，但右边的树不是。右边的树在其项是6的节点(该节点正好是根节点)的左子树中，有一个节点的项是7。

![](../../raw/pages_0097-0128/images/page_121_image_6.jpg)

图 4.15 两棵二叉树(只有左边的树是查找树)

现在给出通常对二叉查找树进行的操作的简要描述。注意，由于树的递归定义，通常是递归地编写这些操作的例程。因为二叉查找树的平均深度是 $O(\log N)$，所以一般不必担心栈空间被用尽。

图 4.16 显示的是 BinarySearchTree 类模板的接口。这里有几项要注意的事情。查找是基于操作符<的，它必须被定义成特定的 Comparable 类型。特别地，如果 x<y 和 y<x 均为 false，那么项 x 匹配项 y。这使得 Comparable 可以是一个复杂的类型（比如雇员的记录），不过，比较功能只在类型的一部分上定义（如社会保险号数据成员或工资）。1.6.3 节阐释设计能够用作 Comparable 的类的一般方法。在 4.3.1 节描述的另一种方法适用于函数对象。

数据成员是一个指向根结点的指针。对于空树，这个指针为 nullptr。public 成员函数使用一般的技巧调用 private 的递归函数。图 4.17 中显示了一个例子，说明对于 contains、insert 和 remove，这种技巧是如何实施的。

---

第4章 树

109

```cpp
template <typename Comparable>
class BinarySearchTree
{
    public:
        BinarySearchTree( );
        BinarySearchTree( const BinarySearchTree & rhs );
        BinarySearchTree( BinarySearchTree && rhs );
        ~BinarySearchTree( );

        const Comparable & findMin( ) const;
        const Comparable & findMax( ) const;
        bool contains( const Comparable & x ) const;
        bool isEmpty( ) const;
        void printTree( ostream & out = cout ) const;

        void makeEmpty( );
        void insert( const Comparable & x );
        void insert( Comparable && x );
        void remove( const Comparable & x );

        BinarySearchTree & operator=( const BinarySearchTree & rhs );
        BinarySearchTree & operator=( BinarySearchTree && rhs );

private:
    struct BinaryNode
    {
        Comparable element;
        BinaryNode *left;
        BinaryNode *right;

        BinaryNode( const Comparable & theElement, BinaryNode *lt, BinaryNode *rt )
            : element{ theElement }, left{ lt }, right{ rt } { }

        BinaryNode( Comparable && theElement, BinaryNode *lt, BinaryNode *rt )
            : element{ std::move( theElement ) }, left{ lt }, right{ rt } { }
    };

    BinaryNode *root;

    void insert( const Comparable & x, BinaryNode * & t );
    void insert( Comparable && x, BinaryNode * & t );
    void remove( const Comparable & x, BinaryNode * & t );
    BinaryNode * findMin( BinaryNode *t ) const;
    BinaryNode * findMax( BinaryNode *t ) const;
    bool contains( const Comparable & x, BinaryNode *t ) const;
    void makeEmpty( BinaryNode * & t );
    void printTree( BinaryNode *t, ostream & out ) const;
    BinaryNode * clone( BinaryNode *t ) const;
};
```

图 4.16 二叉查找树类架构

几个 private 型成员函数通过传引用调用(call-by-reference)使用传递指针变量的技巧。这使得 public 型成员函数能够把指向根结点的指针传递给 private 型的递归成员函数。这些递归函数此时可以改变根的值，使得 root 指向另外的节点。当考查 insert 的代码时，我们将详细描述这种技巧。

---

110

数据结构与算法分析——C++语言描述(第四版)

现在，我们可以描述一些 private 型的方法了。

```c
/**
 * 如果在树中找到 x，则返回true.
 */
bool contains( const Comparable & x ) const
{
    return contains( x, root );
}

/**
 * 将x插入到树中;忽略重复元.
 */
void insert( const Comparable & x )
{
    insert( x, root );
}

/**
 * 将x从树中删除。如果没找到x，则什么也不做。
*/
void remove( const Comparable & x )
{
    remove( x, root );
}
```

图 4.17 公有成员函数调用私有递归函数的图示

## 4.3.1 contains

如果在树 $T$ 中存在含有项 $X$ 的节点，那么这个操作需要返回 true，如果这样的节点不存在则返回 false。树的结构使得这种操作很简单。如果 $T$ 是空集，那么可以直接返回 false。否则，如果存储在 $T$ 处的项是 $X$，那么可以返回 true。否则，我们对树 $T$ 的左子树或右子树进行一次递归调用，这依赖于 $X$ 与存储在 $T$ 中的项的关系。图4.18中的代码就是对这种策略的一种实现。

```c
/**
 * 测试一项是否在子树上的内部方法.
 * x 是要查找的项.
 * t 是作为该子树的根的节点.
 */
bool contains( const Comparable & x, BinaryNode *t ) const
{
    if( t == nullptr )
        return false;
    else if( x < t->element )
        return contains( x, t->left );
    else if( t->element < x )
        return contains( x, t->right );
    else
        return true;   // 匹配
}
```

图 4.18 二叉查找树的 contains 操作

---

第 4 章 树

111

注意测试的顺序。关键的问题是首先要对是否空树进行测试，因为否则就会产生一个企图通过 nullptr 指针访问数据成员的运行时错误。剩下的测试使得最不可能的情况安排在最后进行。还要注意，这里的两个递归调用事实上都是尾递归并且可以用一个 while 循环很容易地将它们替换掉。尾递归的使用在这里是合理的，因为算法表达式的简明性是以速度的降低为代价的，而这里所使用的栈空间的量也只不过是 $O(\log N)$ 而已。

图 4.19 显示了一些简单的变化，它们需要使用一个函数对象而不是要求这些项是 Comparable 的。程序模仿了 1.6.4 节的风格。

```cpp
template <typename Object, typename Comparator=less<Object>>
class BinarySearchTree
{
    public:
        // 方法相同，但用 Object 代替Comparable

    private:
        BinaryNode *root;
        Comparator isLessThan;

        // 方法相同，但用 Object 代替Comparable

        /**
         * 检测一项是否在子树上的内部方法.
         * x 是要查找的项.
         * t 是作为子树的根的节点.
         */
        bool contains( const Object & x, BinaryNode *t ) const
        {
            if( t == nullptr )
                return false;
            else if( isLessThan( x, t->element ) )
                return contains( x, t->left );
            else if( isLessThan( t->element, x ) )
                return contains( x, t->right );
            else
                return true;   // 匹配
        }
};
```

图4.19 对使用函数对象实现二叉查找树的图示

## 4.3.2 findMin 和 findMax

这两个 private 例程分别返回指向树中包含最小元素和包含最大元素的节点的指针。为执行 findMin，从根开始并且只要有左儿子就向左查找。终止点就是最小的元素。findMax 例程除分支朝向右儿子外其余过程相同。

许多程序设计员不厌其烦地使用递归。我们用递归的方法将 finMin 写成例程(见图 4.20)，并用非递归的方法将 findMax 写成例程(见图 4.21)。

---

112

数据结构与算法分析——C++语言描述(第四版)

```c
/**
 * 找出子树 t 中最小项的内部方法.
 * 返回包含最小项的节点.
 */
BinaryNode * findMin( BinaryNode *t ) const
{
    if( t == nullptr )
        return nullptr;
    if( t->left == nullptr )
        return t;
    return findMin( t->left );
}
```

图 4.20 对二叉查找树 findMin 的递归实现

```c
/**
 * 找出子树 t 上最大项的内部方法.
 * 返回包含最大项的节点.
 */
BinaryNode * findMax( BinaryNode *t ) const
{
    if( t != nullptr )
        while( t->right != nullptr )
            t = t->right;
    return t;
}
```

图 4.21 对二叉查找树 findMax 的非递归实现

注意，我们是如何小心地处理空树的退化情况的。虽然这么做总是重要的，但是特别在递归程序中它尤其重要。此外，还要注意，在 findMax 中对 t 的改变是安全的，因为我们只用到指针的拷贝来进行工作。不管怎么说，还是应该随时特别小心，因为像 t->right=t->right->right 这样的语句将会产生一些变化。

## 4.3.3 insert

实现插入的例程在概念上是简单的。为了将 $X$ 插入到树 $T$ 中，可以像 contains 那样沿着树查找。如果找到 $X$，则什么也不用做。否则，将 $X$ 插入到所遍历的路径的最后一点上。图 4.22 显示了实际的插入情况。为了插入 5，我们就好像在运行 contains 一样遍历该树。在带有项 4 的节点处，我们需要向右行进，但右边不存在子树，因此 5 不在这棵树上，从而这个位置就是插入 5 的正确位置。

![](../../raw/pages_0097-0128/images/page_125_image_9.jpg)

图 4.22 插入 5 以前和以后的二叉查找树

---

第4章 树

113

重复元的插入可以通过在节点记录中保留一个附加域以指示发生的频率来处理。这对整个的树增加了某些附加空间，但是，却比将重复元放到树中要好(它将使树的深度变得很大)。当然，如果操作符<用到的关键字只是一个更大结构的一部分，那么这种方法行不通。此时可以把具有相同关键字的所有结构保留在一个辅助数据结构中，譬如表或另一棵查找树。

图 4.23 显示了插入例程的程序。第 12 行和第 14 行递归地将 x 插入到相应的子树中。注意，在递归例程中，唯一一次 t 变化的时刻是在一片新树叶创建的时候。此时意味着，递归例程已经从某个其他的节点 p 处被调用，而这个节点将是新建树叶的父亲。该调用将是 insert(x, p->left) 或 insert(x, p->right)。不管哪种方法，t 现在都是对 p->left 或 p->right 的引用，这就意味着，p->left 或 p->right 将改变以指向新的节点。总的来说，方法简明巧妙。

```cpp
/**
 * 向子树插入元素的内部方法.
 * x 是要插入的项.
 * t 为该子树的根节点.
 * 置子树的新根.
 */
void insert( const Comparable & x, BinaryNode * & t )
{
    if( t == nullptr )
        t = new BinaryNode{ x, nullptr, nullptr };
    else if( x < t->element )
        insert( x, t->left );
    else if( t->element < x )
        insert( x, t->right );
    else
        ; // 重复元; 什么也不做
}

/**
 * 向子树插入元素的内部方法.
 * x 是通过移动实现要插入的项.
 * t 为该子树的根.
 * 置子树的新根.
 */
void insert( Comparable && x, BinaryNode * & t )
{
    if( t == nullptr )
        t = new BinaryNode{ std::move( x ), nullptr, nullptr };
    else if( x < t->element )
        insert( std::move( x ), t->left );
    else if( t->element < x )
        insert( std::move( x ), t->right );
    else
        ; // 重复元; 什么也不做
}
```

图 4.23 向二叉查找树进行插入的例程

## 4.3.4 remove

正如许多数据结构一样，最困难的操作是删除。一旦发现要被删除的节点，我们就需要考虑几种可能的情况。

---

114

数据结构与算法分析——C++语言描述(第四版)

如果节点是一片树叶，那么它可以被立即删除。如果节点有一个儿子，则该节点可以在其父节点调整它的链以绕过该节点后被删除(为了清楚起见，我们将明确地画出链的指向)，见图4.24。

![](../../raw/pages_0097-0128/images/page_127_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  C["3"] --> D["4"]
  E["6"] --> F["8"]
  B --> G["1"]
  B --> H["2"]
  D --> I["3"]
  F --> J["6"]
  G --> K["1"]
  H --> L["2"]
  I --> M["4"]
  J --> N["6"]
  K --> O["1"]
  L --> P["2"]
  M --> Q["3"]
  N --> R["8"]
```
</details>

图4.24 具有一个儿子的节点(4)删除前后的情况

复杂的是处理具有两个儿子的节点的情况。一般的删除策略是用其右子树的最小的数据(很容易找到)代替该节点的数据并递归地删除那个节点(现在它是空的)。因为右子树中的最小的节点不可能有左儿子，所以第二次 remove 要容易。图 4.25 显示一棵初始的树及其中一个节点被删除后的结果。要被删除的节点是根的左儿子，其关键字的值为 2。它被右子树中的最小数据 (3) 所代替，然后关键字是 3 的原节点如前例那样被删除。

![](../../raw/pages_0097-0128/images/page_127_image_6.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["6"] --> B["2"]
  A --> C["8"]
  B --> D["1"]
  B --> E["5"]
  E --> F["3"]
  F --> G["4"]
  C --> H["6"]
  H --> I["8"]
  J["3"] --> K["1"]
  J --> L["5"]
  L -.-> M["3"]
  M --> N["4"]
  I --> O["6"]
  O --> P["8"]
```
</details>

图 4.25 删除具有两个儿子的节点(2)前后的情况

图 4.26 中的程序实施删除的工作，但它的效率并不高，因为它沿该树进行两趟搜索以查找和删除右子树中最小的节点。通过写一个特殊的 removeMin 方法可以容易地克服这种效率不高的缺点，我们这里将它略去只是为了简明。

如果预计删除的次数不多，则通常使用的策略是懒惰删除(lazy deletion):当一个元素要被删除时，它仍然留在树中，而是只作了个被删除的标记。这特别是在有重复项时很流行，因为此时记录出现频率数的域可以减1。如果树中的实际节点数和“被删除”的节点数相同，那么树的深度预计只上升一个小的常数(为什么？)，因此，存在一个与懒惰删除相关的非常小的时间损耗。再有，如果被删除的项被重新插入，那么分配一个新单元的开销也就避免了。

---

第4章 树

115

```c
/**
 * 从一棵子树删除一项的内部方法.
 * 参数 x 是要被删除的项.
 * 参数 t 为该子树的根节点.
 * 置该子树的新的根.
 */
void remove( const Comparable & x, BinaryNode * & t )
{
    if( t == nullptr )
        return;   // 项没找到; 什么也不做
    if( x < t->element )
        remove( x, t->left );
    else if( t->element < x )
        remove( x, t->right );
    else if( t->left != nullptr && t->right != nullptr ) // 有两个儿子
    {
        t->element = findMin( t->right )->element;
        remove( t->element, t->right );
    }
    else
    {
        BinaryNode *oldNode = t;
        t = ( t->left != nullptr ) ? t->left : t->right;
        delete oldNode;
    }
}
```

图4.26 二叉查找树的删除例程

## 4.3.5 析构函数和拷贝构造函数

通常，析构函数调用 makeEmpty。这个公有的 makeEmpty 函数(未显示)直接调用私有递归版本的 makeEmpty 函数。如图 4.27 所示，在递归地处理 t 的子节点之后，则对 t 调用 delete 函数。因此，所有的节点都将被递归地回收。注意，最后，t 从而 root 改为指向 nullptr。拷贝构造函数如图 4.28 所示，遵循通常的过程，首先初始化 root 为 nullptr，然后复制 rhs 的拷贝。我们使用一个非常成熟的递归函数来处理所有这些苦活，这个递归函数名为 clone。

## 4.3.6 平均情况分析

直观上, 我们期望这一节描述的所有操作(除makeEmpty和复制外)都应该花费 $O(\log N)$ 时间, 因为我们以常数时间在树中降低了一层, 这样一来, 现在对树进行的操作大致减小一半左右。实际上, 所有操作的运行时间(除makeEmpty和复制外)都是 $O(d)$, 其中 $d$ 是包含所访问项的节点的深度(在remove的情形, 它可能是两个儿子情形的替代节点)。

我们在本节要证明，在所有的插入序列都是等可能的假设下，则树的所有节点的平均深度为 $O(\log N)$。

一棵树的所有节点的深度之和称为内部路径长 (internal path length)。我们现在将要计算二叉查找树的平均内部路径长，其中的平均是对向二叉查找树中所有可能的插入序列进行的。

---

116

数据结构与算法分析——C++语言描述(第四版)

```c
/**
 * 二叉查找树的析构函数
 */
~BinarySearchTree( )
{
    makeEmpty( );
}
/**
 * 使子树为空的内部方法.
 */
void makeEmpty( BinaryNode * & t )
{
    if( t != nullptr )
    {
        makeEmpty( t->left );
        makeEmpty( t->right );
        delete t;
    }
    t = nullptr;
}
```

图 4.27 析构函数与递归成员函数 makeEmpty

```txt
/**
 * 拷贝构造函数
 */
BinarySearchTree( const BinarySearchTree & rhs ) : root{ nullptr }
{
    root = clone( rhs.root );
}

/**
 * 克隆子树的内部方法.
 */
BinaryNode * clone( BinaryNode *t ) const
{
    if( t == nullptr )
        return nullptr;
    else
        return new BinaryNode{ t->element, clone( t->left ), clone( t->right ) };
}
```

图 4.28 拷贝构造函数与递归成员函数 clone

令 $D(N)$ 是具有 $N$ 个节点的某棵树 $T$ 的内部路径长，$D(1) = 0$。一棵 $N$ 节点树是由一棵 $i$ 节点左子树和一棵 $(N - i - 1)$ 节点右子树以及深度 0 处的一个根节点组成的，其中 $0 \leqslant i < N, D(i)$ 为根的左子树的内部路径长。但是在原树中，所有这些节点都要加深一层。同样的结论对于右子树也是成立的。由此，我们得到递推关系:

$$
D (N) = D (i) + D (N - i - 1) + N - 1
$$

如果所有子树的大小都是等可能地出现，这对于二叉查找树(但对于二叉树不)是成立的(因为子树的大小只依赖于第一个插入到树中的元素相对的秩(rank))，那么 $D(i)$ 和 $D(N - i - 1)$ 的

---

第4章 树

117

平均值都是 $(1 / N)\sum_{j = 0}^{N - 1}D(j)$ 。于是得到

$$
D (N) = \frac {2}{N} \left[ \sum_ {j = 0} ^ {N - 1} D (j) \right] + N - 1
$$

在第7章将遇到并求解这个递推式，得到的平均值为 $D(N) = O(N \log N)$ 。因此，任意节点的期望深度为 $O(\log N)$ 。作为一个例子，图4.29所示随机生成的500个节点的树的节点期望深度为9.98。

但是，上来就断言这个结果意味着上一节讨论的所有操作的平均运行时间是 $O(\log N)$ 颇有诱惑力，但这并不完全正确。原因在于删除操作，我们并不清楚是否所有的二叉查找树都是等可能出现的。特别是，上面描述的删除算法有助于使得左子树比右子树深度深，因为我们总是用右子树的一个节点来代替删除的节点。这种方法的准确的效果仍然是未知的，但它似乎只是理论上的悬念。业已证明，如果交替插入和删除 $\Theta (N^2)$ 次，那么树的期望深度将是 $\Theta (\sqrt{N})$ 。在进行25万次随机insert/remove对操作后，图4.29中有些右沉的树在图4.30中看起来就变得太不平衡了(平均深度 $= 12.51$ )。

![](../../raw/pages_0129-0160/images/page_130_image_6.jpg)

<details>
<summary>natural_image</summary>

Abstract line drawing of branching, tree-like structures with no text or symbols
</details>

图 4.29 一棵随机生成的二叉查找树

![](../../raw/pages_0129-0160/images/page_130_image_8.jpg)

<details>
<summary>natural_image</summary>

Line drawing of a long, curved, leaf-like structure with no text or symbols
</details>

图4.30 在 $\Theta(N^2)$ 次 insert/remove 对操作后的二叉查找树

在删除操作中, 可以通过随机选取右子树的最小元素或左子树的最大元素来代替被删除的元素以消除这种不平衡问题。这种做法明显地消除了上述偏向并使树保持平衡, 但是, 没有人实际上证明过这一点。无论如何, 这种现象似乎主要是理论上的问题, 因为对于小的树上述效果根本显示不出来, 甚至更奇怪, 如果使用 $o(N^{2})$ insert/remove 对操作, 那么树似乎可以得到平衡。

上面的讨论主要是说明，决定“平均”意味着什么一般是极其困难的，可能需要一些假设，而这些假设可能合理，也可能不合理。不过，在没有删除或是使用懒惰删除的情况下，我们可以断言:上述那些操作的平均运行时间都是 $O(\log N)$ 。除像上面讨论的一些个别情形外，这个结果与实际观察到的情形是非常一致的。

如果向一棵树输入预先排序的数据，那么一连串 insert 操作将花费二次的(quadratic)时间，而链表实现的代价会非常巨大，因为此时的树将只由那些没有左儿子的节点组成。一种解决办法就是要有一个称为平衡(balance)的附加结构条件:任何节点的深度均不得过深。

有许多一般的算法实现平衡树。但是，大部分算法都要比标准的二叉查找树复杂得多，而且更新要平均花费更长的时间。不过，它们确实防止了处理起来非常麻烦的一些简单情形。下面将介绍最老的一种平衡查找树，即 AVL 树 (AVL tree)。

第二种方法是放弃平衡条件，允许树有任意的深度，但是在每次操作之后要使用一个调

---

118

数据结构与算法分析——C++语言描述(第四版)

整规则进行调整，使得后面的操作效率要高。这种类型的数据结构一般属于自调整(self-adjusting)类结构。在二叉查找树的情况下，对于任意单次操作我们不再保证 $O(\log N)$ 的时间界，但是可以证明任意连续 $M$ 次操作在最坏的情形下花费时间 $O(M\log N)$ 。一般这足以防止令人棘手的最坏情形。我们将要讨论的这种数据结构叫作伸展树(splay tree)，它的分析相当复杂，我们将在第11章讨论。

## 4.4 AVL 树

AVL (Adelson-Velskii 和 Landis) 树是带有平衡条件 (balance condition) 的二叉查找树。这

个平衡条件必须要容易保持，而且它保证树的深度是 $O(\log N)$ 。最简单的想法是要求左右子树具有相同的高度。如图4.31所示，这种想法并不强求树的深度要浅。

另一种平衡条件是要求每个节点都必须要有相同高度的左子树和右子树。如果空子树的高度定义为-1（通常就是这么定义），那么只有具有 $2^{k} - 1$ 个节点的理想平衡树(perfectly balanced tree)满足这个标准。因此，虽然这种平衡条件保证了树的深度小，但是它太严格了以至难以使用，需要把它放宽。

![](../../raw/pages_0129-0160/images/page_131_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Start Node"] --> B["Intermediate Node 1"]
  B --> C["Intermediate Node 2"]
  C --> D["Intermediate Node 3"]
  D --> E["Intermediate Node 4"]
  E --> F["Intermediate Node 5"]
  F --> G["End Node"]
```
</details>

图 4.31 一棵坏的二叉树。只要求在根节点平衡是不够的

一棵 AVL 树 (AVL tree) 是其每个节点的左子树和右子树的高度最多差 1 的二叉查找树。(空树的高度定义为 -1。) 在图 4.32 中, 左边的树是 AVL 树, 但右边的树不是。每一个节点 (在其节点结构中) 保留高度信息。可以证明, 粗略地说, 一棵 AVL 树的高度最多为 $1.44 \log (N + 2) - 1.328$, 而实际上的高度只比 $\log N$ 稍微多一些。作为例子, 图 4.33 显示一棵具有最少节点 (143) 高度为 9 的 AVL 树。这棵树的左子树是高度为 7 且大小最小的 AVL 树, 右子树是高度为 8 且大小最小的 AVL 树。它告诉我们, 在高度为 $h$ 的 AVL 树中, 最少节点数 $S(h)$ 由 $S(h) = S(h - 1) + S(h - 2) + 1$ 给出。对于 $h = 0, S(h) = 1$; 而当 $h = 1$ 时, $S(h) = 2$ 。函数 $S(h)$ 与斐波那契数 (Fibonacci number) 密切相关, 由此推出上面提到的关于 AVL 树的高度的界。

![](../../raw/pages_0129-0160/images/page_131_image_10.jpg)

图 4.32 两棵二叉查找树，只有左边的树是 AVL 树

因此，除去可能的插入和删除外，所有的树操作都可以以时间 $O(\log N)$ 执行。当进行插入操作时，我们需要更新通向根节点路径上那些节点的所有平衡信息，而插入操作隐含着困难的原因在于，插入一个节点可能破坏AVL树的特性。（例如，将6插入到图4.32的AVL树中将会破坏关键字为8的节点处的平衡条件。）如果发生这种情况，那么就要在考虑这一步插入完成之前恢复平衡的性质。事实上，这总可以通过对树进行简单的修正来做到，我们称其为旋转(rotation)。

---

第4章 树

119

![](../../raw/pages_0129-0160/images/page_132_image_2.jpg)

<details>
<summary>natural_image</summary>

Abstract geometric tree-like structure composed of interconnected nodes and lines, no text or symbols present
</details>

图4.33 高度为9的最小的AVL树

在一次插入之后，只有那些从插入点到根节点的路径上的节点的平衡可能被改变，因为只有这些节点的子树可能发生变化。当沿着这条路径上行到根并更新平衡信息时，我们可以发现一个节点，它的新平衡破坏了 AVL 条件。我们将指出如何在第一个这样的节点(即最深的节点)重新平衡这棵树，并证明，这一重新平衡保证整个树满足 AVL 性质。

我们把必须重新平衡的节点叫作 $\alpha$ 。由于任意节点最多有两个儿子，因此出现高度不平衡就需要 $\alpha$ 点的两棵子树的高度差2。容易看出，这种不平衡可能出现在下面4种情况中:

1. 对 $\alpha$ 的左儿子的左子树进行一次插入。
2. 对 $\alpha$ 的左儿子的右子树进行一次插入。
3. 对 $\alpha$ 的右儿子的左子树进行一次插入。
4. 对 $\alpha$ 的右儿子的右子树进行一次插入。

情形 1 和 4 是关于  $\alpha$  点的镜像对称 (mirror image symmetry)，而情形 2 和 3 也是关于  $\alpha$  点的镜像对称。因此，理论上只有两种基本情况，当然从编程的角度来看还是 4 种情形。

第一种情况是插入发生在“外边”的情况(即左-左的情况或右-右的情况)，该情况通过对树的一次单旋转(single rotation)而完成调整。第二种情况是插入发生在“内部”的情形(即左右的情况或右-左的情况)，该情况通过稍微复杂些的双旋转(double rotation)来处理。我们将会看到，这些都是对树的基本操作，它们多次用在一些平衡树算法中。本节其余部分将描述这些旋转，证明它们足以保持树的平衡，并顺便给出 AVL 树的一种非正式的实现。第 12 章描述其他的平衡树方法，这些方法着眼于 AVL 树的更仔细的实现。

## 4.4.1 单旋转

图 4.34 显示单旋转如何调整情形 1。旋转前的图在左边，而旋转后的图在右边。让我们来仔细分析具体的做法。节点 $k_{2}$ 不满足 AVL 平衡性质，因为它的左子树比右子树深 2 层（图中间的几条虚线标示树的各层）。该图所描述的情况只是情形 1 的一种可能的情况，在插入之前 $k_{2}$ 满足 AVL 性质，但在插入之后这种性质被破坏了。子树 $X$ 已经长出一层，这使得它比子树 $Z$ 深出 2 层。$Y$ 不可能与新 $X$ 在同一水平上，因为那样 $k_{2}$ 在插入以前就已经失去平衡了；$Y$ 也不可能与 $Z$ 在同一层上，因为那样 $k_{1}$ 就会是在通向根的路径上破坏 AVL 平衡条件的第一个节点。

---

120

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0129-0160/images/page_133_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["k1"] --> B["k2"]
  A --> C["X"]
  A --> D["Y"]
  A --> E["Z"]
  B --> F["k1"]
  B --> G["k2"]
  C --> F
  C --> G
  D --> F
  D --> G
  E --> F
  E --> G
```
</details>

图4.34 调整情形1的单旋转

为使树恢复平衡，我们把 $X$ 上移一层，并把 $Z$ 下移一层。注意，此时实际上超出了 AVL 性质的要求。为此，我们重新安排节点以形成一棵等价的树，如图 4.34 的第二部分所示。抽象地形容就是:把树形象地看成是柔软灵活的，抓住子节点 $k_{1}$，闭上你的双眼，使劲摇动它，在重力作用下，$k_{1}$ 就变成了新的根。二叉查找树的性质告诉我们，在原树中 $k_{2} > k_{1}$，于是在新树中 $k_{2}$ 变成了 $k_{1}$ 的右儿子，$X$ 和 $Z$ 仍然分别是 $k_{1}$ 的左儿子和 $k_{2}$ 的右儿子。子树 $Y$ 包含原树中介于 $k_{1}$ 和 $k_{2}$ 之间的那些项的节点，可以将它放在新树中 $k_{2}$ 的左儿子的位置上，这样，所有对顺序的要求都得到满足。

这样的操作只需要一部分指针改变，结果我们得到另外一棵二叉查找树，它是一棵 AVL 树，因为 X 向上移动了一层，Y 停在原来的水平上，而 Z 下移一层。 $k_{2}$  和  $k_{1}$  不仅满足 AVL 要求，而且它们的子树都恰好处在同一高度上。不仅如此，整个树的新高度恰恰与插入前原树的高度相同，而插入操作却使得子树 X 升高了。因此，通向根节点的路径的高度不需要进一步的修正，因而也不需要进一步的旋转。图 4.35 显示在将 6 插入左边原始的 AVL 树后节点 8 便不再平衡。于是，我们在节点 7 和 8 之间做一次单旋转，结果得到右边的树。

![](../../raw/pages_0129-0160/images/page_133_image_6.jpg)

图 4.35 插入 6 破坏了 AVL 性质，而后经过单旋转又将性质恢复

正如我们较早提到的，情形4代表一种对称的情形。图4.36指出单旋转是如何使用的。让我们演示一个更长一些的例子。假设从初始的空AVL树开始插入关键字3、2和1，然后依序插入 $4\sim 7$ 。在插入关键字1时第一个问题出现了，AVL性质在根处被破坏。我们在根与其左儿子之间施行单旋转修正这个问题。下面是旋转之前和之后的两棵树:

![](../../raw/pages_0129-0160/images/page_133_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["k1"] --> B["k2"]
  C["X"] --> A
  D["Y"] --> A
  E["Z"] --> A
  B --> F["k1"]
  G["X"] --> F
  H["Y"] --> F
  I["Z"] --> F
  F --> J["k2"]
```
</details>

图 4.36 单旋转修复情形 4

---

第4章 树

121

![](../../raw/pages_0129-0160/images/page_134_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  B -.-> C["3"]
  D["2"] --> E["2"]
  E --> F["1"]
  E --> G["3"]
  C --> H["→"]
  F --> H
  G --> H
```
</details>

图中虚线连接两个节点，它们是旋转的主体。下面插入关键字为 4 的节点，这没有问题，但插入 5 破坏了在节点 3 处的 AVL 性质，而通过单旋转又将其修正。除旋转引起的局部变化外，编程人员必须记住:树的其余部分必须被告知该变化。如本例中节点 2 的右儿子必须重新设置以链接到 4 来代替 3。这一点很容易忘记，从而导致树被破坏(4 就会是不可访问的)。

![](../../raw/pages_0129-0160/images/page_134_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  B --> C["3"]
  C -.-> D["4"]
  D --> E["5"]
  F["1"] --> G["2"]
  G --> H["4"]
  H --> I["3"]
  H --> J["5"]
```
</details>

下面插入 6。这在根节点产生一个平衡问题，因为它的左子树高度是 0 而右子树高度为 2。因此我们在根处于 2 和 4 之间实施一次单旋转。

![](../../raw/pages_0129-0160/images/page_134_image_6.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  B -.-> C["4"]
  C --> D["3"]
  C --> E["5"]
  C --> F["6"]
  D --> G["2"]
  E --> G
  F --> G
  G --> H["4"]
  G --> I["5"]
  G --> J["6"]
```
</details>

旋转是通过使节点 2 是 4 的一个儿子而 4 原来的左子树变成节点 2 的新的右子树来完成的。在该子树上的每一个关键字均在 2 和 4 之间，因此这个变换是成立的。我们插入的下一个关键字是 7，它导致了另外的旋转:

![](../../raw/pages_0129-0160/images/page_134_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph sg["\"之前\""]
  A["1"] --> B["2"]
  B --> C["3"]
  C --> D["4"]
  D --> E["5"]
    E -.-> F["6"]
  F --> G["7"]
  end
  subgraph sg_2["\"之后\""]
  H["1"] --> I["2"]
  I --> J["3"]
  J --> K["4"]
  K --> L["5"]
  L --> M["6"]
  M --> N["7"]
  end
```
</details>

## 4.4.2 双旋转

上面描述的算法有一个问题:如图 4.37 所示，对于情形 2 和情形 3 上面的做法无效。问题在于子树 Y 太深，单旋转没有减低它的深度。解决这个问题的双旋转 (double rotation) 如图 4.38 所示。

在图 4.37 中的子树 Y 已经有一项插入其中，这个事实保证它是非空的。因此，可以假设它有一个根和两棵子树。于是，可以把整棵树看成是 4 棵子树由 3 个节点连接。如图所示，

---

122

数据结构与算法分析——C++语言描述(第四版)

恰好树 B 或树 C 中有一棵比 D 深两层(除非它们都是空的)，但是我们不能肯定是哪一棵。事实上这并不要紧，在图 4.38 中 B 和 C 都被画成比 D 低  $1\frac{1}{2}$  层。

![](../../raw/pages_0129-0160/images/page_135_image_3.jpg)

<details>
<summary>flowchart</summary>

This diagram illustrates a hierarchical decomposition or transformation process where two nodes (k1 and k2) are split into two sub-nodes (X, Y, Z), with arrows indicating the direction of transformation.
</details>

图 4.37 单旋转不能修复情形 2

![](../../raw/pages_0129-0160/images/page_135_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> K1["k1"]
  B["B"] --> K2["k2"]
  C["C"] --> K2
  D["D"] --> K3["k3"]
  K1 --> K1
  K1 --> K2
  K2 --> K3
  K3 --> K1
```
</details>

图 4.38 左-右双旋转变修复情形 2

为了重新平衡，我们看到，不能再让 $k_{3}$ 作根了，而图4.34所示的在 $k_{3}$ 和 $k_{1}$ 之间的旋转又解决不了问题，唯一的选择就是把 $k_{2}$ 用作新的根。这迫使 $k_{1}$ 成为 $k_{2}$ 的左儿子，$k_{3}$ 成为它的右儿子，从而完全确定了这4棵树的最终位置。容易看出，最后得到的树满足AVL树的性质，与单旋转的情形一样，我们也把树的高度恢复到插入以前的水平，这就保证所有的重新平衡和高度更新是完善的。图4.39指出，对称情形3也可以通过双旋转得以修正。在这两种情形下，其效果与先在 $\alpha$ 的儿子和孙子之间旋转而后再在 $\alpha$ 和它的新儿子之间旋转的效果是相同的。

![](../../raw/pages_0129-0160/images/page_135_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> K1["k1"]
  B["B"] --> K2["k2"]
  C["C"] --> K3["k3"]
  D["D"] --> K1
  K1 --> K2
  K2 --> K3
  K3 --> L["k1"]
  L --> M["k2"]
  M --> N["k3"]
  N --> O["k3"]
  O --> P["A"]
  O --> Q["B"]
  O --> R["C"]
  O --> S["D"]
```
</details>

图 4.39 右-左双旋转变修复情形 3

我们继续在前面例子的基础上以倒序插入关键字 $10\sim 16$ ，接着插入8，然后再插入9。插入16容易，因为它并不破坏平衡性质，但是插入15就会引起在节点7处的高度不平衡。这属于情形3，需要通过一次右-左双旋转来解决。在我们的例子中，这个右-左双旋转将涉及7、16和15。此时， $k_{1}$ 是具有项7的节点， $k_{3}$ 是具有项16的节点，而 $k_{2}$ 是具有项15的节点。子树 $A$ 、 $B$ 、 $C$ 和 $D$ 都是空树。

![](../../raw/pages_0129-0160/images/page_135_image_11.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  B --> C["4"]
  D["3"] --> E["6"]
  F["5"] --> G["7"]
  H["k1"] -.-> I["k3"]
  J["16"] -.-> K["k2"]
  L["15"] -.-> M["k3"]
  N["2"] --> O["4"]
  P["3"] --> Q["6"]
  R["5"] --> S["15"]
  T["k1"] --> U["7"]
  V["16"] --> W["k3"]
```
</details>

---

第4章 树

123

下面插入 14，它也需要一个双旋转。此时修复该树的双旋转还是右-左双旋转，它将涉及 6、15 和 7。在这种情况下， $k_{1}$ 是具有项 6 的节点， $k_{2}$ 是具有项 7 的节点，而 $k_{3}$ 是具有项 15 的节点。子树 A 的根在项为 5 的节点上，子树 B 是空子树，它是项 7 的节点原先的左儿子，子树 C 置根于项 14 的节点上，最后，子树 D 的根在项为 16 的节点上。

![](../../raw/pages_0129-0160/images/page_136_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph sg["\"之前\""]
  A["1"] --> B["2"]
  B --> C["4"]
  C --> D["6"]
    D -.-> E["k₁"]
  E --> F["5"]
  F --> G["15"]
  G --> H["7"]
  H --> I["16"]
  I --> J["14"]
  end
  subgraph sg_2["\"之后\""]
  K["1"] --> L["2"]
  L --> M["4"]
  M --> N["7"]
  N --> O["k₂"]
  O --> P["k₁"]
  P --> Q["6"]
  Q --> R["15"]
  R --> S["5"]
  S --> T["14"]
  T --> U["16"]
  end
  style A fill:#f9f,stroke:#333
  style K fill:#f9f,stroke:#333
  style L fill:#f9f,stroke:#333
  style M fill:#f9f,stroke:#333
  style N fill:#f9f,stroke:#333
  style O fill:#f9f,stroke:#333
  style P fill:#f9f,stroke:#333
  style Q fill:#f9f,stroke:#333
  style R fill:#f9f,stroke:#333
  style S fill:#f9f,stroke:#333
  style T fill:#f9f,stroke:#333
  style U fill:#f9f,stroke:#333
```
</details>

如果现在插入 13，那么在根处就会产生一个不平衡。由于 13 不在 4 和 7 之间，因此我们知道一次单旋转就能完成修正的工作。

![](../../raw/pages_0129-0160/images/page_136_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph Before_Process["\"Before Process\""]
  A["1"] --> B["2"]
  B --> C["3"]
    C -.-> D["4"]
  D --> E["7"]
  E --> F["6"]
  F --> G["5"]
  G --> H["15"]
  H --> I["14"]
  I --> J["13"]
  J --> K["16"]
  end
  subgraph After_Process["\"After Process\""]
  L["1"] --> M["2"]
  M --> N["3"]
  N --> O["5"]
  O --> P["6"]
  P --> Q["15"]
  Q --> R["7"]
  R --> S["14"]
  S --> T["13"]
  T --> U["16"]
  U --> V["15"]
  V --> W["16"]
  end
```
</details>

12 的插入也需要一次单旋转:

![](../../raw/pages_0129-0160/images/page_136_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph Before["之前"]
  A["1"] --> B["2"]
  B --> C["3"]
  C --> D["5"]
    D -.-> E["13"]
  E --> F["12"]
  F --> G["4"]
  G --> H["7"]
  I["15"] --> J["14"]
  J --> K["16"]
  end
  subgraph After["之后"]
  L["1"] --> M["2"]
  M --> N["3"]
  N --> O["5"]
  O --> P["6"]
  P --> Q["13"]
  Q --> R["12"]
  R --> S["14"]
  S --> T["15"]
  U["16"] --> V["7"]
  V --> W["4"]
  W --> X["15"]
  X --> Y["16"]
  end
```
</details>

为了插入 11，还需要进行一次单旋转，对于其后的 10 的插入也需要这样的旋转。不过插入 8 不用进行旋转，这样就建立了一棵近乎理想的平衡树。

![](../../raw/pages_0129-0160/images/page_136_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["7"] --> B["4"]
  A --> C["13"]
  B --> D["2"]
  B --> E["6"]
  B --> F["11"]
  C --> G["15"]
  C --> H["10"]
  C --> I["12"]
  C --> J["14"]
  C --> K["16"]
  D --> L["1"]
  D --> M["3"]
  D --> N["5"]
  E --> O["8"]
```
</details>

---

124

数据结构与算法分析——C++语言描述(第四版)

最后，我们插入9以演示双旋转的对称情形。注意，9引起含有10的节点产生不平衡。由于9在10和8之间(8在10通向9的路径上是节点10的儿子)，因此需要进行一个双旋转，我们得到下面的树:

![](../../raw/pages_0129-0160/images/page_137_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["7"] --> B["4"]
  A --> C["13"]
  B --> D["2"]
  B --> E["6"]
  C --> F["15"]
  C --> G["11"]
  C --> H["12"]
  C --> I["14"]
  C --> J["16"]
  D --> K["1"]
  D --> L["3"]
  D --> M["5"]
  E --> N["9"]
  F --> O["8"]
  G --> P["10"]
  H --> Q["11"]
  I --> R["12"]
  J --> S["13"]
  K --> T["之后"]
  L --> T
  M --> T
  N --> U["8"]
  P --> V["10"]
```
</details>

现在让我们对上面的讨论做个总结。除几种情形外，编程的细节是相当简单的。为将项是 $X$ 的一个新节点插入到一棵 AVL 树 $T$ 中, 我们递归地将 $X$ 插入到 $T$ 的相应的子树 (称为 $T_{\mathrm{LR}}$) 中。如果 $T_{\mathrm{LR}}$ 的高度不变, 那么插入完成。否则, 如果在 $T$ 中出现高度不平衡, 那么根据 $X$ 以及 $T$ 和 $T_{\mathrm{LR}}$ 中的项做适当的单旋转或双旋转, 更新这些高度 (并解决好与树的其余部分的链接), 从而完成插入。由于一次旋转总能足以解决问题, 因此, 仔细地编写非递归的程序一般说来要比编写递归程序快, 但对于现代编译器, 这种差别不像过去那么显著。但是, 要想把非递归程序编写正确是相当困难的, 而简便的递归实现却简单易读。

另一个效率问题涉及到高度信息的存储。由于真正需要的实际上就是子树高度的差，应该保证它很小。如果我们真的尝试这一点，则可用两个二进制位(代表+1,0,-1)表示这个差。这么做将避免平衡因子的重复计算，但是却丧失了某些简明性。最后的程序多多少少要比在每一个节点存储高度复杂。如果编写递归程序，那么速度恐怕不是主要考虑的问题。此时，通过存储平衡因子所得到的些微速度优势很难抵消清晰性和相对简明性的损失。不仅如此，由于大部分机器存储的最小单位是8个二进制位，因此所用的空间量不可能有任何差别。一个8位(带符号)的char将使我们存储高达127的绝对高度。既然树是平衡的，当然也就不可想象这会少到不够用(见练习)。

有了上面的讨论，现在准备编写 AVL 树的一些例程。不过，这里我们只想做一部分工作，其余的在线提供。首先，我们需要 AvlNode 类，它在图 4.40 中给出。我们还需要一个快速的函数来返回节点的高度，这个函数必须处理 nullptr 指针的恼人情形。该例程在图 4.41 中给出。基本的插入例程(见图 4.42)只在最后添加了一行，调用一个平衡方法。这个平衡方法在需要时用到单旋转或双旋转，更新高度，并返回所得到的树。

对于图 4.43 中的那些树，函数 rotateWithLeftChild 把左边的树变成右边的树，并返回指向新根的指针。函数 routateWithRightChild 是对称的，程序如图 4.44 所示。

类似地，图4.45中描述的双旋转可以通过图4.46所示的代码来实现。

---

第4章 树

125

```cpp
struct AvlNode
{
    Comparable element;
    AvlNode *left;
    AvlNode *right;
    int height;

    AvlNode( const Comparable & ele, AvlNode *lt, AvlNode *rt, int h = 0 )
    : element{ ele }, left{ lt }, right{ rt }, height{ h } { }

    AvlNode( Comparable && ele, AvlNode *lt, AvlNode *rt, int h = 0 )
    : element{ std::move( ele ) }, left{ lt }, right{ rt }, height{ h } { }
};
```

图 4.40 AVL 树的节点声明

```c
/**
 * 返回节点t的高度，如果是nullptr则返回-1.
 */
int height( AvlNode *t ) const
{
    return t == nullptr ? -1 : t->height;
}
```

图 4.41 计算 AVL 节点的高度的方法

```c
/**
 * 向一棵子树进行插入的内部方法.
 * x 是要插入的项.
 * t 为该子树的根节点.
 * 设置子树的新根.
 */
void insert( const Comparable & x, AvlNode * & t )
{
    if( t == nullptr )
        t = new AvlNode{ x, nullptr, nullptr };
    else if( x < t->element )
        insert( x, t->left );
    else if( t->element < x )
        insert( x, t->right );

    balance( t );
}

static const int ALLOWED_IMBALANCE = 1;

// 假设t是平衡的，或与平衡相差不超过1
void balance( AvlNode * & t )
{
    if( t == nullptr )
        return;
```

图 4.42 向 AVL 树进行插入的例程

---

126

数据结构与算法分析——C++语言描述(第四版)

```c
if( height( t->left ) - height( t->right ) > ALLOWED_IMBALANCE )
    if( height( t->left->left ) >= height( t->left->right ) )
        rotateWithLeftChild( t );
    else
        doubleWithLeftChild( t );
else
if( height( t->right ) - height( t->left ) > ALLOWED_IMBALANCE )
    if( height( t->right->right ) >= height( t->right->left ) )
        rotateWithRightChild( t );
    else
        doubleWithRightChild( t );

t->height = max( height( t->left ), height( t->right ) ) + 1;
}
```

图 4.42(续) 向 AVL 树进行插入的例程

![](../../raw/pages_0129-0160/images/page_139_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["k1"] --> B["k2"]
  A --> C["X"]
  A --> D["Y"]
  A --> E["Z"]
  B --> F["k1"]
  B --> G["k2"]
  C --> F
  C --> G
  D --> F
  D --> G
  E --> F
  E --> G
```
</details>

图4.43 单旋转

```c
/**
 * 用左儿子旋转二叉树的节点.
 * 这是对 AVL 树在情形1的一次单旋转.
 * 更新高度，然后设置新根.
 */
void rotateWithLeftChild( AvlNode * & k2 )
{
    AvlNode *k1 = k2->left;
    k2->left = k1->right;
    k1->right = k2;
    k2->height = max( height( k2->left ), height( k2->right ) ) + 1;
    k1->height = max( height( k1->left ), k2->height ) + 1;
    k2 = k1;
}
```

图 4.44 执行单旋转的例程

![](../../raw/pages_0129-0160/images/page_139_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> B["k1"]
  B --> C["k2"]
  C --> D["k3"]
  E["D"] --> F["k1"]
  G["B"] --> H["k2"]
  I["C"] --> J["k3"]
  K["A"] --> L["k1"]
  M["B"] --> N["k2"]
  O["C"] --> P["k3"]
  Q["D"] --> R["k1"]
  S["A"] --> T["k1"]
  U["B"] --> V["k2"]
  W["C"] --> X["k3"]
  Y["D"] --> Z["k1"]
  AA["A"] --> AB["k1"]
  AC["B"] --> AD["k2"]
  AE["C"] --> AF["k3"]
  AG["D"] --> AH["k1"]
  AI["A"] --> AJ["k2"]
  AK["B"] --> AL["k3"]
  AM["C"] --> AN["k1"]
  AO["D"] --> AP["k2"]
  AQ["A"] --> AR["k3"]
  AS["B"] --> AT["k1"]
  AU["C"] --> AV["k2"]
  AW["D"] --> AX["k3"]
  AZ["A"] --> BA["k1"]
  BA --> BC["k2"]
  BD["C"] --> BE["k3"]
  BF["D"] --> BG["k1"]
  BH["A"] --> BI["k2"]
  BJ["B"] --> BK["k3"]
  BL["C"] --> BM["k1"]
  BN["D"] --> BO["k2"]
  BP["A"] --> BR["k3"]
  BR --> BC
  BD["B"] --> BD
  BE["C"] --> BF
  BF --> BG
  BH["A"] --> BH
  BI["B"] --> BI
  BK["C"] --> BK
  BM["D"] --> BM
  BN["A"] --> BN
  BI["B"] --> BI
  BK["C"] --> BK
  BM["D"] --> BM
  BN["A"] --> BN
  BI["B"] --> BI
  BK["C"] --> BK
  BM["D"] --> BM
  BN["A"] --> BN
  BI["B"] --> BI
  BK["C"] --> BK
  BM["D"] --> BM
  BN["A"] --> BN
  BI2["BI“”"] --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
  BI" --> BI
    B -.-> F
    C -.-> F
    D -.-> F
    E -.-> F
    F -.-> G
    G -.-> H
    H -.-> I
    J -.-> I
    K -.-> L
    L -.-> M
    M -.-> N
    O -.-> N
    P -.-> Q
    Q -.-> R
    S -.-> S
    T -.-> T
    U -.-> U
    V -.-> V
    W -.-> W
    X -.-> X
    Y -.-> Y
```
</details>

图 4.45 双旋转

由于在二叉查找树中进行删除多少要比插入复杂，因此可以假设，在 AVL 树中的删除也会更复杂。理想情形下，我们希望将图 4.26 中的删除例程能够通过将最后一行改为在调用 balance 方法之后再返回而轻易地完成修改，这和前面对插入例程曾做过的修改是一样的。由

---

第4章 树

127

此得到图 4.47 的代码。它改善了删除的结果。一次删除能够造成树的一边变成比另一边浅了 2 层。具体的分析类似于由插入引起的不平衡，但又不完全一样。例如，图 4.34 中的情形 1，现在应该表达从树 Z 中进行一次删除（而不是向 X 进行一次插入），必须考虑树 Y 可能与树 X 具有同样深度的可能性。即使如此，仍然容易看到，旋转平衡了这种情形以及图 4.36 中的对称情形 4。于是，图 4.42 中第 28 行和第 34 行的平衡代码使用了 $> =$ 而不是 $>$，特别保证了在这些情形下使用单旋转而不是双旋转。我们把验证其余两种情形的工作留作练习。

```c
/**
 * 双旋转二叉树的节点: 首先左儿子和它的右儿子进行.
 * 然后节点k3和新的左儿子进行.
 * 这是对AVL树情形2的一次双旋转.
 * 更新高度, 然后设置新根.
 */
void doubleWithLeftChild( AvlNode * & k3 )
{
    rotateRightChild( k3->left );
    rotateLeftChild( k3 );
}
```

图 4.46 执行双旋转的例程

```c
/**
 * 从子树实施删除的内部方法.
 * x 是要被删除的项.
 * t 为该子树的根节点.
 * 设置该子树的新根.
 */
void remove( const Comparable & x, AvlNode * & t )
{
    if( t == nullptr )
        return;  // 没发现要删除的项；什么也不做

    if( x < t->element )
        remove( x, t->left );
    else if( t->element < x )
        remove( x, t->right );
    else if( t->left != nullptr && t->right != nullptr ) // 两个儿子
    {
        t->element = findMin( t->right )->element;
        remove( t->element, t->right );
    }
    else
    {
        AvlNode *oldNode = t;
        t = ( t->left != nullptr ) ? t->left : t->right;
        delete oldNode;
    }

    balance( t );
}
```

图 4.47 AVL 树中的删除例程

---

128

数据结构与算法分析——C++语言描述(第四版)

## 4.5 伸展树

现在描述一种相对简单的数据结构，叫作伸展树(splay tree)，它保证从空树开始任意连续 $M$ 次对树的操作最多花费 $O(M \log N)$ 时间。不过这种保证并不排除任意单次操作花费 $\Theta(N)$ 时间的可能，而且这样的界也不如每次操作最坏情形的界为 $O(\log N)$ 那么强，但实际效果却是一样的:不存在坏的输入序列。一般说来，当 $M$ 次的操作序列总的最坏情形运行时间为 $O(Mf(N))$ 时，我们就说它的摊还运行时间(amortized running time)为 $O(f(N))$ 。因此，一棵伸展树每次操作的摊还代价是 $O(\log N)$ 。经过长系列的操作，有的操作可能花费时间多一些，有的可能要少一些。

伸展树是基于这样的事实:对于二叉查找树来说，每次操作最坏情形时间 $O(N)$ 并不坏，只要它相对不常发生就行。任何一次访问，即使花费 $\Theta (N)$，仍然可能非常快。二叉查找树的问题在于，虽然一系列访问整体都是坏的操作有可能发生，但是很罕见。此时，累积的运行时间很重要。具有最坏情形运行时间 $O(N)$ 但保证对任意 $M$ 次连续操作最多花费 $O(M\log N)$ 运行时间的查找树数据结构确实可以满意了，因为不存在坏的操作序列。

如果任意特定操作可以有最坏时间界 $O(N)$, 而我们仍然想要一个 $O(\log N)$ 的摊还时间界, 那么很清楚, 只要一个节点被访问, 它就必须被移动。否则, 一旦发现一个深层的节点, 我们就有可能不断对它进行访问。如果这个节点不改变位置, 而每次访问又花费 $\Theta(N)$, 那么 $M$ 次访问就要花费 $\Theta(M \cdot N)$ 的时间。

伸展树的基本想法是，当一个节点被访问后，它就要经过一系列 AVL 树旋转向根推进。注意，如果一个节点很深，那么在其路径上就存在许多的节点也相对较深，通过重新构造可以使对所有这些节点的进一步访问所花费的时间变少。因此，如果节点过深，那么我们要求这种重新构造应具有平衡这棵树(到某种程度)的副作用。除在理论上给出好的时间界外，这种方法还可能有实际的效用，因为在许多应用中，若一个节点被访问，它就很可能不久再被访问。研究表明，这种情况的发生比人们预料的要频繁得多。另外，伸展树还不要求保留高度或平衡信息，因此它在某种程度上节省空间并简化代码(特别是当实现例程经过审慎考虑而被写出的时候)。

## 4.5.1 一个简单的想法(不能直接使用)

实施上面描述的重新构造的一种方法是执行单旋转，从底向上进行。这意味着我们将在访问路径上的每一个节点和它们的父节点实施旋转。作为例子，考虑在下面的树中对 $k_{1}$ 进行一次访问(一次find)之后所发生的情况。

![](../../raw/pages_0129-0160/images/page_141_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> k2["k2"]
  k2 --> k3["k3"]
  k3 --> k4["k4"]
  k4 --> k5["k5"]
  k1["k1"] --> k1
  k1 --> B["B"]
  k1 --> C["C"]
  k3 -.-> D["D"]
  k4 -.-> E["E"]
  k5 -.-> F["F"]
```
</details>

---

第4章 树

129

虚线是访问的路径。首先，我们在 $k_{1}$ 和它的父节点之间实施一次单旋转，得到下面的树:

![](../../raw/pages_0129-0160/images/page_142_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  k2["k2"] --> k1["k1"]
  k1 --> k3["k3"]
  k3 --> k4["k4"]
  k4 --> k5["k5"]
  k5 --> F["F"]
  k2 --> A["A"]
  k2 --> B["B"]
  k1 -.-> D["D"]
  k3 -.-> E["E"]
```
</details>

然后，在 $k_{1}$ 和 $k_{3}$ 之间执行旋转，得到下一棵树:

![](../../raw/pages_0129-0160/images/page_142_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  k1["k1"] --> k2["k2"]
  k2 --> A["A"]
  k2 --> B["B"]
  k2 --> k3["k3"]
  k3 --> C["C"]
  k3 --> D["D"]
  k4["k4"] -.-> k5["k5"]
  k5 --> F["F"]
```
</details>

此后，再实行两次旋转直到 $k_{1}$ 到达树根:

![](../../raw/pages_0129-0160/images/page_142_image_7.jpg)

这些旋转的效果是将 $k_{1}$ 一直推向树根，使得对 $k_{1}$ 的进一步访问很容易(暂时的)。不足的是，它把另外一个节点 $(k_{3})$ 几乎推向和 $k_{1}$ 以前那么深。而对那个节点的访问又将把另外的节点向深处推进，如此等等。虽然这个策略使得对 $k_{1}$ 的访问花费时间减少，但是它并没有明显地改善(原始)访问路径上其他节点的状况。事实上可以证明，使用这种策略将会存在一系列$M$ 个操作共需要 $\Omega (M\cdot N)$ 的时间，因此这个想法还不够好。说明这个问题最简单的方法是考

---

130

数据结构与算法分析——C++语言描述(第四版)

虑向初始的空树插入关键字 1,2,3,…,N 所形成的树(请将这个例子算出)。由此得到一棵树，这棵树只由一些左儿子构成。由于建立这棵树总共花费时间为 O(N)，因此这未必就有多坏。问题在于访问关键字为 1 的节点花费 N 个单元的时间，其中在访问路径上的每个节点则按 1 个时间单元计。在这些旋转完成以后，对关键字为 2 的节点的一次访问花费 N 个单元的时间，对关键字为 3 的节点的访问花费 N-1 个单元的时间，等等。依序访问所有关键字的总时间是 $N+\sum_{i=2}^{N}i=\Omega(N^{2})$ 。在它们都被访问以后，该树转变回原始状态，而且我们可能重复这个访问顺序。

## 4.5.2 展开

展开(splaying)的思路类似于上面介绍的旋转的想法，不过在旋转如何实施上我们稍微有些选择的余地。我们仍然从底部向上沿着访问路径旋转。令 $X$ 是在访问路径上的一个(非根)节点，我们将在这个节点上实施旋转操作。如果 $X$ 的父节点是树的根，那么只要旋转 $X$ 和根即可。这就是沿着访问路径上的最后的旋转。否则，$X$ 就有父亲 $(P)$ 和祖父 $(G)$，于是存在两种情况外加对称的情形要考虑。第一种情况是之字形情形(zig-zag case)(见图4.48)。这里，$X$ 是右儿子，$P$ 是左儿子(反之亦然)。如果是这种情况，那么执行一次就像AVL双旋转那样的双旋转。否则，出现另一种情形即一字形情形(zig-zig case): $X$ 和 $P$ 都是左儿子(或者其对称的情形，都是右儿子)。在这种情况下，我们把图4.49左边的树变换成右边的树。

![](../../raw/pages_0129-0160/images/page_143_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> B["P"]
  B --> C["G"]
  D["D"] --> E["X"]
  F["B"] --> G["C"]
  E --> H["P"]
  H --> I["X"]
  J["C"] --> K["G"]
  L["D"] --> M["G"]
```
</details>

图 4.48 之字形情形

![](../../raw/pages_0129-0160/images/page_143_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["X"] --> P["P"]
  P --> G["G"]
  G --> D["D"]
  A --> X["X"]
  X --> P
  P --> G
  G --> A
  G --> B
  G --> C
  G --> D
```
</details>

图4.49 一字形情形

作为例子，考虑最后的例子中的树，对 $k_{1}$ 执行一次 contains:

![](../../raw/pages_0129-0160/images/page_143_image_10.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> k2["k2"]
  k2 --> k3["k3"]
  k3 --> k4["k4"]
  k4 --> k5["k5"]
  k3 -.-> k1["k1"]
  k1 --> B["B"]
  k1 --> C["C"]
  k4 -.-> E["E"]
  k5 -.-> F["F"]
```
</details>

---

第4章 树

131

展开的第一步是在 $k_{1}$，显然这是一个之字形，因此我们用 $k_{1}, k_{2}$ 和 $k_{3}$ 执行一次标准的 AVL 双旋转，得到如下的树:

![](../../raw/pages_0129-0160/images/page_144_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  k1["k1"] --> k2["k2"]
  k2 --> A["A"]
  k2 --> B["B"]
  k2 --> C["C"]
  k2 --> D["D"]
  k3["k3"] --> E["E"]
  k3 --> F["F"]
  k4["k4"] -.-> F
  k5["k5"] --> F
```
</details>

在 $k_{1}$ 的下一步展开是一个一字形，因此我们用 $k_{1}, k_{4}$ 和 $k_{5}$ 做一字形旋转，得到最后的树:

![](../../raw/pages_0129-0160/images/page_144_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  k1["k1"] --> k2["k2"]
  k2 --> A["A"]
  k2 --> B["B"]
  k2 --> k3["k3"]
  k3 --> C["C"]
  k3 --> D["D"]
  k4["k4"] --> k5["k5"]
  k5 --> E["E"]
  k5 --> F["F"]
```
</details>

虽然从小的例子很难看出来，但是展开操作不仅将访问的节点移动到根处，而且还有把访问路径上的大部分节点的深度大致减少一半的效果(某些浅的节点最多向下推后两层)。

为了看出展开与简单旋转的差别，再来考虑将 $1, 2, 3, \dots, N$ 各项插入到初始空树中去的效果。如前所述可知共花费 $O(N)$ 时间，并产生与一些简单旋转结果相同的树。图4.50指出在项为1的节点展开的结果。区别在于，在对项为1的节点访问(花费 $N$ 个单元的时间)之后，对项为2的节点的访问只花费 $N/2$ 个时间单元而不是 $N$ 个时间单元，不存在像以前那么深层的节点。

![](../../raw/pages_0129-0160/images/page_144_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] --> B["2"]
  B --> C["3"]
  C --> D["4"]
  D --> E["5"]
  E --> F["6"]
  F --> G["7"]
  H["1"] --> I["2"]
  I --> J["3"]
  K["5"] --> L["6"]
  L --> M["7"]
  N["1"] --> O["2"]
  O --> P["3"]
  Q["4"] --> R["5"]
  R --> S["6"]
  T["1"] --> U["2"]
  U --> V["3"]
  W["6"] --> X["7"]
  Y["1"] --> Z["2"]
  Z --> AA["3"]
  AB["4"] --> AC["5"]
  AC --> AD["6"]
  AE["7"] --> AF["8"]
```
</details>

图4.50 在节点1展开的结果

对项为 2 的节点的访问将把诸节点带到距根 N/4 的深度之内，并且如此进行下去直到深度大约为  $\log N(N=7$  的例子太小，不能很好地看清这种效果）。图 4.51～图 4.59 显示在 32 个节点的树中访问项 1～9 的结果，这棵树最初只含有左儿子。我们从伸展树得不到在简单旋转策略中常见的那种低效率的坏现象。（实际上，这个例子只是一种非常好的情况。有一个相当复杂的证明指出，对于这个例子，N 次访问共耗费  $O(N)$  的时间。）

这些图着重强调了伸展树基本和关键的性质。当访问路径长而导致长于正常查找时间的时候，这些旋转将对未来的操作有益。当访问耗时很少的时候，这些旋转则不那么有益甚至有害。极端的情形是经过若干插入而形成的初始树。所有的插入都是花费常数时间的操作，

---

132

数据结构与算法分析——C++语言描述(第四版)

它们导致坏的初始树形成。此时，我们会得到一棵很差的树，但是运行却比预计的快，从而总的较少运行时间补偿了损失。这样，少数真正麻烦的访问却留给我们一棵几乎是平衡的树，其代价是必须返还某些已经省下的时间。在第11章将证明的主要定理指出，平均每个操作决不会落后 $O(\log N)$ 这个时间:我们总是遵守这个时间，即使偶尔有些坏的操作。

![](../../raw/pages_0129-0160/images/page_145_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 32["32"]
  2["2"] --> 4["4"]
  3["3"] --> 5["5"]
  4["6"] --> 7["7"]
  6["8"] --> 9["9"]
  7["9"] --> 10["10"]
  8["11"] --> 11["11"]
  9["11"] --> 12["12"]
  10["13"] --> 13["13"]
  11["13"] --> 14["14"]
  12["15"] --> 15["15"]
  13["15"] --> 16["16"]
  14["17"] --> 17["17"]
  15["17"] --> 18["18"]
  16["18"] --> 19["19"]
  17["19"] --> 20["20"]
  18["20"] --> 21["21"]
  19["21"] --> 22["22"]
  20["22"] --> 23["23"]
  21["23"] --> 24["24"]
  22["24"] --> 25["25"]
  23["25"] --> 26["26"]
  24["26"] --> 27["27"]
  25["27"] --> 28["28"]
  26["28"] --> 29["29"]
  27["29"] --> 30["30"]
  28["30"] --> 31["31"]
  29["31"] --> n30["30"]
  30["30"] --> n31["31"]
```
</details>

图4.51 一棵均为左儿子的树在节点1展开的结果

![](../../raw/pages_0129-0160/images/page_145_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 32["32"]
  4["3"] --> 4["4"]
  6["5"] --> 6["6"]
  7["7"] --> 7["7"]
  8["8"] --> 8["8"]
  10["9"] --> 10["10"]
  11["11"] --> 11["11"]
  12["12"] --> 12["12"]
  13["13"] --> 13["13"]
  14["14"] --> 14["14"]
  15["15"] --> 15["15"]
  16["16"] --> 16["16"]
  17["17"] --> 17["17"]
  18["18"] --> 18["18"]
  19["19"] --> 19["19"]
  20["20"] --> 20["20"]
  21["21"] --> 21["21"]
  22["22"] --> 22["22"]
  23["23"] --> 23["23"]
  24["24"] --> 24["24"]
  25["25"] --> 25["25"]
  26["26"] --> 26["26"]
  27["27"] --> 27["27"]
  28["28"] --> 28["28"]
  29["29"] --> 29["29"]
  30["30"] --> 30["30"]
  31["31"] --> 31["31"]
```
</details>

图4.52 将前面的树在节点2展开的结果

![](../../raw/pages_0129-0160/images/page_145_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 3["3"]
  2["2"] --> n3["3"]
  n3 --> 28["28"]
  n3 --> 32["32"]
  4["4"] --> 12["12"]
  n4["4"] --> 8["8"]
  n4 --> 6["6"]
  n4 --> 5["5"]
  n4 --> 7["7"]
  n4 --> 9["9"]
  n4 --> 10["10"]
  n4 --> 11["11"]
  n12["12"] --> 20["20"]
  n12 --> 16["16"]
  n12 --> 14["14"]
  n12 --> 13["13"]
  n16["16"] --> 24["24"]
  n16 --> 18["18"]
  n16 --> 15["15"]
  n16 --> 17["17"]
  n16 --> 19["19"]
  n20["20"] --> 22["22"]
  n20 --> 24["24"]
  n20 --> 26["26"]
  n20 --> 21["21"]
  n22["22"] --> 25["25"]
  n22 --> 23["23"]
  n26["26"] --> 27["27"]
  30["30"] --> n32["32"]
  n30["30"] --> 29["29"]
  n30 --> 31["31"]
```
</details>

图4.53 将前面的树在节点3展开的结果

---

第4章 树

133

![](../../raw/pages_0129-0160/images/page_146_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 4["4"]
  2["2"] --> 3["3"]
  n3["3"] --> n4["4"]
  n4 --> 28["28"]
  n4 --> 32["32"]
  n28["28"] --> 30["30"]
  n28 --> 29["29"]
  n30["30"] --> 31["31"]
  12["12"] --> 8["8"]
  n12["12"] --> 20["20"]
  n8["8"] --> 6["6"]
  n8 --> 10["10"]
  n8 --> 5["5"]
  n8 --> 7["7"]
  n8 --> 9["9"]
  n8 --> 11["11"]
  16["16"] --> 24["24"]
  n16["16"] --> 14["14"]
  n16 --> 18["18"]
  n16 --> 13["13"]
  n18["18"] --> 22["22"]
  n18 --> 15["15"]
  n18 --> 17["17"]
  n18 --> 19["19"]
  n24["24"] --> 26["26"]
  n24 --> 21["21"]
  n24 --> 23["23"]
  n26["26"] --> 25["25"]
  n26 --> 27["27"]
```
</details>

图4.54 将前面的树在节点4处展开的结果

![](../../raw/pages_0129-0160/images/page_146_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  n3["3"] --> 4["4"]
  n4["4"] --> 5["5"]
  n5["5"] --> 6["6"]
  n6["6"] --> 7["7"]
  n6 --> 8["8"]
  n7["7"] --> 9["9"]
  n8["8"] --> 10["10"]
  n9["9"] --> 11["11"]
  12["12"] --> 16["16"]
  n16["16"] --> 18["18"]
  n18["18"] --> 20["20"]
  n20["20"] --> 22["22"]
  n22["22"] --> 24["24"]
  n24["24"] --> 26["26"]
  n26["26"] --> 29["29"]
  28["28"] --> 30["30"]
  n30["30"] --> 32["32"]
  13["13"] --> 14["14"]
  15["15"] --> 16["16"]
  17["17"] --> 18["18"]
  19["19"] --> 20["20"]
  21["21"] --> 22["22"]
  23["23"] --> 24["24"]
  25["25"] --> 26["26"]
  27["27"] --> 29["29"]
  30["30"] --> 31["31"]
```
</details>

图 4.55 将前面的树在节点 5 处展开的结果

![](../../raw/pages_0129-0160/images/page_146_image_6.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  n3["3"] --> 4["4"]
  n4["4"] --> 5["5"]
  n5["5"] --> 6["6"]
  n6["6"] --> 7["7"]
  n7["7"] --> 8["8"]
  n8["8"] --> 9["9"]
  n8 --> 10["10"]
  n9["9"] --> 11["11"]
  12["12"] --> 13["13"]
  n13["13"] --> 14["14"]
  n14["14"] --> 15["15"]
  n15["15"] --> 16["16"]
  n16["16"] --> 17["17"]
  n17["17"] --> 18["18"]
  n18["18"] --> 19["19"]
  n19["19"] --> 20["20"]
  n20["20"] --> 21["21"]
  n21["21"] --> 22["22"]
  n22["22"] --> 23["23"]
  n23["23"] --> 24["24"]
  n24["24"] --> 25["25"]
  n25["25"] --> 26["26"]
  n26["26"] --> 27["27"]
  n27["27"] --> 28["28"]
  n28["28"] --> 29["29"]
  n29["29"] --> 30["30"]
  n30["30"] --> 31["31"]
  n31["31"] --> 32["32"]
```
</details>

图 4.56 将前面的树在节点 6 处展开的结果

![](../../raw/pages_0129-0160/images/page_146_image_8.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  n3["3"] --> 4["4"]
  n4["4"] --> 5["5"]
  n5["5"] --> 6["6"]
  n6["6"] --> 7["7"]
  n7["7"] --> 8["8"]
  n8["8"] --> 12["12"]
  9["9"] --> 10["10"]
  10["10"] --> 11["11"]
  n12["12"] --> 28["28"]
  n28["28"] --> 32["32"]
  13["13"] --> 14["14"]
  14["14"] --> 16["16"]
  15["15"] --> n16["16"]
  16["16"] --> 18["18"]
  17["17"] --> n18["18"]
  18["18"] --> 20["20"]
  20["20"] --> 24["24"]
  24["24"] --> 26["26"]
  26["26"] --> 29["29"]
  27["27"] --> 30["30"]
  29["30"] --> 31["31"]
  30["30"] --> n32["32"]
  31["32"] --> n32
```
</details>

图 4.57 将前面的树在节点 7 处展开的结果

![](../../raw/pages_0129-0160/images/page_146_image_10.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  n3["3"] --> 4["4"]
  n4["4"] --> 5["5"]
  n5["5"] --> 6["6"]
  n6["6"] --> 7["7"]
  n7["7"] --> 8["8"]
  n8["8"] --> 9["9"]
  n8 --> 10["10"]
  n8 --> 11["11"]
  n8 --> 12["12"]
  n12["12"] --> 20["20"]
  n20["20"] --> 21["21"]
  n20 --> 22["22"]
  n20 --> 23["23"]
  n20 --> 24["24"]
  n20 --> 25["25"]
  n20 --> 26["26"]
  n20 --> 27["27"]
  n20 --> 30["30"]
  n20 --> 31["31"]
  28["28"] --> 32["32"]
  n32["32"] --> n30["30"]
  n30 --> n31["31"]
```
</details>

图 4.58 将前面的树在节点 8 处展开的结果

---

134

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0129-0160/images/page_147_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  n3["3"] --> 4["4"]
  n4["4"] --> 5["5"]
  n5["5"] --> 6["6"]
  n6["6"] --> 7["7"]
  n7["7"] --> 8["8"]
  n8["8"] --> 9["9"]
  n9["9"] --> 10["10"]
  n10["10"] --> 11["11"]
  n11["11"] --> 12["12"]
  n12["12"] --> 28["28"]
  n28["28"] --> 32["32"]
  n32["32"] --> 30["30"]
  n30["30"] --> 29["29"]
  n29["29"] --> 31["31"]
  20["20"] --> 16["16"]
  n20["20"] --> 24["24"]
  n20 --> 18["18"]
  n16["16"] --> 14["14"]
  n16 --> 13["13"]
  n18["18"] --> 17["17"]
  n18 --> 19["19"]
  n24["24"] --> 22["22"]
  n24 --> 23["23"]
  n26["26"] --> 25["25"]
  n26 --> 27["27"]
```
</details>

图 4.59 将前面的树在节点 9 处展开的结果

可以通过访问要被删除的节点执行删除的操作。这种操作将节点上推到根处。如果删除该节点，则得到两棵子树 $T_{L}$ 和 $T_{R}$ （左子树和右子树）。如果找到 $T_{L}$ 中的最大的元素(这很容易)，那么这个元素就被旋转到 $T_{L}$ 的根下，此时 $T_{L}$ 将有一个没有右儿子的根。我们可以使 $T_{R}$ 为右儿子从而结束删除。

对伸展树的分析很困难，因为必须要考虑树的经常变化的结构。另一方面，伸展树的编程要比大部分平衡查找树简单得多，这是因为要考虑的情形少并且没有平衡信息需要保留。一些实际经验指出，在实践中它可以转化成更快的程序代码，不过这种状况离完善还很远。最后，我们指出，伸展树有几种变化，它们在实践中甚至运行得更好。有一种变化在第12章中已被完全编成程序。

## 4.6 树的遍历

由于二叉查找树中对信息进行了排序, 因此按照排序的顺序列出所有的项很简单, 图 4.60 中的递归函数进行的就是这项工作。

```cpp
/**
 * 按排序顺序打印树的内容.
 */
void printTree( ostream & out = cout ) const
{
    if( isEmpty( ) )
        out << "Empty tree" << endl;
    else
        printTree( root, out );
}

/**
 * 以排序顺序打印根在 t 处的子树的内部方法.
 */
void printTree( BinaryNode *t, ostream & out ) const
{
    if( t != nullptr )
    {
        printTree( t->left, out );
        out << t->element << endl;
        printTree( t->right, out );
    }
}
```

图 4.60 按顺序打印二叉查找树的例程

---

第4章 树

135

毫无疑问，这个函数能够解决将各项排序列出的问题。正如我们前面看到的，这类例程当用于树的时候则称为中序遍历(inorder traversal)(由于它依序列出各项，因此是有意义的)。中序遍历的一般方法是首先处理左子树，然后处理当前的节点，最后处理右子树。这个算法的有趣部分除了它的简单性之外，还在于其总的运行时间是 $O(N)$ 。这是因为在树的每一个节点处进行的工作是常数时间的。每一个节点均被访问一次，而在每一个节点进行的工作是:检测是否 nullptr、建立两个函数调用并执行一个输出语句。由于在每个节点的工作花费常数时间而总共有 $N$ 个节点，因此运行时间为 $O(N)$ 。

有时需要先处理两棵子树然后才能处理当前节点。例如，为了计算一个节点的高度，首先需要知道它的子树的高度。图4.61中的程序就是这样计算高度的。由于检验一些特殊的情况总是有益的——当涉及递归时尤其如此，因此要注意这个例程将声明树叶的高度为零，这是正确的。这种一般的遍历顺序叫作后序遍历(postorder traversal)，我们在前面也见到过。因为在每个节点的工作花费常数时间，所以总的运行时间也是 $O(N)$ 。

```c
/**
 * 计算根在t处子树的高度的内部方法.
 */
int height( BinaryNode *t )
{
    if( t == nullptr )
        return -1;
    else
        return 1 + max( height( t->left ), height( t->right ) );
}
```

图4.61 使用后序遍历计算树的高度的例程

我们见过的第三种常用的遍历方案为先序遍历(preorder traversal)。这里，当前节点是在其子节点之前处理。这种遍历是有用的，比如，如果要想用其深度标记每一个节点，那么就会用到这种遍历。

所有这些例程有一个共同的思路，那就是首先处理 nullptr 的情形，然后才是其余的工作。注意，此处缺少一些附加的变量。这些例程仅仅传递指向作为子树的根的节点的指针，并没有声明或是传递任何附加的变量。程序越紧凑，一些愚蠢的错误出现的可能就越小。第四种遍历不常使用，这种遍历叫作层序遍历 (level-order traversal)，我们尚未见到过。在层序遍历中，所有深度为 $d$ 的节点要在深度 $d+1$ 的节点之前进行处理。层序遍历与其他类型的遍历不同的地方在于它不是递归地实施的，它用到队列，而不使用递归所默认的栈。

## 4.7 B树

迄今为止，我们始终假设可以把整个数据结构存储到计算机的主存中。可是，如果数据太多主存装不下，那么就意味着必须把数据结构放到磁盘上。此时，因为大O模型不再适用，所以导致游戏规则发生了变化。

问题在于，大 O 分析假设所有的操作都是相等的。然而，现在这么假设就不合适了，特别是涉及到磁盘 I/O 时。现代计算机每秒执行数十亿条指令。这是相当快的，主要是因为速度很大程度上依赖于电的特性。另一方面，磁盘是机械运动装置，它的速度主要依赖于转动磁

---

136

数据结构与算法分析——C++语言描述(第四版)

盘和移动磁头的时间。许多磁盘以 7200RPM(Revolutions Per Minute)旋转。就是说，它 1 分钟转 7200 转。因此，1 转占用 1/120 秒，或即 8.3 毫秒。平均可以认为磁盘转到一半的时候发现我们要寻找的信息，但这可通过移动磁盘磁头的时间抵消，因此我们得到一次访问时间为 8.3 毫秒。(这是非常宽松的估计；9～11 毫秒的访问时间更为普通。)因此，我们每秒大约可以进行 120 次磁盘访问。若不和处理器的速度比较，那么这听起来还是相当不错的。可是考虑到处理器的速度，数十亿条指令却花费相当于 120 次磁盘访问的时间。当然，这里每一个数据都是粗略的计算，不过相对速度还是相当清楚的:磁盘访问的代价太高了。不仅如此，处理器的速度还在以比磁盘速度快得多的速度增长(增长相当快的是磁盘容量的大小)。因此，为了节省一次磁盘访问，我们愿意进行大量的计算。几乎在所有的情况下，控制运行时间的都是磁盘访问的次数。于是，如果把磁盘访问次数减少一半，那么运行时间也将减少一半。

在磁盘上，典型的查找树执行如下:设我们想要访问佛罗里达州公民的驾驶记录。假设我们有1000万项，每一个关键字是32字节(代表一个名字)，而一个记录是256字节。假设这些数据不能都装入主存，我们是正在系统上的20个用户中的一个(因此我们有1/20的资源)。这样，在1秒内，我们可以执行几百万次指令，或者执行6次磁盘访问。

不平衡的二叉查找树是一个灾难。在最坏情形下它有线性的深度，从而可能需要1000万次磁盘访问。平均来看，一次成功的查找可能需要 $1.38\log N$ 次磁盘访问，由于 $\log 10000000 \approx 24$ ，因此平均一次查找需要32次磁盘访问，或5秒的时间。在一棵典型的随机构造的树中，我们预料会有一些节点的深度要深3倍。它们需要大约100次磁盘访问，或16秒的时间。AVL树多少要好一些。 $1.44\log N$ 的最坏情形不可能发生，典型的情形是非常接近于 $\log N$ 。这样，一棵AVL树平均将使用大约25次磁盘访问，需要的时间是4秒。

我们想要把磁盘访问次数减小到一个非常小的常数，比如3次或4次；而且我们愿意写一个复杂的程序来做这件事，因为只要我们不无理到荒谬的地步，机器指令基本上是不占时间的。由于典型的AVL树接近到最优的高度，因此应该清楚的是，二叉查找树是不可行的。使用二叉查找树不可能低于 $\log N$ 。解法直觉上看是简单的:如果我们有更多的分支，那么就有更少的高度。这样，31个节点的理想二叉树(perfect binary tree)有5层，而31个节点的5叉树则只有3层，如图4.62所示。一棵 $M$ 叉查找树(M-ary search tree)可以有 $M$ 路分支。随着分支增加，树的深度在减少。一棵完全二叉树(complete binary tree)的高度大约为 $\log_2N$ ，而一棵完全 $M$ 叉树(complete M-ary tree)的高度大约是 $\log_M N$ 。

![](../../raw/pages_0129-0160/images/page_149_image_6.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Node 1"] --> B["Node 2"]
  B --> C["Node 3"]
  C --> D["Node 4"]
  D --> E["Node 5"]
  E --> F["Node 6"]
  F --> G["Node 7"]
```
</details>

图4.62 31个节点的5叉树只有3层

我们可以以与建立二叉查找树大致相同的方式建立 $M$ 叉查找树。在二叉查找树中，我们需要一个关键字来决定两个分支到底取用哪个分支；而在 $M$ 叉查找树中我们需要 $M - 1$ 个关键字来决定选取哪个分支。为使这种方案在最坏的情形下有效，我们需要保证 $M$ 叉查找树以某种方式得到平衡。否则，像二叉查找树，它可能退化成一个链表。实际上，我们甚至想要更具限制性的平衡条件。就是说，我们不想要 $M$ 叉查找树退化到甚至是二叉查找树，因为那样又将无法摆脱 $\log N$ 次访问了。

---

第4章 树

137

实现这种想法的一种方式是使用 B 树。这里描述基本的 B 树。 $^{①}$  已知还有许多的变种和改进，但实现起来多少要复杂些，因为有相当多的情形需要考虑。不过，容易看到，原则上 B 树保证只有少数的磁盘访问。

阶为 $M$ 的 $\mathbf{B}$ 树(B-tree)是一棵具有下列特性的 $M$ 叉树:②

1. 数据项存储在树叶上。
2. 非叶节点存储直到 M-1 个关键字以指示搜索的方向；关键字 i 代表子树  $i+1$  中的最小的关键字。
3. 树的根或者是一片树叶，或者其儿子数在 2 和 M 之间。
4. 除根外，所有非叶节点的儿子数在 $[M/2]$ 和 M 之间。
5. 所有的树叶都在相同的深度上，并且每片树叶拥有的数据项其个数在 $\lceil L / 2 \rceil$ 和 $L$ 之间，$L$ 的确定稍后描述。

图 4.63 给出了 5 阶 B 树的一个例子。注意, 所有的非叶节点的儿子数都在 3 和 5 之间 (从而有 2\~4 个关键字); 根可能只有两个儿子。这里, 我们让 $L = 5$ 。在这个例子中 $L$ 和 $M$ 恰好是相同的, 但这不是必须的。由于 $L$ 是 5 , 因此每片树叶有 3\~5 个数据项。要求节点一半满将保证 B 树不致退化成简单的二叉树。虽然存在改变该结构的各种 B 树的定义, 但大部分在一些次要的细节上变化, 而我们这个定义是流行形式中的一种。

![](../../raw/pages_0129-0160/images/page_150_image_11.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  Root["Top Node"] --> A["Left Branch"]
  Root --> B["Middle Branch"]
  Root --> C["Right Branch"]
  
  A --> A1["8"]
  A --> A2["18"]
  A --> A3["26"]
  A --> A4["35"]
  A --> A5["48"]
  A --> A6["51"]
  A --> A7["54"]
  A --> A8["72"]
  A --> A9["78"]
  A --> A10["83"]
  A --> A11["92"]
  
  B --> B1["48"]
  B --> B2["51"]
  B --> B3["54"]
  B --> B4["72"]
  B --> B5["78"]
  B --> B6["83"]
  B --> B7["92"]
  B --> B8["97"]
  
  C --> C1["66"]
  C --> C2["68"]
  C --> C3["72"]
  C --> C4["78"]
  C --> C5["83"]
  C --> C6["87"]
  C --> C7["92"]
  C --> C8["97"]
  
  D["Bottom Left Branch"] --> D1["2\n4\n6"]
  D --> D2["8\n10\n12\n14\n16"]
  D --> D3["18\n20\n22\n24"]
  D --> D4["26\n28\n30\n31\n32"]
  D --> D5["35\n36\n37\n38\n39"]
  D --> D6["41\n42\n44\n46"]
  D --> D7["48\n49\n50"]
  D --> D8["51\n52\n53"]
  D --> D9["54\n56\n58\n59"]
  D --> D10["66\n68\n69\n70"]
  D --> D11["72\n73\n74\n76"]
  D --> D12["78\n79\n81"]
  D --> D13["83\n84\n85"]
  
  E["Bottom Right Branch"] --> E1["87\n89\n90"]
  E --> E2["92\n93\n95"]
  E --> E3["97\n98\n99"]
```
</details>

图4.63 5阶B树

每个节点代表一个磁盘区块，于是我们根据所存储的项数的多少选择 $M$ 和 $L$ 。例如，设一个区块容纳8192字节。在上面的佛罗里达例子中，每个关键字使用32个字节。在一棵 $M$ 阶B树中，我们有 $M - 1$ 个关键字，总数为 $32M - 32$ 字节，再加上 $M$ 个分支。由于每个分支基本上都是另外的一些磁盘区块，因此可以假设一个分支是4个字节。这样，这些分支共用$4M$ 字节。一个非叶节点总的内存需求为 $36M - 32$ 字节。使得不超过8192字节的 $M$ 的最大值是228。因此，我们选择 $M = 228$ 。由于每个数据记录是256字节，因此我们能够把32个记录装入一个区块中。于是，我们选择 $L = 32$ 。这样就保证每片树叶有 $16\sim 32$ 个数据记录以及每个内部节点(除根外)至少以114种方式分叉。由于有1000万个记录，因此至多存在625000片树叶。由此得知，在最坏情形下树叶将在第4层上。更具体地说，最坏情形的访问次数近似地由 $\log_{M / 2}N$ 给出，这个数可以有1的误差(例如，根及其下一层可以存放在主存的高速缓存中，使得经过长时间运行后只需要对第3层或更深层进行磁盘访问)。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里所描述的是通常称为  $B^{+}$ 树的树。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 法则 3 和 5 对于前 L 次插入必须要放宽。</span></small>

---

138

数据结构与算法分析——C++语言描述(第四版)

剩下的问题是如何向 B 树添加项和从 B 树删除项的问题，下面将概述所涉及的想法。注意，许多重复的论题以前都曾见到过。

我们首先考查插入。设我们想要把 57 插入到图 4.63 的 B 树中。沿树向下查找揭示出它不在树中。此时我们把它作为第 5 项添加到树叶上。注意，我们可能要为此重新组织该树叶上的所有数据。然而，与磁盘访问相比(在这种情况下它还包含一次磁盘写入)，这么做的开销是可以忽略的。

当然，这次是相对简单的，因为该树叶还没有被装满。设现在我们想要插入55。图4.64显示了一个问题:55想要插入其中的那片树叶已经满了。解决方案并不复杂:由于我们现在有 $L + 1$ 项，因此把它们分成两片树叶，这两片树叶保证都有所需最小个数的记录。我们形成两片树叶，每叶3项。写这两片树叶需要两次磁盘访问，更新它们的父节点需要第3次磁盘访问。注意，在父节点中关键字和分支均发生了变化，但这种变化是以容易计算的受控方式处理的。最后得到的B树在图4.65中示出。虽然分裂节点是耗时的，因为它至少需要两次附加的磁盘写，但它相对很少发生。例如，如果 $L$ 是32，那么当节点被分裂时，具有16和17项的两片树叶分别被建立。对于有17项的那片树叶，我们可以再执行15次插入而不用另外的分裂。换句话说，对于每次分裂，大致存在 $L / 2$ 次非分裂的插入。

![](../../raw/pages_0129-0160/images/page_151_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Input Values"] --> B["Intermediate Step 1"]
  A --> C["Intermediate Step 2"]
  A --> D["Intermediate Step 3"]
  A --> E["Intermediate Step 4"]
  A --> F["Intermediate Step 5"]
```
</details>

图4.64 将57插入到图4.63的树中后的B树

![](../../raw/pages_0129-0160/images/page_151_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  Root["Top Node"] --> Branch1["Branch 1"]
  Root --> Branch2["Branch 2"]
  Root --> Branch3["Branch 3"]
  Branch1 --> Node1_8["8"]
  Branch1 --> Node1_18["18"]
  Branch1 --> Node1_26["26"]
  Branch1 --> Node1_35["35"]
  Branch2 --> Node2_4["2"]
  Branch2 --> Node2_8["8"]
  Branch2 --> Node2_10["10"]
  Branch2 --> Node2_12["12"]
  Branch2 --> Node2_14["14"]
  Branch2 --> Node2_16["16"]
  Branch3 --> Node3_4["48"]
  Branch3 --> Node3_51["51"]
  Branch3 --> Node3_54["54"]
  Branch3 --> Node3_57["57"]
  Branch4 --> Node4_42["42"]
  Branch4 --> Node4_49["49"]
  Branch4 --> Node4_50["50"]
  Branch4 --> Node4_51["51"]
  Branch4 --> Node4_52["52"]
  Branch4 --> Node4_53["53"]
  Branch4 --> Node4_54["54"]
  Branch4 --> Node4_55["55"]
  Branch4 --> Node4_56["56"]
  Branch4 --> Node4_57["57"]
  Branch4 --> Node4_58["58"]
  Branch4 --> Node4_59["59"]
  Branch5 --> Node5_72["72"]
  Branch5 --> Node5_78["78"]
  Branch5 --> Node5_83["83"]
  Branch5 --> Node5_66["66"]
  Branch5 --> Node5_68["68"]
  Branch5 --> Node5_69["69"]
  Branch5 --> Node5_70["70"]
  Branch5 --> Node5_72["72"]
  Branch5 --> Node5_73["73"]
  Branch5 --> Node5_74["74"]
  Branch5 --> Node5_76["76"]
  Branch5 --> Node5_78["78"]
  Branch5 --> Node5_79["79"]
  Branch5 --> Node5_81["81"]
  Branch5 --> Node5_83["83"]
  Branch5 --> Node5_84["84"]
  Branch5 --> Node5_85["85"]
  Branch6["Bottom Node"] --> Node6_92["92"]
  Branch6 --> Node6_97["97"]
  Branch6 --> Node6_98["98"]
  Branch6 --> Node6_99["99"]
```
</details>

图4.65 将55插入到图4.64的B树中导致分裂成两片树叶

前面例子中的节点分裂之所以行得通是因为其父节点的儿子个数尚未满员。可是，如果满员了又会怎样呢？例如，假设想要把40插入到图4.65的B树中，此时必须把包含关键字35～39而现在又要包含40的树叶分裂成两片树叶。但是这将使父节点有6个儿子，可是它只能有5个儿子。因此，解法就要分裂这个父节点。结果在图4.66中给出。当父节点被分裂时，我们必须更新那些关键字以及父节点的父亲的值，这样就招致额外的两次磁盘写（从而这次插入花费5次磁盘写）。然而，虽然由于有大量的情况要考虑而使得程序确实不那么简单，但这些关键字还是以完全受控的方式变化的。

---

第4章 树

139

![](../../raw/pages_0129-0160/images/page_152_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  Root["Top Node"] --> Branch1["Branch 1"]
  Root --> Branch2["Branch 2"]
  Root --> Branch3["Branch 3"]
  Root --> Branch4["Branch 4"]
  Root --> Branch5["Branch 5"]
```
</details>

图 4.66 把 40 插入到图 4.65 的 B 树中，这将引起树叶被分裂成两片，然后又造成父节点的分裂

正如这里的情形所示，当一个非叶节点分裂时，它的父节点得到了一个儿子。如果父节点的儿子个数已经达到规定的限度怎么办呢？在这种情况下，我们继续沿树向上分裂节点直到或者找到一个父节点它不需要再分裂，或者到达树根。如果分裂树根，那么就得到两个树根。显然这是不可接受的，但我们可以建立一个新的根，这个根以分裂得到的两个树根作为它的两个儿子。这就是为什么准许树根可以最少有两个儿子的特权的原因。这也是 B 树增加高度的唯一的方式。不用说，一路向上分裂直到根的情况是一种特别少见的异常事件，因为一棵具有 4 层的树意味着其根在整个插入序列中已经被分裂了 3 次(假设没有删除发生)。事实上，任何非叶节点的分裂也是相当少见的。

还有其他一些方法处理儿子过多的情况。一种方法是在相邻节点有空间时把一个儿子交给该邻节点领养。例如，为了把29插入到图4.66的B树中，可以把32移到下一片树叶而为29腾出一个空间。这种方法要求对父节点进行修改，因为有些关键字受到了影响。然而，它趋向于使得节点更满从而在长时间运行中节省空间。

我们可以通过查找需要被删除的项并在找到后删除它来执行删除操作。问题在于，如果被删元素所在的树叶的数据项数已经是最小值，那么删除后它的项数就低于最小值了。我们可以通过在相邻节点本身没有达到最小值时领养一个邻项来矫正这种状况。如果邻节点也已达到最小值，那么可以与相邻节点联合以形成一片满叶。可是，这意味着其父节点失去一个儿子。如果失去儿子的结果又引起父节点的儿子数低于最小值，那么我们使用相同的策略继续进行后面的工作。这个过程可以一直上行到根。根不可能只有一个儿子(要是允许根有一个儿子那可就不明智了)。如果这个领养过程的结果使得根只剩下一个儿子，那么删除该根并让它的这个儿子作为树的新根。这是 B 树降低高度的唯一方式。例如，假设我们想要从图 4.66 的 B 树中删除 99。由于那片树叶只有两项而它的邻居已经是最小值 3 项了，因此我们把这些项合并成有 5 项的一片新的树叶。结果，它们的父节点只有两个儿子了。不过，该父节点可以从它的邻节点领养，因为邻节点有 4 个儿子。领养的结果使得双方都有 3 个儿子，结果如图 4.67 所示。

![](../../raw/pages_0129-0160/images/page_152_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  Root["26 41 66 83"] --> Node1["8 18"]
  Root --> Node2["35 38"]
  Root --> Node3["48 51 54 57"]
  Root --> Node4["72 78"]
  Root --> Node5["87 92"]

  Node1 --> Left1["2 4 6\n8 10 12 14 16\n18 20 22 24"]

  Node2 --> Left2["26 28 30 31 32\n35 36 37\n38 39 40"]

  Node3 --> Left3["41 42 44 46\n48 49 50\n51 52 53\n54 55 56\n57 58 59"]

  Node4 --> Left4["66 68 69 70\n72 73 74 76\n78 79 81"]

  Node5 --> Right1["83 84 85\n87 89 90\n92 93 95 97 98"]
```
</details>

图 4.67 在从图 4.66 的 B 树中删除 99 后的 B 树

---

140

数据结构与算法分析——C++语言描述(第四版)

## 4.8 标准库中的容器 set 和 map

在第 3 章中讨论过的 STL 容器即 vector 和 list 用于查找时效率很低。因此，STL 提供了两个附加容器 set 和 map，它们能够保证对诸如插入、删除和查找等基本操作的对数开销。

## 4.8.1 集合容器 set

set 是一个不允许重复元的有序容器。用于访问 vector 和 list 的项的许多做法也对 set 适用。特别是，嵌套在 set 中的 iterator 和 const\_iterator 类型允许对 set 的遍历，而来自 vector 和 list 的几个方法在 set 中拥有相同的名称，包括 begin、end、zise 和 empty。在图 3.6 中描述的 print 函数模板如果传送一个 set 也将会正常工作。

由 set 所要求的一些特有的操作是一些插入、删除以及(有效地)执行基本查找的能力。

插入例程自然地被命名为 insert。然而，由于 set 不允许有重复元，因此 insert 就有可能招致插入失败。这样一来，我们就要使返回类型能够通过布尔变量指出这一点。可是，insert 拥有比布尔量更为复杂的返回类型。这是因为，insert 也返回一个 iterator，它代表当 insert 返回时项 x 所在的位置。这个 iterator 或者表示一个新插入的项，或者表示造成 insert 失败的已有的项，而且这样做很有必要，因为知道该项的位置使我们避免查找而直接达到包含该项的节点，从而能够更有效地删除它。

STL 定义了一个类模板叫作 pair, 比 struct 稍微复杂些, 它使用 first 成员和 second 成员来访问 pair 中对应的两项。下面是两个不同的 insert 例程:

```txt
pair<iterator,bool> insert( const Object & x );
pair<iterator,bool> insert( iterator hint, const Object & x );
```

单参数 insert 的行为上面做了描述。双参数 insert 有一个提示说明，指示项 x 应该插入的位置。如果提示准确，那么插入就迅速，常常是 $O(1)$ 时间。如果不准确，那么插入就用常规算法进行，执行起来与单参数 insert 类似。例如，下述代码使用双参数 insert 可能比单参数 insert 更快:

```txt
set<int> s;
for( int i = 0; i < 1000000; ++i )
    s.insert( s.end( ), i );

erase 有如下几个版本:
int erase( const Object & x );
iterator erase( iterator itr );
iterator erase( iterator start, iterator end );
```

第一个单参数 erase 删除 x(如果找到的话)，并且返回实际删除的项数，显然它不是 0 就是 1。第 2 个单参数 erase 的行为与 vector 和 list 中的一样，它删除由 iterator 给定位置上的对象，且返回一个 iterator，表示调用 erase 之前直接位于 itr 后面的元素，并使 itr 失效，不能再使用。双参数 erase 的行为与 vector 和 list 中的相同，删除所有从 start 开始的项，直到但不包括 end 处的项。

对于查找，set 不使用返回布尔变量的 contains 例程，而是提供一个 find 例程，它返回一个表示该项位置的 iterator(或在查找失败时返回终端标记)。这提供了更多的信息，而且不占用运行时间。find 的格式为

---

第4章 树

141

iterator find( const Object & x ) const;

默认情况下，排序用到 less&lt;Object&gt;函数对象，它本身通过为 Object 调用 operator<来实现。另一种排序可以通过实例化带有一个函数对象类型的 set 模板来指定。例如，我们可以创建一个存储 string 对象的 set，通过使用图 1.25 中编写的 CaseInsensitiveCompare 函数对象忽略大小写。在下面的代码中，sets 的大小为 1。

```txt
set<string,CaseInsensitiveCompare> s;
s.insert( "Hello" ); s.insert( "HeLLo" );
cout << "The size is: " << s.size( ) << endl;
```

## 4.8.2 映射容器 map

map 用来存储由关键字和它们的值构成的一些有序项的集合。关键字必须是唯一的，但多个关键字可能映射到一些相同的值。这样，值可不必唯一。map 中的关键字保持逻辑上的有序状态。

map 的行为就像是用 pair 实例化的 set，其比较函数只涉及到关键字。 $^{①}$  因此，它支持 begin、end、size 和 empty，但其基础迭代器是一个关键字-值对。换句话说，对于 iteratoritr，\*itr 为 pair&lt;KeyType,ValueType&gt;类型。map 还支持 insert、find 和 erase。对于 insert，我们必须提供一个 pair&lt;KeyType,ValueType&gt;对象。虽然 find 只要求一个关键字，但是它返回的 iterator 却引用一个 pair。只使用这些操作常常是不划算的，因为语法代价可能会很高昂。

所幸的是，map 有一个重要的附加操作，这个操作会带来简单的语法。对 map 来说，其数组索引运算符重载如下:

ValueType & operator[] ( const KeyType & key );

operator[]语义如下。如果在 map 中出现 key，那么对应值的引用就被返回。如果在 map 中 key 不出现，那么它就和一个默认值一起被插入到 map 中，然后返回所插入的默认值的引用。这个默认值通过应用零参数构造函数获得，对于一些基本类型它的值为零。语法不允许访问函数版本的 operator[]，因此 operator[] 不能用在常量的 map 上。例如，如果一个 map 通过常量引用传递，那么在例程内部 operator[] 是不可用的。

图 4.68 中的代码片段阐释访问 map 中的项的两种方法。首先，在第 3 行上左边调用 operator[]，如此，将"Pat"和 double 型的值 0 插入到 map 中，并返回对该 double 型量的引用。然后，赋值操作将 map 内的 double 型量改为 75000。第 4 行输出 75000。不过，第 5 行将"Jan"和工资 0.0 插入到 map 然后将其输出。这可能是应该要做的工作，也可能不是，它依赖于具体的应用。如果区分位于 map 中的项和不在 map 中的项很重要，或如果不 insert 到 map 中(因为它是不可改变的)很重要，那么可以使用在 7\~12 行上显示的另一种处理方法。这时我们看到对 find 的一次调用。如果没有找到关键字，那么 iterator 就是终端标记并可被测试到。如果找到关键字，那么就可以访问由 iterator 所引用的对偶中的第 2 项，该项即与所找到的关键字相关的值。如果 itr 是一个 iterator 对象而不是 const\_iterator 对象，那么也可以输出 itr->second。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 像 set 一样，一个可选的模板参数可以被用来指定不同于 less&lt;KeyType&gt; 的比较函数。</span></small>

---

142

数据结构与算法分析——C++语言描述(第四版)

```cpp
map<string,double> salaries;

salaries[ "Pat" ] = 75000.00;
cout << salaries[ "Pat" ] << endl;
cout << salaries[ "Jan" ] << endl;

map<string,double>::const_iterator itr;
itr = salaries.find( "Chris" );
if( itr == salaries.end( ) )
    cout << "Not an employee of this company!" << endl;
else
    cout << itr->second << endl;
```

图4.68 访问map中的值

## 4.8.3 set 和 map 的实现

C++要求 set 和 map 以对数最坏情形时间支持基本的 insert、erase 和 find 操作。因此，基础的实现方法就是平衡二叉查找树。一般说来，我们并不使用 AVL 树，而经常使用一些自顶向下的红黑树，它们将在 12.2 节讨论。

实现 set 和 map 的一个重要问题是提供对迭代器类的支持。当然，在内部，迭代器保留在迭代中指向 “当前” 节点的一个指针。困难的部分是高效地到下一个节点的推进。存在几种可能的解决方案，其中的一些方案列出如下:

1. 在构造迭代器时，让每个迭代器把包含 set 的项的数组作为该迭代器的数据存储。但这行不通:在修改 set 以后，高效地实现返回迭代器的任何例程都是不可能的，譬如某些版本的 erase 和 insert。
2. 让迭代器保留一个栈，存储通向当前节点的路径上的那些节点。根据该信息，我们可以推出迭代中的下一个节点，它或者是当前节点的包含最小项的右子树上的节点，或者包含其左子树当前节点的最近的祖先。这使得迭代器多少有些大，并使得迭代器的代码笨拙。
3. 让查找树中的每个节点除存储其子节点外还要存储它的父节点。此时迭代器不至于那么大，但是在每个节点上需要额外的内存，并且迭代的代码仍然笨拙。
4. 让每个节点保留两个附加的链:一个通向下一个更小的节点，另一个通向下一个更大的节点。这要占用空间，不过迭代执行起来非常简单，并且保留这些链也容易。
5. 只对那些具有 nullptr 左链或 nullptr 右链的节点保留附加的链，做法是通过使用附加的布尔变量让例程判断是一个左链正在被用作标准二叉查找树的左链，还是一个指向下一个更小节点的链，对右链的做法类似(练习 4.49)。这种做法叫作线索树(threaded tree)，并用于许多 STL 的实现中。

## 4.8.4 使用多个 map 的示例

许多单词都和另外一些单词相似。例如，通过改变第1个字母，单词wine可以变成dine、fine、line、mine、nine、pine或vine。通过改变第3个字母，wine可以变成wide、wife、wipe或wire，以及其他一些单词。通过改变第4个字母wine可以变成wind、wing、

---

第4章 树

143

wink 或 wins，以及其他一些单词。这样我们就得到 15 个不同的单词，它们仅仅通过改变 wine 中的一个字母而得到。实际上，存在 20 多个不同的单词，其中有些单词更生僻。我们想要编写一个程序来找出通过单个字母的替换可以变成至少 15 个其他的单词的单词。假设有一本词典，由大约 89 000 个各种长度的不同单词组成。大部分单词在 6 和 11 个字母之间。其中 6 字母单词有 8205 个，7 字母单词有 11 989 个，8 字母单词 13672 个，9 字母单词 13 014 个，10 字母单词 11 297 个，11 字母单词 8617 个。（实际上，一些最易互变的单词是 3 字母、4 字母和 5 字母单词，而更长的单词检查起来更耗费时间。）

最直接的策略是使用一个 map 对象，其中的关键字是单词，而相应的值是用单字母替换能够从关键字变换得到的一些单词组成的向量。图 4.69 中的例程显示最后得到的（我们必须写出这部分的代码）map 如何能够用来打印所要求的答案。该程序使用一个范围 for 循环 (range for loop) 遍历 map 并查验由一个单词和一列单词的 vector 组成的序偶。第 4 行和第 6 行上的常量引用用来代替复杂的表达式以及避免不必要的复制。

```txt
void printHighChangeables( const map<string,vector<string>> & adjacentWords,
                          int minWords = 15 )
{
    for( auto & entry : adjacentWords )
    {
        const vector<string> & words = entry.second;

        if( words.size( ) >= minWords )
        {
            cout << entry.first << " (" << words.size( ) << "):";
            for( auto & str : words )
                cout << " " << str;
            cout << endl;
        }
    }
}
```

图4.69 给定一个map，它包含一些单词作为关键字，和只在一个字母上彼此互异的一些单词的vector对象作为其值，输出那些具有minWords个或更多的通过单字母替换所得单词中的单词

主要的问题是如何从包含 89 000 个单词的数组构造 map 对象。图 4.70 中的例程是一个简单函数，测试除一个单字母替换外两个单词是否相等。我们可以使用该例程来提供最简单的 map 构造算法，它是所有单词对的蛮力测试。这个算法如图 4.71 所示。

如果发现一对单词只在一个字母上不同，则可在第 12 行和第 13 行上更新 map。在第 12 行我们使用的约定是，adjWords[str] 代表除一个字母外其余部分与 str 相同的单词的 vector。如果我们之前见过 str，那么它就在 map 中，而我们只需要把新的单词添加到 map 中的 vector 内，这项工作是通过调用 push\_back 完成的。如果我们之前从未见过 str，那么使用 operator[] 将它放入 map 中，且 vector 大小为 0，并返回该 vector，于是 push\_back 将 vector 的大小更新为 1。总之，这是一种超精辟的做法，它保持 map 使其中的值为一个集合。

这个算法的问题在于，它的速度太慢，在我们的计算机上用时97秒。一个明显的改进是避免比较不同长度的单词。我们可以通过按照长度将单词分组来做到这一点，然后在每个分组上运行上面的算法。

---

144

数据结构与算法分析——C++语言描述(第四版)

```txt
// 如果word1和word2具有相同的长度
// 并且只有一个字母不同，则返回true
bool oneCharOff( const string & word1, const string & word2 )
{
    if( word1.length( ) != word2.length( ))
        return false;

    int diffs = 0;

    for( int i = 0; i < word1.length( ); ++i )
        if( word1[ i ] != word2[ i ] )
            if( ++diffs > 1 )
                return false;

    return diffs == 1;
}
```

图 4.70 检测两个单词是否只在一个字母上不同的例程

```cpp
// 计算 map 对象，其中关键字为单词而值则是一些只在一个字母上
// 与对应的关键字不同单词组成的向量
// 使用一个二次的算法
map<string,vector<string>> computeAdjacentWords( const vector<string> & words )
{
    map<string,vector<string>> adjWords;

    for( int i = 0; i < words.size( ); ++i )
        for( int j = i + 1; j < words.size( ); ++j )
            if( oneCharOff( words[ i ], words[ j ] ) )
            {
                adjWords[ words[ i ] ].push_back( words[ j ] );
                adjWords[ words[ j ] ].push_back( words[ i ] );
            }

    return adjWords;
}
```

图 4.71 计算 map 对象的函数，该对象以一些单词作为关键字而以只在一个字母处互异的一列单词的 vector 作为其值。该函数对一个 89000 单词的词典运行 1.5 分钟

为此，可以使用第 2 个 map。此时，关键字是一个代表单词长度的整数，而值则是具有该长度的所有单词的集合。我们可以用 vector 存储每个集合，而相同的做法同样适用。代码如图 4.72 所示。第 8 行上显示的是第 2 个 map 的声明，第 11 行和第 12 行向这个 map 中添加成员，然后使用一个附加的循环对每个单词组进行迭代。与第 1 个算法相比，第 2 个算法只在边缘上编码困难而运行则只用了 18 秒，大约是改进前的 6 倍快。

我们的第 3 个算法更复杂，它使用了一些附加的 map。和前面一样，将单词按照长度分组，然后分别对每组进行处理。为理解这个算法是如何工作的，假设我们的工作对长度为 4 的单词进行。首先，要找出像 wine 和 nine 这样的单词对，它们除第 1 个字母外完全相同。一种做法是:对于长度为 4 的每一个单词，删除第 1 个字母，剩下一个 3 字母单词代表 (representative)。这样就形成一个 map，其中的关键字为该代表，而值则是包含该代表的所有

---

第4章 树

145

单词的一个 vector。例如，在考虑 4 字母单词组的第 1 个字母时，代表"ine"对应"dine"、"fine"、"wine"、"nine"、"mine"、"vine"、"pine"、"line"。代表"oot"对应"boot"、"foot"、"hoot"、"loot"、"soot"、"zoot"。每一个作为最新 map 的值的 vector 对象形成单词的一个团(clique)，其中任何一个单词均可以通过单字母替换变成另一个单词，因此在这个最新的 map 构成之后，遍历它以及添加一些项到正在被计算的原 map 中很容易。然后，我们再使用一个新的 map 来处理这个 4 字母单词组的第 2 个字母。此后处理第 3 个字母，最后处理第 4 个字母。

```txt
// 计算map对象，其中关键字为单词，而值则是单词组成的向量
// 向量中的单词只在一个字母上与对应的关键字不同
// 使用一个二次算法，通过保留一个附加的map加速处理过程
// 这个附加的map按长度将单词分组
map<string,vector<string>> computeAdjacentWords( const vector<string> & words )
{
    map<string,vector<string>> adjWords;
    map<int,vector<string>> wordsByLength;

    // 按长度将单词分组
    for( auto & thisWord : words )
        wordsByLength[ thisWord.length( ) ].push_back( thisWord );

    // 对每组分别进行处理
    for( auto & entry : wordsByLength )
    {
        const vector<string> & groupsWords = entry.second;

        for( int i = 0; i < groupsWords.size( ); ++i )
            for( int j = i + 1; j < groupsWords.size( ); ++j )
                if( oneCharOff( groupsWords[ i ], groupsWords[ j ] ) )
                {
                    adjWords[ groupsWords[ i ] ].push_back( groupsWords[ j ] );
                    adjWords[ groupsWords[ j ] ].push_back( groupsWords[ i ] );
                }
            }

        return adjWords;
    }
```

图 4.72 计算一个 map 对象的函数，这个 map 使用其中的单词作为关键字，而把只在一个字母上互异的那些单词构成的 vector 作为其值。按照单词的长度把单词分组。该算法对 89000 单词的词典运行耗时 18 秒总的处理轮廓如下:

```typescript
for each group g, containing words of length len
    for each position p (ranging from 0 to len-1)
    {
        Make an empty map<string,vector<string>> repsToWords
        for each word w
        {
            Obtain w's representative by removing position p
            Update repsToWords
        }
        Use cliques in repsToWords to update adjWords map
    }
```

---

146

数据结构与算法分析——C++语言描述(第四版)

图 4.73 包含该算法的一种实现，其运行时间改进到 2 秒。虽然这些附加的 map 使得算法更快，而且语法结构也相对清晰，但是程序没有利用到该 map 的这些关键字保持有序排列的事实，注意到这一点很有意思。

```txt
// 计算map对象，其中关键字为单词，值为单词的vector
// vector中的这些单词只在一个字母上不同于对应的关键字
// 使用一个高效的算法，该算法用到一个map运行时间为0(N log N)
map<string,vector<string>> computeAdjacentWords( const vector<string> & words )
{
    map<string,vector<string>> adjWords;
    map<int,vector<string>> wordsByLength;

    // 将单词按照它们的长度分组
    for( auto & str : words )
        wordsByLength[ str.length( ) ].push_back( str );

    // 对每组分别处理
    for( auto & entry : wordsByLength )
    {
        const vector<string> & groupsWords = entry.second;
        int groupNum = entry.first;

        // 对每组的每一个位置进行处理
        for( int i = 0; i < groupNum; ++i )
        {
            // 删除特定位置上的字母，算出代表
            // 具有相同代表的单词是相邻的；填充map ...
            map<string,vector<string>> repToWord;

            for( auto & str : groupsWords )
            {
                string rep = str;
                rep.erase( i, 1 );
                repToWord[ rep ].push_back( str );
            }

            // 然后查找那些具有多于一个串的map值
            for( auto & entry : repToWord )
            {
                const vector<string> & clique = entry.second;
                if( clique.size( ) >= 2 )
                    for( int p = 0; p < clique.size( ); ++p )
                        for( int q = p + 1; q < clique.size( ); ++q )
                        {
                            adjWords[ clique[ p ] ].push_back( clique[ q ] );
                            adjWords[ clique[ q ] ].push_back( clique[ p ] );
                        }
                    }
                }
            }
        return adjWords;
}
```

图 4.73 计算 map 的函数，该 map 包含单词作为关键字，以及只有一个字母不同的那些单词的 vector 作为其值。该算法对 89 000 单词的词典运行耗时 2 秒钟

---

第4章 树

147

同样，有一种支持 map 的操作但不保证有序排列的数据结构可能运行得更快，因为它被要求做的更少。第 5 章探索这种可能性，并讨论隐藏在另一种 map 实现背后的想法，C++ 将其添加到标准库 (Standard Library) 中，叫作 unordered\_map。无序映射 (unordered map) 将实现的运行时间从 2 秒减少到 1.5 秒。

## 小结

我们已经看到树在操作系统、编译器设计以及搜索中的应用。表达式树是更一般结构即所谓的分析树 (parse tree) 的一个小例子，分析树是编译器设计中的核心数据结构。分析树不是二叉树，而是表达式树相对简单的扩充 (可是，建立分析树的算法却不是那么简单)。

查找树在算法设计中是非常重要的。它几乎支持所有有用的操作，而其对数平均开销很小。查找树的非递归实现多少要快一些，但是递归实现更巧妙、更简练，而且更易于理解和除错。查找树的问题在于，其性能严重地依赖于随机的输入。如果情况不是这样，则运行时间会显著增加，使得查找树成为昂贵的链表。

我们看到了处理这个问题的几个方法。AVL 树要求所有节点的左子树与右子树的高度相差最多是 1。这就保证了树不至于太深。那些不改变树的操作(但插入操作使树改变)都可以使用标准二叉查找树的程序。改变树的操作必须将树恢复。这多少有些复杂，特别是在删除的情况。我们介绍了在以 $O(\log N)$ 时间插入后如何将树恢复。

我们还考察了伸展树。伸展树中的节点可以达到任意深度，但是在每次访问之后树又以多少有些神秘的方式被调整。实际效果在于，任意连续 $M$ 次操作花费 $O(M\log N)$ 时间，它与平衡树花费的时间相同。

与2路树或二叉树不同，B树是平衡 $M$ 路树，它能很好地适应磁盘；一种特殊情形是2-3树 $(M = 3)$，它是实现平衡查找树的另一种方法。

在实践中，所有平衡树方案的运行时间对于插入和删除操作(除查找稍微快一些外)都不如简单二叉查找树省时(差一个常数因子)，但考虑到从防止轻易得到最坏情形的输入来看，这一般说来还是可以接受的。第12章讨论某些另外的查找树数据结构并给出一些详细的实现方法。

最后注意:通过将一些元素插入到查找树然后执行一次中序遍历，我们得到的是排过顺序的元素。这给出排序的一种 $O(N\log N)$ 算法，如果使用任何成熟的查找树则它就是最坏情形的界。我们将在第7章介绍一些更好的方法，不过这些方法的时间界都不可能更低。

## 练习

4.1 对于图 4.74 中的树:

a. 哪个节点是根？
b. 哪些节点是树叶？

4.2 对于图 4.74 树上的每一个节点:

a. 指出它的父节点。
b. 列出它的儿子。
c. 列出它的兄弟。
d. 计算它的深度。

---

148

数据结构与算法分析——C++语言描述(第四版)

e. 计算它的高度。

4.3 图 4.74 中树的深度是多少?

![](../../raw/pages_0161-0192/images/page_161_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["A"] --> B["B"]
  B --> D["D"]
  B --> E["E"]
  D --> G["G"]
  D --> H["H"]
  E --> I["I"]
  E --> J["J"]
  J --> L["L"]
  J --> M["M"]
  C["C"] --> F["F"]
  F --> K["K"]
```
</details>

图 4.74 练习 4.1～练习 4.3 所用到的树

4.4 证明在 $N$ 个节点的二叉树中，存在 $N + 1$ 个 nullptr 链，它们代表 $N + 1$ 个儿子。
4.5 证明在高度为 h 的二叉树中，节点的最大个数是  $2^{h+1}-1$ 。
4.6 满节点(full node)是具有两个儿子的节点。证明满节点的个数加1等于非空二叉树的树叶的个数。
4.7 设二叉树在深度 $d_{1}, d_{2}, \ldots, d_{M}$ 处分别有树叶 $l_{1}, l_{2}, \ldots, l_{M}$。证明，$\sum_{i=1}^{M} 2^{-d_{i}} \leqslant 1$ 并确定何时等号成立。
4.8 给出对应图 4.75 中的树的前缀表达式、中缀表达式以及后缀表达式。

![](../../raw/pages_0161-0192/images/page_161_image_12.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["a"] --> B["*"]
  C["b"] --> B
  D["c"] --> E["+"]
  F["d"] --> E
  G["*"] --> E
  H["-"] --> I["e"]
```
</details>

图 4.75 练习 4.8 中的树

4.9 a. 指出将 3, 1, 4, 6, 9, 2, 5, 7 插入到初始为空的二叉查找树中的结果。

b. 指出删除根后的结果。

4.10 令 $f(N)$ 为 $N$ 节点二叉查找树中满节点的平均个数。

a. 确定  $f(0)$  和  $f(1)$  的值。
b. 证明对于 $N > 1$

$$
f (N) = \frac {N - 2}{N} + \frac {1}{N} \sum_ {i = 0} ^ {N - 1} (f (i) + f (N - i - 1))
$$

c. 通过归纳法证明， $f(N) = (N - 2)/3$ 是问题(b)中方程的一个解，其初始条件在问题(a)中。
d. 使用练习 4.6 的结果确定一棵 N 节点二叉查找树中树叶的平均数。

---

第4章 树

149

4.11 编写 set 类的实现程序，其中相关的迭代器使用二叉查找树。在每个节点上添加一个指向其父节点的链。

4.12 通过存储类型 set<Pair&lt;KeyType,ValueType&gt;>的一个数据成员编写实现 map 类的程序。

4.13 编写 set 类的实现程序，其中相关的迭代器使用二叉查找树。在每个节点上添加通向下一个最小节点和下一个最大节点的链。为使所写代码更简单，添加头节点和尾节点，它们不是二叉查找树的一部分，但有助于使得代码的链表部分更简单。

4.14 设欲做一个实验来验证由随机 insert/remove 操作对可能引起的问题。这里有一个策略，它虽不是完全随机的，但却足够接近随机。通过插入从 1 到 $M = \alpha N$ 之间随机选出的 $N$ 个元素来建立一棵具有 $N$ 个元素的树。然后执行 $N^2$ 对先插入后删除的操作。假设存在例程 randomInteger(a,b)，它返回一个在 a 和 b 之间（包括 a、b）的均匀随机整数。

a. 解释如何生成在 1 和 M 之间的一个随机整数，该整数不在这棵树上（从而随机插入可以进行）。用 N 和  $\alpha$  来表示这个操作的运行时间。

b. 解释如何生成在 1 和 M 之间的一个随机整数，该整数已经存在于这棵树上(从而随机删除可以进行)。这个操作的运行时间是多少？

c. α的好的选择是什么？为什么？

4.15 编写一个程序，凭经验计算下列删除具有两个儿子的节点的各方法的值:

a. 用  $T_{L}$  中最大节点 X 来代替，递归地删除 X。

b. 交替地用  $T_{L}$  中最大的节点以及  $T_{R}$  中最小的节点来代替，并递归地删除相应的节点。

c. 随机地选用  $T_{L}$  中最大的节点或  $T_{R}$  中最小的节点来代替(递归地删除适当的节点)。哪种方法给出最好的平衡？哪种在处理整个操作过程中花费最少的 CPU 时间？

4.16 重做二叉查找树类以实现懒惰删除。务必注意，这将影响所有的例程。特别具有挑战性的是 findMin 和 findMax，它们现在必须递归地完成。

\*\*4.17 证明，随机二叉查找树的深度(即最深的节点的深度)平均为 $O(\log N)$。

4.18 \*a. 给出高度为 h 的 AVL 树中节点最少个数的精确表达式。

b. 高度为 15 的 AVL 树中节点的最小个数是多少？

4.19 指出将 2, 1, 4, 5, 9, 3, 6, 7 插入到初始空 AVL 树后的结果。

\*4.20 依次将关键字 1, 2, ..., $2^{k}-1$ 插入到一棵初始空 AVL 树中。证明所得到的树是理想平衡 (perfectly balanced) 的。

4.21 写出实现 AVL 单旋转和双旋转的其余的过程。

4.22 设计一个线性时间算法, 该算法检验 AVL 树中的高度信息是否被正确保留并且平衡性质是否成立。

4.23 写出向 AVL 树进行插入的非递归函数。

4.24 证明图 4.47 中的删除算法是正确的。

4.25 a. 为了存储一棵 $N$ 节点的 AVL 树中一个节点的高度，每个节点需要多少比特位 (bit)? b. 使 8 比特高度计数器溢出的最小 AVL 树是什么样的树？

4.26 写出执行双旋转的函数，其效率要超过做两个单旋转。

4.27 指出依序访问图 4.76 的伸展树中关键字 3、9、1、5 后的结果。

---

150

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0161-0192/images/page_163_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  1["1"] --> 2["2"]
  n2["2"] --> 3["3"]
  4["4"] --> 6["6"]
  n4["4"] --> 10["10"]
  n6["6"] --> 5["5"]
  8["8"] --> 7["7"]
  n8["8"] --> 9["9"]
  n10["10"] --> 11["11"]
  n11["11"] --> 12["12"]
  n12["12"] --> 13["13"]
```
</details>

图 4.76 练习 4.27 中的树

4.28 指出在前一个练习所得到的伸展树中删除具有关键字 6 的元素后的结果。

4.29 a. 证明如果按顺序访问伸展树中的所有节点，则所得到的树由一连串的左儿子组成。

\*\*b. 证明如果依序访问伸展树中的所有节点，则总的访问时间是 $O(N)$，与初始树无关。

4.30 编写一个程序对伸展树执行一些随机操作。计算所执行的总的旋转次数。与 AVL 树和非平衡二叉查找树相比，其运行时间如何？

4.31 编写一些高效率的函数，只使用一个指向二叉树 $T$ 的根的指针，并计算:

a. T 中节点的个数。

b. T 中树叶的片数。

c. T 中满节点的个数。

所编写的函数的运行时间是多少？

4.32 设计一个递归的线性时间算法，该算法测试一棵二叉树是否在每一个节点都满足查找树的序的性质。

4.33 编写一个递归函数，该函数使用指向树 T 根节点的指针，并返回指向从 T 删除所有树叶所得到的树的根节点的指针。

4.34 写出生成一棵 $N$ 节点随机二叉查找树的函数，该树具有从1直到 $N$ 互异的关键字。该函数的运行时间是多少？

4.35 写出生成具有最少节点高度为 $h$ 的 AVL 树的函数，该函数的运行时间是多少？

4.36 编写一个函数,生成一棵具有关键字从 1 直到 $2^{h+1}-1$ 且高为 $h$ 的理想平衡二叉查找树 (perfectly balanced binary search tree)。该函数运行时间是多少?

4.37 编写一个函数，以二叉查找树 $T$ 和两个有序的关键字 $k_{1}$ 和 $k_{2}$ 作为输入，其中 $k_{1} \leqslant k_{2}$，并打印树中所有满足 $k_{1} \leqslant \operatorname{Key}(X) \leqslant k_{2}$ 的元素 $X$。除去可以被排序外，不对关键字的类型做任何假设。所写的程序应该以平均时间 $O(K + \log N)$ 运行，其中 $K$ 是所打印的关键字的个数。确定该算法的运行时间界。

4.38 本章中一些更大的二叉树是由一个程序自动生成的。这可以通过给树的每一个节点指定坐标 $(x, y)$，围绕每个坐标点画一个圆圈（在某些图片中这可能很难看清），并将每个节点连到它的父节点上来完成。假设在存储器中存有一棵二叉查找树（或许是由上面的一个例程生成的）并设每个节点都有两个附加的域存放坐标。

a. $x$ 坐标可以通过指定中序遍历数来计算。写出一个例程对树中的每个节点做这项工作。

---

第4章 树

151

b. y 坐标可以通过使用节点深度的负值算出。写出一个例程对树中的每个节点做这项工作。
c. 若使用某个虚拟的单位表示，则所画图形的具体尺寸是多少？如何调整单位使得所画的树总是高大约为宽的 2/3？
d. 证明，使用这个系统没有线出现交叉，同时，对于任意节点 X，X 的左子树的所有元素都出现在 X 的左边，X 的右子树的所有元素都出现在 X 的右边。

4.39 编写一个通用的画树程序，该程序将把一棵树转变成下列的图-汇编语言指令:

a. Circle $(X, Y)$
b. DrawLine(i, j)

第一个指令在 $(X, Y)$ 处画一个圆，而第二个指令则连接第i个圆和第j个圆（圆以所画的顺序编号）。你或者把它写成一个程序并定义某种输入语言，或者把它写成一个函数，该函数可以被任何程序调用。你的程序的运行时间是多少？

4.40 编写一个例程以层序(level-order)列出二叉树的节点。先列出根，然后列出深度为1的那些节点，再列出深度为2的节点，等等。必须要在线性时间内完成这个工作。证明所编例程的时间界。
4.41 \*a. 写出向一棵 B 树进行插入的例程。

\*b. 写出从一棵 B 树执行删除的例程。当一个项被删除时，是否有必要更新内部节点的信息？
\*c. 修改所编的插入例程，使得如果想要向一个已经有 M 项的节点添加元素，则在分裂该节点以前要执行搜索具有少于 M 个儿子的兄弟的工作。

4.42 $M$ 阶 $\mathbf{B}^{*}$ 树 $(\mathbf{B}^{*}$-tree) 是其每个内部节点的儿子数在 $2M/3$ 和 $M$ 之间的 $\mathbf{B}$ 树。描述一种向 $\mathbf{B}^{*}$ 树执行插入的方法。
4.43 指出如何用儿子/兄弟链的实现来表示图 4.77 中的树。

![](../../raw/pages_0161-0192/images/page_164_image_20.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["A"] --> B["B"]
  B --> D["D"]
  B --> E["E"]
  D --> H["H"]
  D --> I["I"]
  E --> J["J"]
  F["F"] --> K["K"]
  F --> L["L"]
  F --> M["M"]
  G["G"] --> N["N"]
  C["C"] --> F
  C --> M
  O["O"] --> L
  P["P"] --> Q["Q"]
  R["R"] --> M
```
</details>

图4.77 练习4.43中的树

4.44 编写一个过程遍历一棵用儿子/兄弟链存储的树。
4.45 如果两棵二叉树或者都是空树，或者非空且具有相似的左子树和右子树，则这两棵二叉树是相似(similar)的。编写一个函数以确定两棵二叉树是否相似。所编函数的运行时间是多少？
4.46 如果树 $T_{1}$ 通过交换其(某些)节点的左右儿子变换成树 $T_{2}$，则称树 $T_{1}$ 和 $T_{2}$ 是同构(isomorphic)的。例如，图4.78中的两棵树是同构的，因为交换 $A$、$B$、$G$ 的儿子而不交换其他节点后这两棵树是相同的。

a. 给出一个多项式时间算法以决定是否两棵树是同构的。

---

152

数据结构与算法分析——C++语言描述(第四版)

![](../../raw/pages_0161-0192/images/page_165_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> B["B"]
  A["A"] --> C["C"]
  B["B"] --> D["D"]
  B["B"] --> E["E"]
  B["B"] --> F["F"]
  C["C"] --> G["G"]
  C["C"] --> H["H"]
  D["D"] --> I["I"]
  E["E"] --> J["J"]
  F["F"] --> K["K"]
  G["G"] --> L["L"]
  H["H"] --> M["M"]
  I["I"] --> N["N"]
  J["J"] --> O["O"]
  K["K"] --> P["P"]
  L["L"] --> Q["Q"]
  M["M"] --> R["R"]
  N["N"] --> S["S"]
  O["O"] --> T["T"]
  P["P"] --> U["U"]
  Q["Q"] --> V["V"]
  R["R"] --> W["W"]
  S["W"] --> X["X"]
  Y["Y"] --> Z["Z"]
```
</details>

图 4.78 两棵同构的树

\*b. 所编程序的运行时间是多少(存在线性的解决方案)?

4.47 \*a. 证明，经过一些 AVL 单旋转，任意二叉查找树 $T_{1}$ 可以变换成另一棵(具有相同项的)查找树 $T_{2}$。

\*b. 给出一个算法平均用 $O(N \log N)$ 次旋转完成这种变换。

\*\*c. 证明该变换在最坏情形下可以用 $O(N)$ 次旋转完成。

4.48 设我们想要把操作 findKth 添加到指令集中去。该操作 findKth(k) 返回树中第 k 个最小项。假设所有的项都是互异的。解释如何修改二叉查找树以平均  $O(\log N)$  时间支持这种运算，而又不影响任何其他操作的时间界。

4.49 由于具有 $N$ 个节点的二叉查找树有 $N + 1$ 个 nullptr 指针, 因此在二叉查找树中为指针信息分配的空间有一半被浪费了。设若一个节点有一个 nullptr 左儿子, 我们使它的左儿子链接到它的中序前驱元 (inorder predecessor), 若一个节点有一个 nullptr 右儿子, 我们让它的右儿子链接到它的中序后继元 (inorder successor)。这就叫作线索树 (threaded tree), 而附加的链就叫作线索 (thread)。

a. 我们如何能够将线索从真儿子的指针中区分出来？

b. 编写执行向由上面描述的方式形成的线索树进行插入的例程和删除的例程。

c. 使用线索树的优点是什么？

4.50 编写一个程序, 该程序读入 C++源代码文件并以字母顺序输出所有的标识符(即变量名而非关键字, 并且这些变量名还不是从注释和串常数中找出的)。每个标识符要和它所在的那些行的行号一起输出。

4.51 为一本书生成一个索引。输入文件由一组索引项组成。每行由串 IX:组成，其后跟着一个索引项的名字(封在花括号内)，后面是封在花括号内的页号。在索引项名字中的每个!代表一个子层(sublevel)。符号|(代表一个范围的开始，而)|则代表这个范围的结束。偶尔这个范围是在同一页上。在这种情形下只输出一个单页的页号。在其他情况下不要套叠，否则就扩大了范围。例如，图 4.79 显示了一个样本输入，而图 4.80 则显示出对应的输出。

![](../../raw/pages_0161-0192/images/page_165_image_15.jpg)

<details>
<summary>text_image</summary>

IX: {Series|()          {2}
IX: {Series!geometric|()  {4}
IX: {Euler's constant}      {4}
IX: {Series!geometric|})  {4}
IX: {Series!arithmetic|() {4}
IX: {Series!arithmetic|})  {5}
IX: {Series!harmonic|()   {5}
IX: {Euler's constant}      {5}
IX: {Series!harmonic|})  {5}
IX: {Series|})          {5}
</details>

图 4.79 练习 4.51 的样本输入

---

第4章 树

153

```yaml
Euler's constant: 4, 5
Series: 2-5
    arithmetic: 4-5
    geometric: 4
    harmonic: 5
```

图4.80 练习4.51的样本输出

## 参考文献

关于二叉查找树的更多的信息,特别是树的数学性质,可以在 Knuth 的两本书([22]和[23])中找到。

有几篇论文处理由在二叉查找树中的有偏删除算法(biased deletion algorithm)引起的平衡不足问题。Hibbard的论文[19]提出原始删除算法并确立一次删除保持树的随机性的结果。文献[20]和[5]分别对只有3个节点的树和4个节点的树进行了全面的分析。Eppinger的论文[14]提供了非随机性的早期经验性的证据，而Culberson和Munro的论文[10]和[11]则提供了某些解析论证(但不是对混杂插入和删除的一般情形的完整证明)。

AVL 树由 Adelson-Velskii 和 Landis $^{[1]}$ 提出。最近有人证明了，对于 AVL 树，如果只对插入执行再平衡而不对删除进行，则在某些情况下所得到的结构仍然保持 $O(\log M)$ 的深度，其中 M 是插入的次数 $^{[28]}$ 。AVL 树的模拟结果以及高度的不平衡允许最多到 k（的不同的值）的各种变化在文献 $^{[21]}$ 中讨论。AVL 树的删除算法可以在文献 $^{[23]}$ 中找到。在 AVL 树中平均查找开销的分析是不完全的，不过，文献 $^{[24]}$ 中得到了某些结果。

文献[3]和[8]考虑了类似本书4.5.1节类型的自调整树。伸展树在文献[29]中作了描述。

B 树首先出现在文献[6]中。这篇原始论文所描述的实现允许数据既能存储在内部节点也能存储在树叶上。我们描述过的数据结构有时叫作 $\mathrm{B}^{+}$树。文献[9]对不同类型的 B 树进行了综合分析。文献[17]报告了各种方案的经验性结果。2-3 树和 B 树的分析可以在文献[4]、[13]以及[32]中找到。

练习 4.17 使人误以为很难。一种解法可以在文献[15]中找到。练习 4.29 取自文献[32]。在练习 4.42 中描述的 B\*树的信息可以在文献[12]中找到。练习 4.46 取自文献[2]。练习 4.47 的解法使用 2N-6 次旋转，该解法在文献[30]中给出。按照练习 4.49 的方式使用的线索 (threads) 首先在文献[27]中提出。处理多维数据的 k-d 树首先在文献[7]中提出，并在本书第 12 章进行了讨论。

另外一些流行的平衡查找树是红黑树 $^{[18]}$ 和赋权平衡树 $^{[26]}$ 。更多的平衡树方案可以在文献 $[16]$ 和 $[25]$ 中找到。

1. G. M. Adelson-Velskii and E. M. Landis, "An Algorithm for the Organization of Information," Soviet. Mat. Doklady, 3 (1962), 1259–1263.
2. A. V. Aho, J. E. Hopcroft, and J. D. Ullman, The Design and Analysis of Computer Algorithms, Addison-Wesley, Reading, Mass., 1974.
3. B. Allen and J. I. Munro, "Self Organizing Search Trees," Journal of the ACM, 25 (1978), 526–535.
4. R. A. Baeza-Yates, "Expected Behaviour of $B^{+}$-trees under Random Insertions," Acta Informatica, 26 (1989), 439-471.
5. R. A. Baeza-Yates, "A Trivial Algorithm Whose Analysis Isn't: A Continuation," BIT, 29 (1989), 88–113.

---

154

数据结构与算法分析——C++语言描述(第四版)

6. R. Bayer and E. M. McCreight, "Organization and Maintenance of Large Ordered Indices," Acta Informatica, 1 (1972), 173–189.
7. J. L. Bentley, "Multidimensional Binary Search Trees Used for Associative Searching," Communications of the ACM, 18 (1975), 509–517.
8. J. R. Bitner, "Heuristics that Dynamically Organize Data Structures," SIAM Journal on Computing, 8 (1979), 82–110.
9. D. Comer, "The Ubiquitous B-tree," Computing Surveys, 11 (1979), 121-137.
10. J. Culberson and J. I. Munro, "Explaining the Behavior of Binary Search Trees under Prolonged Updates: A Model and Simulations," Computer Journal, 32 (1989), 68–75.
11. J. Culberson and J. I. Munro, "Analysis of the Standard Deletion Algorithms in Exact Fit Domain Binary Search Trees," Algorithmica, 5 (1990), 295–311.
12. K. Culik, T. Ottman, and D. Wood, "Dense Multiway Trees," ACM Transactions on Database Systems, 6 (1981), 486–512.
13. B. Eisenbath, N. Ziviana, G. H. Gonnet, K. Melhorn, and D. Wood, "The Theory of Fringe Analysis and Its Application to 2–3 Trees and B-trees," Information and Control, 55 (1982), 125–174.
14. J. L. Eppinger, "An Empirical Study of Insertion and Deletion in Binary Search Trees," Communications of the ACM, 26 (1983), 663–669.
15. P. Flajolet and A. Odlyzko, "The Average Height of Binary Trees and Other Simple Trees," Journal of Computer and System Sciences, 25 (1982), 171–213.
16. G. H. Gonnet and R. Baeza-Yates, Handbook of Algorithms and Data Structures, 2d ed., Addison-Wesley, Reading, Mass., 1991.
17. E. Gudes and S. Tsur, "Experiments with B-tree Reorganization," Proceedings of ACM SIGMOD Symposium on Management of Data (1980), 200–206.
18. L. J. Guibas and R. Sedgewick, "A Dichromatic Framework for Balanced Trees," Proceedings of the Nineteenth Annual IEEE Symposium on Foundations of Computer Science (1978), 8–21.
19. T. H. Hibbard, "Some Combinatorial Properties of Certain Trees with Applications to Searching and Sorting," Journal of the ACM, 9 (1962), 13–28.
20. A. T. Jonassen and D. E. Knuth, "A Trivial Algorithm Whose Analysis Isn't," Journal of Computer and System Sciences, 16 (1978), 301–322.
21. P. L. Karlton, S. H. Fuller, R. E. Scroggs, and E. B. Kaehler, "Performance of Height Balanced Trees," Communications of the ACM, 19 (1976), 23–28.
22. D. E. Knuth, The Art of Computer Programming: Vol. 1: Fundamental Algorithms, 3d ed., Addison-Wesley, Reading, Mass., 1997.
23. D. E. Knuth, The Art of Computer Programming: Vol. 3: Sorting and Searching, 2d ed., Addison-Wesley, Reading, Mass., 1998.
24. K. Melhorn, "A Partial Analysis of Height-Balanced Trees under Random Insertions and Deletions," SIAM Journal of Computing, 11 (1982), 748–760.
25. K. Melhorn, Data Structures and Algorithms 1: Sorting and Searching, Springer-Verlag, Berlin, 1984.
26. J. Nievergelt and E. M. Reingold, "Binary Search Trees of Bounded Balance," SIAM Journal on Computing, 2 (1973), 33–43.
27. A. J. Perlis and C. Thornton, "Symbol Manipulation in Threaded Lists," Communications of the ACM, 3 (1960), 195–204.
28. S. Sen and R. E. Tarjan, "Deletion Without Rebalancing in Balanced Binary Trees," Proceedings of the Twentieth Symposium on Discrete Algorithms (2010), 1490–1499.
29. D. D. Sleator and R. E. Tarjan, "Self-adjusting Binary Search Trees," Journal of the ACM, 32 (1985), 652–686.
30. D. D. Sleator, R. E. Tarjan, and W. P. Thurston, "Rotation Distance, Triangulations, and Hyperbolic Geometry," Journal of the AMS (1988), 647–682.
31. R. E. Tarjan, "Sequential Access in Splay Trees Takes Linear Time," Combinatorica, 5 (1985), 367–378.
32. A. C. Yao, "On Random 2-3 Trees," Acta Informatica, 9 (1978), 159-170.
