# 附录II 积分表

原始 PDF 第 286–292 页。

附录Ⅱ

积分表

## 一、含有 $x^n$ 的形式

1. $\int x^{n}\mathrm{d}x = \frac{x^{n + 1}}{n + 1} +C,\quad n\neq -1$
2. $\int \frac{1}{x} \mathrm{d}x = \ln |x| + C$

## 二、含有 $a + bx$ 的形式

3. $\int \frac{x}{a + bx}\mathrm{d}x = \frac{1}{b^2} (bx - a\ln |a + bx|) + C$

4. $\int \frac{x}{(a + bx)^2} \, \mathrm{d}x = \frac{1}{b^2} \left( \frac{a}{a + bx} + \ln |a + bx| \right) + C$

5. $\int \frac{x}{(a + bx)^n} \, \mathrm{d}x = \frac{1}{b^2} \left[ \frac{-1}{(n - 2)(a + bx)^{n-2}} + \right.$

$$
\left. \frac {a}{(n - 1) (a + b x) ^ {n - 1}} \right] + C, \quad n \neq 1, 2
$$

6. $\int \frac{x^2}{a + bx}\mathrm{d}x = \frac{1}{b^3}\left[-\frac{bx}{2} (2a - bx) + a^2\ln |a + bx|\right] + C$

7. $\int \frac{x^2}{(a + bx)^2} \, \mathrm{d}x = \frac{1}{b^3} \left( bx - \frac{a^2}{a + bx} - 2a \ln |a + bx| \right) + C$

8. $\int \frac{x^2}{(a + bx)^3} \, \mathrm{d}x = \frac{1}{b^3} \left[ \frac{2a}{a + bx} - \frac{a^2}{2(a + bx)^2} + \ln |a + bx| \right] + C$

9. $\int \frac{x^2}{(a + bx)^n}\mathrm{d}x = \frac{1}{b^3}\left[\frac{-1}{(n - 3)(a + bx)^{n - 3}} +\right.$

$$
\left. \frac {2 a}{(n - 2) (a + b x) ^ {n - 2}} - \frac {a ^ {2}}{(n - 1) (a + b x) ^ {n - 1}} \right] + C, \quad n \neq 1, 2, 3
$$

10. $\int \frac{1}{x(a + bx)}\mathrm{d}x = \frac{1}{a}\ln \left|\frac{x}{a + bx}\right| + C$

11. $\int \frac{1}{x(a + bx)^2} \, \mathrm{d}x = \frac{1}{a} \left( \frac{1}{a + bx} + \frac{1}{a} \ln \left| \frac{x}{a + bx} \right| \right) + C$

12. $\int \frac{1}{x^2(a + bx)}\mathrm{d}x = -\frac{1}{a}\left(\frac{1}{x} +\frac{b}{a}\ln \left|\frac{x}{a + bx}\right|\right) + C$

275

---

附录Ⅱ 积分表

13. $\int \frac{1}{x^2(a + bx)^2}\mathrm{d}x = -\frac{1}{a^2}\left[\frac{a + 2bx}{x(a + bx)} +\frac{2b}{a}\ln \left|\frac{x}{a + bx}\right|\right] + C$

## 三、含有 $a^2 \pm x^2, a > 0$ 的形式

14. $\int \frac{1}{a^2 + x^2}\mathrm{d}x = \frac{1}{a}\arctan \frac{x}{a} +C$
15. $\int \frac{1}{x^2 - a^2}\mathrm{d}x = -\int \frac{1}{a^2 - x^2}\mathrm{d}x = \frac{1}{2a}\ln \left|\frac{x - a}{x + a}\right| + C$
16. $\int \frac{1}{(a^2\pm x^2)^n}\mathrm{d}x = \frac{1}{2a^2(n - 1)}\left[\frac{x}{(a^2\pm x^2)^{n - 1}} +\right.$

$$
(2 n - 3) \int \frac {1}{(a ^ {2} \pm x ^ {2}) ^ {n - 1}} \mathrm{d} x \Big ], \quad n \neq 1
$$

