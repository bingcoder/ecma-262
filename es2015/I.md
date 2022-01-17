# Ⅰ

## 介绍

这份标准定义了 ECMAScript 2015。它是 ECMAScript 语言规范的第6个版本。自从1997年第一个版本的发行，ECMAScript 已经成长为一个世界上最广泛使用的通用编程语言。它最广为认知的是作为 web 浏览器嵌入语言，它也广泛应用在服务端和嵌入式应用。自从1997年第一个版本发行以来，这对 ECMAScript 来说，第六个版本改变最多。

ECMAScript 2015 的目标包含了为大型应用提供更好的支持，库的创建和使用 ECMAScript 作为其他语言的编译目标。它的主要增加为模块化，类，块级作用域，迭代器，生成器，promise，解构，正确的尾调用。ECMAScript 内置库已经拓展支持额外的数据结构，包含  maps、sets、和二进制值数组另外字符串和正则里也支持 Unicode 补充字符。内置库现在通过子类继承。

ECMAScript 基于一些原有技术，其中最著名的是JavaScript（网景）和 JScript（微软）。Brendan Eich 在网景公司是发明了这门语言，它最初出现在在网景公司的 Navigator 2.0 浏览器上，在网景公司后来的浏览器和微软 IE 3.0 之后的所有浏览器上也都有它。

ECMAScript 语言规范的制定开始于1996年十一月，1997年六月第一版被 Ecma General Assembly 通过。

ECMAScript 标准在快速追踪程序下被提交给 ISO/IEC JTC 1，并在1998年四月通过作为国际标准 ISO/IEC 16262。为了和 ISO/IEC 16262 保持完全一致1998年六月 Ecma General Assembly 通过了第二版的标准，第二个版本比第一个只在编辑上有一些改动。

标准的第三个版本介绍了强大的正则表达式、更好的字符串处理方式、新的控制语句、try/catch 异常处理、更严格的错误定义。数字格式化输出和适应未来语言增长做的小改动。这一版标准在1999年十二月被 Ecma General Assembly 通过，在2002年六月发布为国际标准 ISO/IEC 16262:2002。

第三版标准发布之后，和 World Wide Web 联系起来的它被大量采用，它变成了一门基本上所有浏览器都支持的编程语言。一些有意义的工作被做去开发第四版 ECMAScript。然而那些工作并没有完成也没有作为第四版标准发布。但是这些工作中的一些被合并到了第六版标准的开发中了。

第五版ECMAScript 规范了许多在第三版 ECMASript 之后出现的被多数浏览器已经实现的新功能。这些功能包含属性访问器、reflective creation、属性检查、属性特性的程序控制、新增的数组处理函数、支持 JSON 对象编码格式、加强错误检查和程序安全的严格模式。2009年十二月Ecma General Assembly 通过了第五版ECMAScript。

第五版 ECMAScript 标准在快速追踪程序下被提交给 ISO/IEC JTC 1，并被通过作为国际标准 ISO/IEC 16262:2011。ECMAScript 标准5.1版本合并了一些小修正，它与 ISO/IEC 16262:2011 相同。2011年六月  Ecma General Assembly 通过了 5.1版本。

2009年开始重点开发第六个版本，第五个版本也正在准备发布。自1999年第三版发布以来，这是最重要的实验和语言加强设计，事实上第六版是十五年努力的结果。

代表许多组织的数十名个人在 Ecma TC39 中为本版本和之前版本的开发做出了非常重要的贡献。此外一个支持 TC39 的工作的充满活力的社区出现了，这个社区接受了数不清的草稿和数以千计的 bug 报告、执行实验、提供测试用例、培训全世界的开发者。不幸的是，很难确定每个人或组织做的贡献。

对于 ECMAScript 不断有新的用途和需求。第六版为常规，增量语言和库增强提供了基础。

Allen Wirfs-Brock
ECMA-262, 第六版编辑

2015年六月 General Assembly 通过了这一版的 Ecma 标准。

## 1 范围

该标准定义了 ECMAScript 2015 通用编程语言。

