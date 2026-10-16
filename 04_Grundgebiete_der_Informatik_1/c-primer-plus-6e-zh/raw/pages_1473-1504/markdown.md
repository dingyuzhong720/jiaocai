```txt
return ((long) num) * num;
}
```

14.输出如下:

1: Hi!

k is 1 in the loop

Now k is 3

k is 3 in the loop

Now k is 5

k is 5 in the loop

Now k is 7

k = 7

**A.7** 第7章复习题答案

1.b是true。

2.a.number >= 90 && number < 100

b.ch != 'q' && ch != 'k'

c.(number >= 1 && number <= 9) && number != 5

d.可以写成!(number >= 1 && number <= 9)，但是number < 1 || number > 9更好理解。

3.第5行:应该是scanf("%d %d", &weight, &height);。不要忘记scanf()中要用&。另外，这一行前面应该有提示用户输入的语句。

第9行:测试条件中要表达的意思是(height < 72 && height > 64)。根据前面第7行中的测试条件，能到第9行的height一定小于72，所以，只需要用表达式(height > 64)即可。但是，第6行中已经包含了height > 64这个条件，所以这里完全不必再判断，if else应改成else。

第11行:条件冗余。第2个表达式（weight不小于或不等于300）和第1个表达式含义相同。只需用一个简单的表达式(weight > 300)即可。但是，问题不止于此。第 11 行是一个错误的if，这行的else if与第6行的if匹配。但是，根据if的“最接近规则”，该else if应该与第9行的else if匹配。因此，在weight小于100且小于或等于64时到达第11行，而此时weight不可能超过300。

第7行～第10行:应该用花括号括起来。这样第11行就确定与第6行匹配。但是，如果把第9行的else if替换成简单的else，就不需要使用花括号。

第13行:应简化成if (height > 48)。实际上，完全可以省略这一行。因为第12行已经测试过该条件。

下面是修改后的版本:

```c
#include <stdio.h>

int main(void)

{

int weight, height; /* weight in lbs, height in inches */
printf("Enter your weight in pounds and ");
```

```txt
printf("your height in inches.\n");
scanf("%d %d", &weight, &height);
if (weight < 100 && height > 64)
if (height >= 72)
printf("You are very tall for your weight.\n");
else
printf("You are tall for your weight.\n");
else if (weight > 300 && height < 48)
printf(" You are quite short for your weight.\n");
else
printf("Your weight is ideal.\n");
return 0;
}
```

4.a.1。5确实大于2，表达式为真，即是1。

b.0。3比2大，表达式为假，即是0。

c.1。如果第 1 个表达式为假，则第 2 个表达式为真，反之亦然。所以，只要一个表达式为真，整个表达式的结果即为真。

d.6。因为6 > 2为真，所以(6 > 2)的值为1。

e.10。因为测试条件为真。