## 四、含有 $a + bx + cx^2, b^2 \neq 4ac$ 的形式

17. $\int \frac{1}{a + bx + cx^2}\mathrm{d}x = \frac{2}{\sqrt{4ac - b^2}}\arctan \frac{2cx + b}{\sqrt{4ac - b^2}} +C,\quad b^2 < 4ac$

$$
= \frac {1}{\sqrt {b ^ {2} - 4 a c}} \ln \left| \frac {2 c x + b - \sqrt {b ^ {2} - 4 a c}}{2 c x + b + \sqrt {b ^ {2} - 4 a c}} \right| + C, \quad b ^ {2} > 4 a c
$$

18. $\int \frac{x}{a + bx + cx^2}\mathrm{d}x = \frac{1}{2c}\left(\ln |a + bx + cx^2| - b\int \frac{1}{a + bx + cx^2}\mathrm{d}x\right)$

## 五、含有 $\sqrt{a + bx}$ 的形式

19. $\int x^{n}\sqrt{a + bx}\mathrm{d}x = \frac{2}{b(2n + 3)}\cdot \left[x^{n}(a + bx)^{3 / 2} - na\int x^{n - 1}\sqrt{a + bx}\mathrm{d}x\right]$

20. $\int \frac{1}{x\sqrt{a + bx}}\mathrm{d}x = \frac{1}{\sqrt{a}}\ln \left|\frac{\sqrt{a + bx} - \sqrt{a}}{\sqrt{a + bx} + \sqrt{a}}\right| + C,\quad a > 0$

$$
= \frac {2}{\sqrt {- a}} \arctan \sqrt {\frac {a + b x}{- a}} + C, \quad a <   0
$$

21. $\int \frac{1}{x^n\sqrt{a + bx}}\mathrm{d}x = \frac{-1}{a(n - 1)}\left[\frac{\sqrt{a + bx}}{x^{n - 1}} +\frac{b(2n - 3)}{2}\int \frac{1}{x^{n - 1}\sqrt{a + bx}}\mathrm{d}x\right],\quad n\neq 1$
22. $\int \frac{\sqrt{a + bx}}{x}\mathrm{d}x = 2\sqrt{a + bx} +a\int \frac{1}{x\sqrt{a + bx}}\mathrm{d}x$
23. $\int \frac{\sqrt{a + bx}}{x^n}\mathrm{d}x = \frac{-1}{a(n - 1)}\left[\frac{(a + bx)^{3 / 2}}{x^{n - 1}} +\right.$

276

---

附录Ⅱ 积分表

11

$$
\frac {(2 n - 5) b}{2} \int \frac {\sqrt {a + b x}}{x ^ {n - 1}} \mathrm{d} x \Bigg ], \quad n \neq 1
$$

24. $\int \frac{x}{\sqrt{a + bx}}\mathrm{d}x = \frac{-2(2a - bx)}{3b^2}\sqrt{a + bx} +C$
25. $\int \frac{x^n}{\sqrt{a + bx}}\mathrm{d}x = \frac{2}{(2n + 1)b}\left(x^n\sqrt{a + bx} -na\int \frac{x^{n - 1}}{\sqrt{a + bx}}\mathrm{d}x\right)$

## 六、含有 $\sqrt{x^2\pm a^2}$ ， $a > 0$ 的形式

