---
title: 从0开始的算法竞赛01-算法基础01：函数和递归
date: 2023-03-02
categories: [Algorithm, Basis]
tags: [algorithm, function, recursion] # lowercase
math: true
---
[![BY-SA](https://img.shields.io/badge/license-BY--SA-blue)](https://creativecommons.org/licenses/by-sa/4.0/) [![BMaC](https://img.shields.io/badge/support-Buy%20Me%20a%20Coffee-%23FFDD00?style=flat&logo=buymeacoffee)](https://www.buymeacoffee.com/zayn7lie) 

### WHY: 为什么要学递归？

- 首先我们先明确，算法其实是另外一种形式的数学 —— 它们解决问题的思路很相近，及通过一系列的计算得出结果。但是在计算机的帮助下，算法能干更多数学干起来很麻烦的事情 —— 一些重复、模板性的问题。
- 而递归，作为算法的第一课，便很好的体现出算法和数学的异同之处。递归，可以化简大量的重复性问题。因此学会递归，我们便可以利用计算机化简许多问题的运算过程。
- 可能不太好理解，没关系，我们先往下看看递归是什么。

### WHAT: 什么是递归？

- 我们先来看下这个函数公式：

$$
f(x) = 
\begin{cases}
0, & x \leq 7 \\
f(x - 1), & x > 7 \\
\end{cases}
$$

- 很显然，当 $x \leq 7$ 的时候 $f(x)$ 均等于0。但是当 $x = 10$ 的时候呢？
    - $f(10) = f(9) = f(8) = f(7) = 0$
    - 当 $x > 7$ 的时候有没有一种感觉，就是这个 $f(x)$ 的 $x$ 一直在 *传递* 到下一个 $f(x)$ ，只是自身每次减一？
    - 当 $x = 7$ 时， $f(x)$ return 0时候有没有一种感觉这个0在不断 *回归* 到 $f(10)$ ?
    - 这种 *传递* 和 *回归* 的感觉就叫做 *递归* 。或者说， *递归* = *传递* + *回归*
- 很多教材喜欢举一些很有趣但是对初学者很不友好的例子： *想要知道递归，就得先知道递归* ， *自己调用自己* 等等。但是经过我利用上面数学公式的举例，相信你能看得懂这些玩笑了。实际上，这些例子都是在强调 $f(x) = f(x - 1)$ 的过程。但这只是 *传递* 的过程。
- 另外，通过这里例子，我们还可以加深算法与数学异同的理解。数学遇到这种公式一般需要转化为其他公式（就想上面的展开 $f(10) = f(9) = f(8) = f(7) = 0$ 等等）再求解，这其实如果数据一大，公式一复杂，求解就会变得困难。而算法，正盼望着你把问题转化为这种 *自己调用自己* 形式，那剩下的求解呢？交给计算机就可以了。

### HOW: 递归怎么写？

- 递归分为传递和回归，传递就是往下的方式，回归就是限制条件回来的过程。很抽象，我们还是看刚刚那个公式：

$$
f(x) = 
\begin{cases}
0, & x \leq 7 \\
f(x - 1), & x > 7 \\
\end{cases}
$$

- 这里传递就是 $f(x) = f(x - 1)$ ，方式就是 $x$ 自己减一。
- 回归的限制条件是 $x \leq 7$ 。
- 如果这些都能理解，我再告诉你个条件。在程序函数中，是可以自己调用自己的，那即使你只学过我 *0基础c++体系-函数* 的第一节课应该可以写的出来这个函数：

```c++
int f(int x){
    if(x <= 7) return 0;
    if(x > 7) return f(x - 1);
}
```

- 这就是递归函数该怎么写。虽然这节课的内容较少，但是递归将伴随整个算法生涯，甚至后面递归我们不会再强调，而是把它当作一种和加减乘除一样常见的方法。所以希望本节课大家能好好理解。特别是注意写递归时不仅要有传递，还要有回归（限制条件要写清楚）。如果没有限制条件或者条件不当，程序将无限运行下去，知道内存超标。

[![BY-SA](https://img.shields.io/badge/license-BY--SA-blue)](https://creativecommons.org/licenses/by-sa/4.0/) [![BMaC](https://img.shields.io/badge/support-Buy%20Me%20a%20Coffee-%23FFDD00?style=flat&logo=buymeacoffee)](https://www.buymeacoffee.com/zayn7lie) 
