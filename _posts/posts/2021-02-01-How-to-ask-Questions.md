---
layout: post
title: 提问的方法
tags: For-Beginners
Author: Mark
---

本文由GitHub上的文章“提问的智慧” [[Link](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/main/README-zh_CN.md)] 节选&改编而来

### 简介

当你拋出一个技术问题时，最终是否能得到有用的回答，往往取决于你所提问和追问的方式。本指南将教你如何正确的提问以获得你满意的答案。

### 在提问之前

在你准备要通过提出技术问题前，请先做到以下事情：

1. 尝试在你准备提问的论坛的旧文章中搜索答案。
2. 尝试上网搜索以找到答案。
3. 尝试阅读教材以找到答案。
4. 尝试自己检查或试验以找到答案。
5. 向你身边的朋友打听以找到答案。
6. 尝试阅读源代码以找到答案。

当你提出问题的时候，请先表明你已经做了上述的努力；这将有助于树立你并不是一个不劳而获且浪费别人的时间的提问者。如果你能一并表达在做了上述努力的过程中所**学到**的东西会更好，因为我们更乐于回答那些表现出能从答案中学习的人的问题。

运用某些策略，比如先用 Google 搜索你所遇到的各种错误信息（搜索 [Google 论坛](http://groups.google.com/)和网页），这样很可能直接就找到了能解决问题的文件或邮件列表线索。即使没有结果，在邮件列表或新闻组寻求帮助时加上一句 `我在 Google 中搜过下列句子但没有找到什么有用的东西` 也是件好事，即使它只是表明了搜索引擎不能提供哪些帮助。这么做（加上搜索过的字串）也让遇到相似问题的其他人能被搜索引擎引导到你的提问来。

准备好你的问题，再将问题仔细的思考过一遍，因为草率的发问只能得到草率的回答，或者根本得不到任何答案。越是能表现出在寻求帮助前你为解决问题所付出的努力，你越有可能得到实质性的帮助。

### 使用有意义且描述明确的标题

在提问时，一个清晰明了的问题更加有机会被解答。不要用喋喋不休的`帮帮忙`、`跪求`、`急`（更别说`救命啊！！！！`这样让人反感的话，用这种标题会被条件反射式地忽略）来浪费这个机会。不要妄想用你的痛苦程度来打动我们，而应该是在这点空间中使用极简单扼要的描述方式来提出问题。

一个好标题范例是`目标 —— 差异`式的描述，许多技术支持组织就是这样做的。在`目标`部分指出是哪一个或哪一组东西有问题，在`差异`部分则描述与期望的行为不一致的地方。

> 反面例子：我的程序就是跑不通啊！！！！怎么办，能帮忙看看吗？求救求救！！
>
> 正确例子：Java用`==`比较"a"和"a"的时候为什么会返回`false`？

### 精确地描述问题并言之有物

- 仔细、清楚地描述你的问题或 Bug 的症状。
- 描述问题发生的环境（机器配置、操作系统、应用程序、以及相关的信息）
- 描述在提问前你是怎样去研究和理解这个问题的。
- 描述在提问前为确定问题而采取的诊断步骤。
- 描述最近做过什么可能相关的硬件或软件变更。
- 尽可能的提供一个可以`重现这个问题的可控环境`的方法。

当你报告的是你认为可能在代码中的问题时，给大家一个可以重现你的问题的环境尤其重要。当你这么做时，你得到有效的回答的机会和速度都会大大的提升。

### 话不在多而在精

你需要提供精确有内容的信息。这并不是要求你简单的把成堆的出错代码或者资料完全转录到你的提问中。如果你有庞大而复杂的测试样例能重现程序挂掉的情境，尽量将它剪裁得越小越好。

这样做的用处至少有三点。 

第一，表现出你为简化问题付出了努力，这可以使你得到回答的机会增加

第二，简化问题使你更有可能得到**有用**的答案

第三，在精炼你的 bug 报告的过程中，你很可能就自己找到了解决方法或权宜之计。

> 例子：
>
> 某Java代码出现bug，源代码大概有200行
>
> ```java
> import java.io.*;
> // ... 
> class Example{
>     public static void main(String[] args){
>         String str1 = "a";
>         //...
>         if (str1 == "a"){
>             // Do Something...
>         }
>         //...
>     }
> }
> ```
>
> 你发现这个代码就是跑不通，于是开始测试，最后你发现这个代码片段里面的东西无论什么时候都没运行
>
> ```java
> if (str1 == "a"){
>     // Do Something ...
> }
> ```
>
> 考虑到 `if` 的特性，你决定通过打印结果的方式看看 `str1=="a"` 是不是`true`，发现就算
>
> ```java
> String str1 = "a";
> System.out.println(str1 == "a");
> ```
>
> 打印出来的也是`false`
>
> 
>
> （如果你没有在网络或者课本里面找到答案）在提问时，你应该这样提问：
>
> *为什么Java代码中 `"a" == "a"` 会返回 `false`？*

### 低声下气不能代替你的功课

有些人明白他们不该粗鲁或傲慢的提问并要求得到答复，但他们选择另一个极端 —— 低声下气：`我知道我只是个可悲的新手，一个撸瑟，但...`。这既使人困扰，也没有用，尤其是伴随着与实际问题含糊不清的描述时更令人反感。



### 别动辄声称找到 Bug

当你在使用软件中遇到问题，除非你非常、**非常**的有根据，不要动辄声称找到了 Bug。提示：除非你能提供解决问题的源代码补丁，或者提供回归测试来表明前一版本中行为不正确，否则你都多半不够完全确信。这同样适用在网页和文件，如果你（声称）发现了文件的`Bug`，你应该能提供相应位置的修正或替代文件。

> 反面例子：
>
> “我的Java出bug了！连 `"a"=="a"` 都返回`false` !



### 询问代码相关的问题时……

别要求他人帮你调试有问题的代码，不提示一下应该从何入手。张贴几百行的代码，然后说一声：`它不能工作`会让你完全被忽略。只贴几十行代码，然后说一句：`在第七行以后，我期待它显示 <x>，但实际出现的是 <y>`比较有可能让你得到回应。



### 如果还是搞不懂

如果你看不懂回应，别立刻要求对方解释。像你以前试着自己解决问题时那样（利用手册，FAQ，网络，身边的高手），先试着去搞懂他的回应。如果你真的需要对方解释，记得表现出你已经从中学到了点什么。

比方说，如果我回答你：`你不应该用==比较字符串类型，因为==是直接比较内存地址的，应该用equal()`，然后，这是一个**很糟的**后续问题回应：`内存地址是啥？` **好**的问法（在大概了解了内存地址是什么以后）应该是这样：`为什么相同的字符串内存地址不一样？如果存在两个一样的内容，内存地址一样的话应该更加省空间啊？`