26. $\int \sqrt{x^2 \pm a^2} \, \mathrm{d}x = \frac{1}{2}\left(x\sqrt{x^2 \pm a^2} \pm a^2 \ln |x + \sqrt{x^2 \pm a^2} |\right) + C$
27. $\int x^{2}\sqrt{x^{2} \pm a^{2}}\mathrm{d}x = \frac{1}{8}\left[x(2x^{2} \pm a^{2})\sqrt{x^{2} \pm a^{2}} - a^{4}\ln |x + \sqrt{x^{2} \pm a^{2}}|\right] + C$
28. $\int \frac{1}{x}\sqrt{x^2 + a^2}\mathrm{d}x = \sqrt{x^2 + a^2} -a\ln \left|\frac{a + \sqrt{x^2 + a^2}}{x}\right| + C$
29. $\int \frac{1}{x}\sqrt{x^2 - a^2}\mathrm{d}x = \sqrt{x^2 - a^2} -a\arccos \frac{a}{x} +C$
30. $\int \frac{1}{x^2}\sqrt{x^2\pm a^2}\mathrm{d}x = \frac{-1}{x}\sqrt{x^2\pm a^2} +\ln |x + \sqrt{x^2\pm a^2}| + C$
31. $\int \frac{1}{\sqrt{x^2 \pm a^2}} \, \mathrm{d}x = \ln |x + \sqrt{x^2 \pm a^2}| + C$
32. $\int \frac{x^2}{\sqrt{x^2 \pm a^2}} \, \mathrm{d}x = \frac{1}{2} (x\sqrt{x^2 \pm a^2} + a^2 \ln |x + \sqrt{x^2 \pm a^2}|) + C$
33. $\int \frac{1}{x\sqrt{x^2 - a^2}}\mathrm{d}x = \frac{1}{a}\arccos \frac{a}{x} +C$
34. $\int \frac{1}{x\sqrt{x^2 + a^2}}\mathrm{d}x = \frac{-1}{a}\ln \left|\frac{a + \sqrt{x^2 + a^2}}{x}\right| + C$
35. $\int \frac{1}{x^2\sqrt{x^2\pm a^2}}\mathrm{d}x = \mp \frac{\sqrt{x^2\pm a^2}}{a^2x} +C$
36. $\int \frac{1}{(x^2\pm a^2)^{3 / 2}}\mathrm{d}x = \frac{\pm x}{a^2\sqrt{x^2\pm a^2}} +C$

## 七、含有 $\sqrt{a^2 - x^2}, a > 0$ 的形式

37. $\int \sqrt{a^2 - x^2} \, \mathrm{d}x = \frac{1}{2} \left( x\sqrt{a^2 - x^2} + a^2 \arcsin \frac{x}{a} \right) + C$
38. $\int x^{2}\sqrt{a^{2} - x^{2}}\mathrm{d}x = \frac{1}{8}\left[x(2x^{2} - a^{2})\sqrt{a^{2} - x^{2}} +a^{4}\arcsin \frac{x}{a}\right] + C$
39. $\int \frac{1}{x}\sqrt{a^2 - x^2} \, \mathrm{d}x = \sqrt{a^2 - x^2} - a\ln \left|\frac{a + \sqrt{a^2 - x^2}}{x}\right| + C$

277

---

附录Ⅱ 积分表

40. $\int \frac{1}{x^2}\sqrt{a^2 - x^2}\mathrm{d}x = \frac{-1}{x}\sqrt{a^2 - x^2} -\arcsin \frac{x}{a} +C$
41. $\int \frac{1}{\sqrt{a^2 - x^2}}\mathrm{d}x = \arcsin \frac{x}{a} +C$
42. $\int \frac{1}{x\sqrt{a^2 - x^2}}\mathrm{d}x = \frac{-1}{a}\ln \left|\frac{a + \sqrt{a^2 - x^2}}{x}\right| + C$
43. $\int \frac{1}{x^2\sqrt{a^2 - x^2}}\mathrm{d}x = \frac{-\sqrt{a^2 - x^2}}{a^2x} +C$
44. $\int \frac{x^2}{\sqrt{a^2 - x^2}}\mathrm{d}x = \frac{1}{2}\left(-x\sqrt{a^2 - x^2} +a^2\arcsin \frac{x}{a}\right) + C$
45. $\int \frac{1}{(a^2 - x^2)^{3 / 2}}\mathrm{d}x = \frac{x}{a^2\sqrt{a^2 - x^2}} +C$

## 八、含有 $\sin x$ 或 $\cos x$ 的形式

