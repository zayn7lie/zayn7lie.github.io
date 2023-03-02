---
title: 从0开始的算法竞赛-01算法基础00：你真的会分析算法问题吗？
date: 2023-03-02 # +/-TTTT
categories: [Algorithm, Basis]
tags: [blog, template] # lowercase
math: true
---
[![BY-SA](https://img.shields.io/badge/license-BY--SA-blue)](https://creativecommons.org/licenses/by-sa/2.0/) [![BMaC](https://img.shields.io/badge/support-Buy%20Me%20a%20Coffee-%23FFDD00?style=flat&logo=buymeacoffee)](https://www.buymeacoffee.com/zayn7lie) 

### WHY: 为什么要分析算法问题？我怎么知道我是分析还是凭感觉？

- 如果你真的有这种疑惑，那么你大概率平时是靠感觉解决问题的 —— 我并不是说我们并不能靠感觉解决问题的，且凭感觉解决问题也是很重要的一项技能（凭感觉解决问题其实并不是什么不好的方式，其实就是第六感），凭感觉有着速度快、和经验正相关的精准等优点。但是作为理科竞赛，我更希望凭感觉少些，分析的成分多些。这样在你一些从没有遇到类型的问题你也可以得出正确答案。

### WHAT: 什么是凭感觉？什么是靠分析？

- 凭感觉准确是指一眼看题目便能不经过任何考虑便知道怎么解决，一个很简单的例子就是 *7 * 7 = ？* ，你能够直接回答出乘法口诀表七七四十九。而不是分析：拆分成7个7进行相加。这就是我对凭感觉的定义。另外一个突出的例子就是网上各大媒体流传的《秒杀高考/中考题目》的各种技巧。很显然，凭感觉的最突出优点就是快。但是当问题复杂时（条件不足、没有见到）很容易就没法得出正确答案。
- 分析就是形成一套万能的体系机器，无论是什么问题输入机器后通过机器内的逻辑加工都能的出正确答案。例如我在写每一章知识时都将知识拆分成 *WHY WHAT HOW* ，这便是 *分析* 中的 *拆分* 。当然，因为它的通用性导致它的速度肯定不如凭感觉。但是它是最稳定的正确答案输出器，且符合理科竞赛的靠逻辑本质。所以我将在本章详细将如何分析一个算法题目。

### HOW: 怎么分析一道理科题目？

- 首先，一道理科题目一般由这几个部分组成： *背景 主体 数据 样例* 。 我们来看这个样例：

```txt
Farmer John(FJ) 的奶牛很喜欢学习，他们看到FJ学了编程也想参与其中，但是在阅读编程书籍的时候出现了问题。

这本编程书籍一上来就要求编译一个程序计算 a + b 的值。但是他们才第一天学，什么都不知道。请问你可以帮助他们写一个样例吗做个示范吗？

输入一行a和b，用空格隔开。
输出一行，输出 a + b 的值。

样例：输入：1 1 输出：2

数据范围：0 < a, b < 10^9
```


[![BY-SA](https://img.shields.io/badge/license-BY--SA-blue)](https://creativecommons.org/licenses/by-sa/2.0/) [![BMaC](https://img.shields.io/badge/support-Buy%20Me%20a%20Coffee-%23FFDD00?style=flat&logo=buymeacoffee)](https://www.buymeacoffee.com/zayn7lie) 