## 2 一致性

符合标准的 ECMAScript 实现必须提供和支持这份规范中所有的 types、value、objects、properties、functions、程序语法和语义描述。

符合标准的 ECMAScript 实现必须解释源文本输入和 Unicode 标准5.1.0版本或以后以及 ISO/1EC 10646 一致。

一个支持需要适应不同国家、不同语言的的人使用的语言和文化程序的应用程序界面的符合标准的 ECMAScript 实现必须实现定义在最新版的和这份规范兼容的 ECMA-402 里的接口。

符合标准的 ECMAScript 实现可以支持这份标准里没有描述的程序和正则语法。特别是，符合标准的 ECMAScript 实现可以支持使用本规范第 11.6.2.2 小节中列出的“未来保留字”的程序语法。

符合标准的 ECMAScript 实现不能实现第 16.1 小节中列出的 Forbidden Extension 里的任何一个扩展。

## 3 参考文献

对于这份文档的实施，下面这些引用文档是必需的。对于注明日期的参考文献，仅引用的版本适用。对于未注明日期的参考文献，适用于文献的最新版（包括任何修改）。

ISO/IEC 10646:2003: *Information Technology – Universal Multiple-Octet Coded Character Set (UCS) plus Amendment 1:2005, Amendment 2:2006, Amendment 3:2008, and Amendment 4:2008*, plus additional amendments and corrigenda, or successor

ECMA-402, *ECMAScript 2015 Internationalization API Specification*.
http://www.ecma-international.org/publications/standards/Ecma-402.htm

ECMA-404, *The JSON Data Interchange Format*.
http://www.ecma-international.org/publications/standards/Ecma-404.htm

## 4 概述

这章节包含了 ECMAScript 语言的非规范概述。

ECMAScript 是在宿主环境里执行计算和操作计算对象的面向对象语言。这里定义的ECMAScript 不是说要在计算上自给自足，实际上这份标准没有规定外部数据的输入和计算结果的输出。相反，希望 ECMAScript 程序的执行环境不仅提供规范中描述的对象和其他设施，也提供超出本标准规定的描述和行为的特定环境对象。except to 它们能提供某些被 ECMAScript 访问的属性和能被调用的方法。

ECMAScript 最初被设计作为脚本语言，但慢慢被广泛使用作为通用程序语言。脚本语言是用来操作、定制和自动处理现有系统设施的。在这样的系统里有用的程序已经可以通过用户界面使用，脚本语言是一个暴露这些功能给程序控制的机制。使用这种方式，这个现有系统被称为完成脚本语言能力提供对象和设备的宿主环境。脚本语言用来给专业和非专业程序员使用。

ECMAScript 最初被设计作为 Web 脚本语言，使浏览器里的网页生动和进行一部分基于 Web 的 B/S 模型的服务端计算。ECMAScript 现在被用作为不同宿主环境提供核心脚本功能，因此，此文档指定的是除了特定环境之外的语言核心。

ECMAScript 的使用已经超过简单的脚本，现在被用在许多不同环境和规模的编程任务。随着它使用的不断扩大，它的特性和功能也不断增加。ECMAScript 现在是通用编程语言。

ECMAScript 的一些功能像其他的一些语言，特别是 C、Java、Self、和Scheme，如下：

ISO/IEC 9899:1996, *Programming Languages – C*.

Gosling, James, Bill Joy and Guy Steele. *The Java™ Language Specification*. Addison Wesley Publishing Co., 1996.

Ungar, David, and Smith, Randall B. Self: The Power of Simplicity. *OOPSLA '87 Conference Proceedings*, pp. 227–241, Orlando, FL, October 1987.

*IEEE Standard for the Scheme Programming Language*. IEEE Std 1178-1990.



- object-oriented programming （OOP）
- host environment 宿主环境
- indeed 事实上、实际 adv
- external 外部的
- expected 预期的
- mechanism 机制
- capability  能力（ies）
- specify 指定
- apart from 除了
-  in particular尤其
- 