46. $\int \sin x\mathrm{d}x = -\cos x + C$
47. $\int \cos x\mathrm{d}x = \sin x + C$
48. $\int \sin^2 x\mathrm{d}x = \frac{1}{2} (x - \sin x\cos x) + C$
49. $\int \cos^2 x\mathrm{d}x = \frac{1}{2} (x + \sin x\cos x) + C$
50. $\int \sin^n x\mathrm{d}x = \frac{1}{n}\left[-\sin^{n - 1}x\cos x + (n - 1)\int \sin^{n - 2}x\mathrm{d}x\right]$
51. $\int \cos^n x\mathrm{d}x = \frac{1}{n}\left[\cos^{n - 1}x\sin x + (n - 1)\int \cos^{n - 2}x\mathrm{d}x\right]$
52. $\int x\sin x\mathrm{d}x = \sin x - x\cos x + C$
53. $\int x\cos x\mathrm{d}x = \cos x + x\sin x + C$
54. $\int x^{n}\sin x\mathrm{d}x = -x^{n}\cos x + n\int x^{n - 1}\cos x\mathrm{d}x$
55. $\int x^{n}\cos x\mathrm{d}x = x^{n}\sin x - n\int x^{n - 1}\sin x\mathrm{d}x$
56. $\int \frac{1}{1 \pm \sin x} \, \mathrm{d}x = \tan x \mp \sec x + C$
57. $\int \frac{1}{1\pm\cos x}\mathrm{d}x = -\cot x\pm \csc x + C$
58. $\int \frac{1}{\sin x\cos x}\mathrm{d}x = \ln |\tan x| + C$

278

---

附录Ⅱ 积分表

## 九、含有 $\tan x, \cot x, \sec x, \csc x$ 的形式

59. $\int \tan x\mathrm{d}x = -\ln |\cos x| + C$
60. $\int \cot x\mathrm{d}x = \ln |\sin x| + C$
61. $\int \sec x\mathrm{d}x = \ln |\sec x + \tan x| + C$
62. $\int \csc x\mathrm{d}x = \ln |\csc x - \cot x| + C$
63. $\int \tan^2 x\mathrm{d}x = -x + \tan x + C$
64. $\int \cot^2 x\mathrm{d}x = -x - \cot x + C$
65. $\int \sec^2 x\mathrm{d}x = \tan x + C$
66. $\int \csc^2 x\mathrm{d}x = -\cot x + C$
67. $\int \tan^n x\mathrm{d}x = \frac{\tan^{n - 1}x}{n - 1} -\int \tan^{n - 2}x\mathrm{d}x,\quad n\neq 1$
68. $\int \cot^n x\mathrm{d}x = -\frac{\cot^{n - 1}x}{n - 1} -\int \cot^{n - 2}x\mathrm{d}x,\quad n\neq 1$
73. $\int \frac{1}{1 \pm \sec x} \, \mathrm{d}x = x + \cot x \mp \csc x + C$
74. $\int \frac{1}{1 \pm \csc x} \, \mathrm{d}x = x - \tan x \pm \sec x + C$

69. $\int \sec^n x\mathrm{d}x = \frac{\sec^{n - 2}x\tan x}{n - 1} +\frac{n - 2}{n - 1}\int \sec^{n - 2}x\mathrm{d}x,\quad n\neq 1$

70. $\int \csc^n x\mathrm{d}x = -\frac{\csc^{n - 2}x\cot x}{n - 1} +\frac{n - 2}{n - 1}\int \csc^{n - 2}x\mathrm{d}x,\quad n\neq 1$

71. $\int \frac{1}{1 \pm \tan x} \, \mathrm{d}x = \frac{1}{2} (x \pm \ln |\cos x \pm \sin x|) + C$

72. $\int \frac{1}{1 \pm \cot x} \mathrm{d}x = \frac{1}{2} (x \mp \ln |\sin x \pm \cos x|) + C$

## 十、含有反三角函数的形式