f.0。如果x > y为真，表达式的值就是 $\mathrm { _ y > x }$ ，这种情况下它为假或0。如果 $\mathrm { { [ X \geq y ] } }$ 为假，那么表达式的值就是 $\mathrm { _ { \mathrm { ( X \mathrm { \mathrm {  } ^ { > } } \mathrm { \mathrm { y } } } } }$ ，这种情况下为假。

5.该程序打印以下内容:

```javascript
*#0%*#0%$#0%*#0%*#0%$#0%*#0%*#0%$#0%*#0%*#0%
```

无论怎样缩排，每次循环都会打印#，因为缩排并不能让putchar('#');成为if else复合语句的一部分。

6.程序打印以下内容:

fat hat cat Oh no!

hat cat Oh no!

cat Oh no!

7.第5行～第7行的注释要以\*/结尾，或者把注释开头的/\*换成//。表达式 $a^{\prime} <= c h >= z$ 应替换成ch >= 'a' && $\mathrm { c h }   < =   \mathrm { ^ { \prime } z ^ { \prime } }$

或者，包含 ctype.h 并使用 islower()，这种方法更简单，而且可移植性更高。顺带一提，虽然从 C 的语法方面看， $a^{\prime} <= c h >= z$ 是有效的表达式，但是它的含义不明。因为关系运算符从左往右结合，该表达式被解释成('a' $< = \mathrm{ch} > = \mathrm{z}$ 。圆括号中的表达式的值不是1就是0（真或假），然后判断该值是否大于或等于'z'的数值码。1和0都不满足测试条件，所以整个表达式恒为0（假）。在第2个测试表达式中，应该把||改成&&。另外，虽然!(ch< 'A')是有

效的表达式，而且含义也正确，但是用 $\mathrm { c h } > = \mathrm { ^ { \prime } A ^ { \prime } }$ 更简单。这一行的'z'后面应该有两个圆括号。更简单的方法是使用isuupper()。在uc++;前面应该加一行else。否则，每输入一个字符， uc 都会递增 1。另外，在 printf()语句中的格式化字符串应该用双引号括起来。下面是修改后的版本:

```c
#include <stdio.h>
```

```c
#include <ctype.h>

int main(void)

{

char ch;

int lc = 0; /*统计小写字母*/

int uc = 0; /*统计大写字母*/

int oc = 0; /*统计其他字母*/

while ((ch = getchar()) != '#')

{

if (islower(ch))

lc++;

else if (isupper(ch))

uc++;

else

oc++;

}

printf("%d lowercase, %d uppercase, %d other", lc, uc, oc);
return 0;

}
```

8.该程序将不停重复打印下面一行:

You are 65.Here is your gold watch.

问题出在这一行:if (age = 65)

这行代码把age设置为65，使得每次迭代的测试条件都为真。

9.下面是根据给定输入的运行结果:

q

Step 1

Step 2

Step 3

c

Step 1

h

Step 1

Step 3

b

Step 1

Done

注意，b和#都可以结束循环。但是输入b会使得程序打印step 1，而输入#则不会。

10.下面是一种解决方案:

```c
#include <stdio.h>

int main(void)
{
char ch;
while ((ch = getchar()) != '#')
{
if (ch != '\n')
{
printf("Step 1\n");
if (ch == 'b')
break;
else if (ch != 'c')
{
if (ch != 'h')
printf("Step 2\n");
printf("Step 3\n");
}
}
```

```c
}

printf("Done\n");

return 0;

}
```

## A.8 第8章复习题答案

1.表达式 putchar(getchar())使程序读取下一个输入字符并打印出来。getchar()的返回值是putchar()的参数。但getchar(putchar())是无效的表达式，因为getchar()不需要参数，而putchar()需要一个参数。

2.a.显示字符H。

b.如果系统使用ASCII，则发出一声警报。

c.把光标移至下一行的开始。

d.退后一格。

3.count &lt;essay &gt;essayct或者count >essayct <essay

4.都不是有效的命令。

5.EOF是由getchar()和scanf()返回的信号（一个特殊值），表明函数检测到文件结尾。

6.a.输出是:If you qu

注意，字符I与字符i不同。还要注意，没有打印i，因为循环在检测到i之后就退出了。

b.如果系统使用ASCII，输出是:HJacrthjacrt

while的第1轮迭代中，为ch读取的值是H。第1个putchar()语句使用的ch的值是H，打印完毕后，ch的值加1（现在是ch的值是I）。然后到第2个putchar()语句，因为是++ch，所以先递增ch（现在ch的值是J）再打印它的值。然后进入下一轮迭代，读取输入序列中的下一个字符（a），重复以上步骤。需要注意的是，两个递增运算符只在ch被赋值后影响它的值，不会让程序在输入序列中移动。

7.C的标准I/O库把不同的文件映射为统一的流来统一处理。

8.数值输入会跳过空格和换行符，但是字符输入不会。假设有下面的代码:

```c
int score;

char grade;

printf("Enter the score.\n");

scanf("%s", %score);

printf("Enter the letter grade.\n");

grade = getchar();
```

如果输入分数98，然后按下Enter键把分数发送给程序，其实还发送了一个换行符。这个换行符会留在输入序列中，成为下一个读取的值（grade）。如果在字符输入之前输入了数字，就应该在处理字符输入之前添加删除换行符的代码。

## A.9 第9章复习题答案

1.形式参数是定义在被调函数中的变量。实际参数是出现在函数调用中的值，该值被赋给形式参数。可以把实际参数视为在函数调用时初始化形式参数的值。

```txt
2.a.void donut(int n)
b.int gear(int t1, int t2)
c.int guess(void)
d.void stuff_it(double d, double *pd)
3.a.char n_to_char(int n)
b.int digits(double x, int n)
c.double * which(double * p1, double * p2)
d.int random(void)
4.
int sum(int a, int b)
{
return a + b;
}
5.用double替换int即可:
double sum(double a, double b)
{
return a + b;
}
6.该函数要使用指针:
```

```lisp
void alter(int * pa, int * pb)
{
int temp;
temp = *pa + *pb;
*pb = *pa - *pb;
*pa = temp;
}
```

或者:

```txt
void alter(int * pa, int * pb)
{
*pa += *pb;
*pb = *pa - 2 * *pb;
}
```

7.不正确。num应声明在salami()函数的参数列表中，而不是声明在函数体中。另外，把count++改成num++。

8.下面是一种方案:

```c
int largest(int a, int b, int c)
{
int max = a;
```

```txt
if (b > max)
max = b;
if (c > max)
max = c;
return max;
}
```

9.下面是一个最小的程序，showmenu()和getchoice()函数分别是a和b的答案。

```c
#include <stdio.h>

/* 声明程序中要用到的函数 */
void showmenu(void);

int getchoice(int, int);

int main()
{
int res;

showmenu();
while ((res = getchoice(1, 4)) != 4)
{
printf("I like choice %d.\n", res);
```

```c
showmenu();
}
printf("Bye!\n");
return 0;
}
void showmenu(void)
{
printf("Please choose one of the following:\n");
printf("1) copy files          2) move files\n");
printf("3) remove files      4) quit\n");
printf("Enter the number of your choice:\n");
}
int getchoice(int low, int high)
{
int ans;
int good;
good = scanf("%d", &ans);
while (good == 1 && (ans < low || ans > high))
{
```

```c
printf("%d is not a valid choice; try again\n", ans);

showmenu();

scanf("%d", &ans);

}

if (good != 1)

{

printf("Non-numeric input.");

ans = 4;

}

return ans;

}
```

## A.10 第10章复习题答案

1.打印的内容如下:

```csv
8 8
4 4
0 0
2 2
```

2.数组ref有4个元素，因为初始化列表中的值是4个。
3.数组名ref指向该数组的首元素（整数8）。表达式ref + 1指向该数组的第2个元素（整数4）。++ref不是有效的表达式，因为ref是一个常量，不是变量。

4.ptr指向第1个元素，ptr + 2指向第3个元素（即第2行的第1个元素）。

a.12和16。

b.12和14（初始化列表中，用花括号把12括起来，把14和16括起来，所以12初始化第1行的第1个元素，而14初始化第2行的第1个元素）。

5.ptr指向第1行，ptr + 1指向第2行。\*ptr指向第1行的第1个元素，而\*(ptr + 1)指向第2行的第1个元素。

a.12和16。

b.12和14（同第4题，12初始化第1行的第1个元素，而14初始化第2行的第1个元素）。

6.a.&grid[22][56]

b.&grid[22][0]或grid[22]

（grid[22]是一个内含100个元素的一维数组，因此它就是首元素grid[22][0]的地址。）

c.&grid[0][0]或grid[0]或(int \*) grid

（grid[0]是int类型元素grid[0][0]的地址，grid是内含100个元素的grid[0]数组的地址。

这两个地址的数值相同，但是类型不同，可以用强制类型转换把它们转换成相同的类型。）

7.a.int digits[10];

b.float rates[6];

```txt
c.int mat[3][5];
d.char * psa[20] ;
```

注意，[]比\*的优先级高，所以在没有圆括号的情况下，psa先与[20]结合，然后再与\*结合。因此该声明与char \*(psa[20]);相同。

```javascript
e.char (*pstr)[20];
```

注意

对第e小题而言，char \*pstr[20];不正确。这会让pstr成为一个指针数组，而不是一个指向数组的指针。具体地说，如果使用该声明，pstr就指向一个char类型的值（即数组的第1个成员），而pstr + 1则指向下一个字节。使用正确的声明，pstr是一个变量，而不是一个数组名。而且pstr+ 1指向起始字节后面的第20个字节。

```txt
a.int sextet[6] = {1, 2, 4, 8, 16, 32};
b.sextet[2]
c.int lots[100] = { [99] = -1};
d.int pots[100] = { [5] = 101, [10] = 101,101, 101, 101};
9.0~9
```

10.a.rootbeer[2] = value;有效。

b.scanf("%f", &rootbeer );无效，rootbeer不是float类型。

c.rootbeer = value;无效，rootbeer不是float类型。

d.printf("%f", rootbeer);无效，rootbeer不是float类型。

e.things[4][4] = rootbeer[3];有效。

f.things[5] = rootbeer;无效，不能用数组赋值。

g.pf = value;无效，value不是地址。

h.pf = rootbeer;有效。

11.int screen[800][600] ;

12.a.

void process(double ar[], int n);

void processvla(int n, double ar[n]);

process(trots, 20);

processvla(20, trots);

b.

void process2(short ar2[30], int n);

void process2vla(int n, int m, short ar2[n][m]);

process2(clops, 10);

process2vla(10, 30, clops);

c.

void process3(long ar3[10][15], int n);

void process3vla(int n, int m,int k, long ar3[n][m][k]);

process3(shots, 5);

process3vla(5, 10, 15, shots);

13.a.

show( (int [4]) {8,3,9,2}, 4);

b.

show2( (int [][3]){{8,3,9}, {5,4,1}}, 2);

## A.11 第11章复习题答案

1.如果希望得到一个字符串，初始化列表中应包含'\0'。当然，也可以用另一种语法自动添加空字符:

char name[] = "Fess";

2.

See you at the snack bar.

ee you at the snack bar.

See you

e you

3.

y

my

mmy

ummy

Yummy

4.I read part of it all the way through.

5.a.Ho Ho Ho!!oH oH oH

b.指向char的指针（即，char \*）。

c.第1个H的地址。

d.\*--pc的意思是把指针递减1，并使用储存在该位置上的值。--\*pc的意思是解引用pc指向的值，然后把该值减1（例如，H变成G）。

e.Ho Ho Ho!!oH oH o

注意

在两个！之间有一个空字符，但是通常该字符不会产生任何打印的效果。

f.while (\*pc)检查 pc 是否指向一个空字符（即，是否指向字符串的末尾）。while 的测试条件中使用储存在指针指向位置上的值。

while (pc - str)检查pc是否与str指向相同的位置（即，字符串的开头）。while的测试条件中使用储存在指针指向位置上的值。

g.进入第1个while循环后，pc指向空字符。进入第2个while循环后，它指向空字符前面的存储区（即，str 所指向位置前面的位置）。把该字节解释成一个字符，并打印这个字符。然后指针退回到前面的字节处。永远都不会满足结束条件(pc == str)，所以这个过程会一直持续下去。

h.必须在主调程序中声明pr():char \* pr(char \*);

6.字符变量占用一个字节，所以sign占1字节。但是字符常量储存为int类型，意思是'\$'通常占用2或4字节。但是实际上只使用int的1字节储存'\$'的编码。字符串"\$"使用2字节:一个字节储存'\$'的编码，一个字节储存的'\0'编码。

7.打印的内容如下:

How are ya, sweetie? How are ya, sweetie?

Beat the clock.

eat the clock.

Beat the clock.Win a toy.

Beat

chat

hat

at

t

t

at

How are ya, sweetie?

8.打印的内容如下:

faavrhee

\*le\*on\*sm

9.下面是一种方案:

#include &lt;stdio.h&gt; // 提供fgets()和getchar()的原型

char \* s\_gets(char \* st, int n)

```c
{
char * ret_val;
ret_val = fgets(st, n, stdin);
if (ret_val)
{
while (*st != '\n' && *st != '\0')
st++;
if (*st == '\n')
*st = '\0';
else
while (getchar() != '\n')
continue;
}
return ret_val;
}
10.下面是一种方案:
int strlen(const char * s)
{
int ct = 0;
```

```txt
while (*s++)          // 或者while (*s++ != '\0')

ct++;

return(ct);

}
```

11.下面是一种方案:

```c
#include <stdio.h>      // 提供 fgets()和getchar()的原型
#include <string.h>   // 提供 strchr()的原型

char * s_gets(char * st, int n)

{

char * ret_val;

char * find;

ret_val = fgets(st, n, stdin);

if (ret_val)

{

find = strchr(st, '\n');  // 查找换行符

if (find)                          // 如果地址不是 NULL,
*find = '\0';          // 在此处放置一个空字符

else

while (getchar() != '\n')
```

```txt
continue;

}

return ret_val;

}
```

12.下面是一种方案:

```c
#include <stdio.h>      /* 提供 NULL 的定义 */

char * strblk(char * string)
{
while (*string != '' && *string != '\0')
string++;          /* 在第1个空白或空字符处停止 */
if (*string == '\0')
return NULL;       /* NULL 指空指针 */
else
return string;
}
```

下面是第2种方案，可以防止函数修改字符串，但是允许使用返回值改变字符串。表达式(char\*)string被称为“通过强制类型转换取消const”。

#include &lt;stdio.h&gt; /\*提供 NULL的定义\*/

char \* strblk(const char \* string)

```txt
{
while (*string != '' && *string != '\0')
string++;          /*在第1个空白或空字符处停止*/
if (*string == '\0')
return NULL;       /* NULL 指空指针*/
else
return (char *)string;
}
```

13.下面是一种方案:

```c
/* compare.c -- 可行方案 */
#include <stdio.h>
#include <string.h> // 提供strcmp()的原型
#include <ctype.h>
#define ANSWER "GRANT"
#define SIZE 40
char * s_gets(char * st, int n);
void ToUpper(char * str);
int main(void)
{
```

```c
char try[SIZE];
puts("Who is buried in Grant's tomb?");
s_gets(try, SIZE);
ToUpper(try);
while (strcmp(try, ANSWER) != 0)
{
puts("No, that's wrong.Try again.");
s_gets(try, SIZE);
ToUpper(try);
}
puts("That's right!");
return 0;
}
void ToUpper(char * str)
{
while (*str != '\0')
{
*str = toupper(*str);
str++;
```

```c
}
}
char * s_gets(char * st, int n)
{
char * ret_val;
int i = 0;
ret_val = fgets(st, n, stdin);
if (ret_val)
{
while (st[i] != '\n' && st[i] != '\0')
i++;
if (st[i] == '\n')
st[i] = '\0';
else
while (getchar() != '\n')
continue;
}
return ret_val;
}
```

## A.12 第12章复习题答案

1.自动存储类别；寄存器存储类别；静态、无链接存储类别。
2.静态、无链接存储类别；静态、内部链接存储类别；静态、外部链接存储类别。
3.静态、外部链接存储类别可以被多个文件使用。静态、内部链接存储类别只能在一个文件中使用。

4.无链接。

5.关键字extern用于声明中，表明该变量或函数已定义在别处。

6.两者都分配了一个内含100个int类型值的数组。第2行代码使用calloc()把数组中的每个元素都设置为0。

7.默认情况下，daisy只对main()可见，以extern声明的daisy才对petal()、stem()和root()可见。文件2中的extern int daisy;声明使得daisy对文件2中的所有函数都可见。第1个lily是main()的局部变量。petal()函数中引用的lily是错误的，因为两个文件中都没有外部链接的lily。虽然文件2中有一个静态的lily，但是它只对文件2可见。第1个外部rose对root()函数可见，但是stem()中的局部rose覆盖了外部的rose。

8.下面是程序的输出:

color in main() is B
color in first() is R
color in main() is B
color in second() is G
color in main() is G

first()函数没有使用color变量，但是second()函数使用了。

9.a.声明告诉我们，程序将使用一个变量plink，该文件包含的函数都可以使用这个变量。calu\_ct()函数的第1个参数是指向一个整数的指针，并假定它指向内含n个元素的数组。这里关键是要理解该程序不允许使用指针arr修改原始数组中的值。
b.不会。value和n已经是原始数据的备份，所以该函数无法更改主调函数中相应的值。这些声明的作用是防止函数修改value和n的值。例如，如果用const限定n，就不能使用n++表达式。

## A.13 第13章复习题答案

1.根据文件定义，应包含#include &lt;stdio.h&gt;。应该把fp声明为文件指针:FILE \*fp;。要给fopen()函数提供一种模式:fopen("gelatin","w")，或者"a"模式。fputs()函数的参数顺序应该反过来。输出字符串应该有一个换行符，提高可读性。fclose()函数需要一个文件指针，而不是一个文件名:

fclose(fp);。下面是修改后的版本:

```c
#include <stdio.h>

int main(void)

{

FILE * fp;

int k;

fp = fopen("gelatin", "w");

for (k = 0; k < 30; k++)

fputs("Nanette eats gelatin.\n", fp);
```

```txt
fclose(fp);

 return 0;

}
```

2.如果可以打开的话，会打开与命令行第1个参数名相同名称的文件，并在屏幕上显示文件中的每个数字字符。

```javascript
3.a.ch = getc(fp1);
b.fprintf(fp2,"%c"\n",ch);
c.putc(ch,fp2);
d fclose(fp1); /* 关闭terky文件 */
```

注意

fp1用于输入操作，因为它识别以读模式打开的文件。与此类似，fp2以写模式打开文件，所以常用于输出操作。

4.下面是一种方案:

```c
#include <stdio.h>

#include <stdlib.h>

int main(int argc, char * argv [])
{
FILE * fp;

double n;

double sum = 0.0;
```

```c
int ct = 0;

if (argc == 1)

fp = stdin;

else if (argc == 2)

{

if ((fp = fopen(argv[1], "r")) == NULL)

{

fprintf(stderr, "Can't open %s\n", argv[1]);

exit(EXIT_FAILURE);

}

}

else

{

fprintf(stderr, "Usage: %s [filename]\n", argv[0]);

exit(EXIT_FAILURE);

}

while (fscanf(fp, "%lf", &n) == 1)
{

sum += n;
```

```txt
++ct;

}

if (ct > 0)

printf("Average of %d values = %f\n", ct, sum / ct);

else

printf("No valid data.\n");

return 0;

}
```

5.下面是一种方案:

```c
#include <stdio.h>

#include <stdlib.h>

#define BUF 256

int has_ch(char ch, const char * line);

int main(int argc, char * argv [])
{
FILE * fp;

char ch;

char line[BUF];

if (argc != 3)
```

```c
{
printf("Usage: %s character filename\n", argv[0]);
exit(EXIT_FAILURE);
}
ch = argv[1][0];
if ((fp = fopen(argv[2], "r")) == NULL)
{
printf("Can't open %s\n", argv[2]);
exit(EXIT_FAILURE);
}
while (fgets(line, BUF, fp) != NULL)
{
if (has_ch(ch, line))
fputs(line, stdout);
}
fclose(fp);
return 0;
}
int has_ch(char ch, const char * line)
```