75. $\int \arcsin x\mathrm{d}x = x\arcsin x + \sqrt{1 - x^2} +C$
76. $\int \arccos x\mathrm{d}x = x\arccos x - \sqrt{1 - x^2} +C$
77. $\int \arctan x\mathrm{d}x = x\arctan x - \frac{1}{2}\ln (1 + x^2) + C$
78. $\int \operatorname{arccot} x \, \mathrm{d}x = x \operatorname{arccot} x + \frac{1}{2} \ln (1 + x^2) + C$

279

---

附录Ⅱ 积分表

79. $\int \operatorname{arcsec} x \, \mathrm{d}x = x \operatorname{arcsec} x - \ln |x + \sqrt{x^2 - 1}| + C$
80. $\int \operatorname{arccsc} x \, \mathrm{d}x = x \operatorname{arccsc} x + \ln |x + \sqrt{x^2 - 1}| + C$
81. $\int x\arcsin x\mathrm{d}x = \frac{1}{4}\left[x\sqrt{1 - x^2} +(2x^2 -1)\arcsin x\right] + C$
82. $\int x\arccos x\mathrm{d}x = \frac{1}{4}\left[-x\sqrt{1 - x^2} + (2x^2 - 1)\arccos x\right] + C$
83. $\int x\arctan x\mathrm{d}x = \frac{1}{2}\left[(1 + x^2)\arctan x - x\right] + C$
84. $\int x\operatorname{arccot}x\mathrm{d}x = \frac{1}{2}\left[(1 + x^2)\operatorname{arccot}x + x\right] + C$

## 十一、含有 $\mathrm{e}^x$ 的形式

85. $\int a^{x}\mathrm{d}x = \frac{a^{x}}{\ln a} +C$

86. $\int \mathrm{e}^{x}\mathrm{d}x = \mathrm{e}^{x} + C$

87. $\int x\mathrm{e}^{x}\mathrm{d}x = (x - 1)\mathrm{e}^{x} + C$

88. $\int x^{n}\mathrm{e}^{x}\mathrm{d}x = x^{n}\mathrm{e}^{x} - n\int x^{n - 1}\mathrm{e}^{x}\mathrm{d}x$

89. $\int \frac{1}{1 + \mathrm{e}^x}\mathrm{d}x = x - \ln (1 + \mathrm{e}^x) + C$

90. $\int \mathrm{e}^{ax}\sin bx\mathrm{d}x = \frac{\mathrm{e}^{ax}}{a^2 + b^2} (a\sin bx - b\cos bx) + C$

91. $\int \mathrm{e}^{ax}\cos bx\mathrm{d}x = \frac{\mathrm{e}^{ax}}{a^2 + b^2}(a\cos bx + b\sin bx) + C$

## 十二、含有 $\ln x$ 的形式

92. $\int \ln x\mathrm{d}x = x(\ln x - 1) + C$

93. $\int \frac{\ln x}{\sqrt{x}}\mathrm{d}x = 4\sqrt{x} (\ln \sqrt{x} -1) + C$

94. $\int x\ln x\mathrm{d}x = \frac{x^2}{4} (2\ln x - 1) + C$

95. $\int x^{n}\ln x\mathrm{d}x = \frac{x^{n + 1}}{(n + 1)^{2}} [(n + 1)\ln x - 1] + C, n\neq -1$

96. $\int (\ln x)^2\mathrm{d}x = x[(\ln x)^2 - 2\ln x + 2] + C$

97. $\int (\ln x)^n\mathrm{d}x = x(\ln x)^n -n\int (\ln x)^{n - 1}\mathrm{d}x$

280

---

附录Ⅱ 积分表

98. $\int \sin (\ln x)\mathrm{d}x = \frac{x}{2}\left[\sin (\ln x) - \cos (\ln x)\right] + C$
99. $\int \cos (\ln x)\mathrm{d}x = \frac{x}{2} [\sin (\ln x) + \cos (\ln x)] + C$
100. $\int \ln (x + \sqrt{1 + x^2})\mathrm{d}x = x\ln (x + \sqrt{1 + x^2}) - \sqrt{1 + x^2} +C$

281
