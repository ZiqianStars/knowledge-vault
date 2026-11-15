---
tags:
  - C++
  - MSVC
  - 文档地图
created: "2026-10-19"
status: 已整理
source:
  平台: Microsoft Learn（中文版）
  标题: C++ / Visual Studio 中的 C++ 文档
  版本: view=msvc-170（Visual Studio 2022 工具集）
  链接: https://learn.microsoft.com/zh-cn/cpp/cpp/?view=msvc-170
  抓取日期: 2026-10-19
---

# MSVC C++ 文档总览

> 原文：[https://learn.microsoft.com/zh-cn/cpp/cpp/?view=msvc-170](https://learn.microsoft.com/zh-cn/cpp/cpp/?view=msvc-170)

## 一句话概括

> 这个网址是 **MSVC C++ 文档的顶层入口**（同时也是「C++ 语言参考」的落地页），它本身几乎不含正文——它是一个**目录索引**，把 Visual Studio 2022 工具集下与 C++ 有关的几百篇文档，按五个板块组织起来：入门、新变化、编译器工具链、语言核心、标准库。

## 核心内容

### 一、文档的五个板块

原始网页自上而下就是这五块，每一块下面挂着若干代表条目：

| 板块 | 解决什么问题 | 代表条目 |
| --- | --- | --- |
| **1. 在 Visual Studio 中学习 C++** | 从零装到跑通第一个程序 | [安装 C/C++ 支持](https://learn.microsoft.com/zh-cn/cpp/build/vscpp-step-0-installation?view=msvc-170) · [Hello World](https://learn.microsoft.com/zh-cn/cpp/build/vscpp-step-1-create?view=msvc-170) · [控制台计算器](https://learn.microsoft.com/zh-cn/cpp/get-started/tutorial-console-cpp?view=msvc-170) · [视频系列](https://learn.microsoft.com/zh-cn/shows/cplusplus-language-library) |
| **2. Visual Studio 中的 C++ 新变化** | 版本升级后该看什么 | [Visual Studio 中的新变化](https://learn.microsoft.com/zh-cn/cpp/overview/what-s-new-for-visual-cpp-in-visual-studio?view=msvc-170) · [C++ 的符合性改进](https://learn.microsoft.com/zh-cn/cpp/overview/cpp-conformance-improvements?view=msvc-170) · [支持的平台](https://learn.microsoft.com/zh-cn/cpp/overview/supported-platforms-visual-cpp?view=msvc-170) |
| **3. 使用编译器和工具** | 编译、链接、构建、报错 | [生成参考](https://learn.microsoft.com/zh-cn/cpp/build/reference/c-cpp-building-reference?view=msvc-170) · [编译器参考](https://learn.microsoft.com/zh-cn/cpp/build/reference/compiling-a-c-cpp-program?view=msvc-170) · [链接器参考](https://learn.microsoft.com/zh-cn/cpp/build/reference/linking?view=msvc-170) · [错误和警告](https://learn.microsoft.com/zh-cn/cpp/error-messages/compiler-errors-1/c-cpp-build-errors?view=msvc-170) |
| **4. C++ 语言** | 语言本身，即「这个网址真正的主角」 | [语言参考](https://learn.microsoft.com/zh-cn/cpp/cpp/cpp-language-reference?view=msvc-170) · [关键字](https://learn.microsoft.com/zh-cn/cpp/cpp/keywords-cpp?view=msvc-170) · [运算符](https://learn.microsoft.com/zh-cn/cpp/cpp/cpp-built-in-operators-precedence-and-associativity?view=msvc-170) · [预处理器](https://learn.microsoft.com/zh-cn/cpp/preprocessor/c-cpp-preprocessor-reference?view=msvc-170) |
| **5. C++ 标准库 (STL)** | 标准库各组件的用法 | [标准库概述](https://learn.microsoft.com/zh-cn/cpp/standard-library/cpp-standard-library-overview?view=msvc-170) · [按头文件索引](https://learn.microsoft.com/zh-cn/cpp/standard-library/cpp-standard-library-header-files?view=msvc-170) · [容器](https://learn.microsoft.com/zh-cn/cpp/standard-library/stl-containers?view=msvc-170) · [迭代器](https://learn.microsoft.com/zh-cn/cpp/standard-library/iterators?view=msvc-170) · [算法](https://learn.microsoft.com/zh-cn/cpp/standard-library/algorithms?view=msvc-170) · [分配器](https://learn.microsoft.com/zh-cn/cpp/standard-library/allocators?view=msvc-170) · [函数对象](https://learn.microsoft.com/zh-cn/cpp/standard-library/function-objects-in-the-stl?view=msvc-170) · [iostream](https://learn.microsoft.com/zh-cn/cpp/standard-library/iostream-programming?view=msvc-170) · [正则](https://learn.microsoft.com/zh-cn/cpp/standard-library/regular-expressions-cpp?view=msvc-170) · [文件系统](https://learn.microsoft.com/zh-cn/cpp/standard-library/file-system-navigation?view=msvc-170) |

### 二、板块 4「C++ 语言参考」的完整章节脉络

这是最有价值的一支。原文声明其结构**照着两本经典著作排**：Margaret Ellis 与 Bjarne Stroustrup 的《C++ 参考手册批注》（ARM），以及 ISO/IEC 14882 国际标准。所以章节顺序本质上是「标准委员会的视角」：

| 章节 | 内容 | 页面 |
| --- | --- | --- |
| 词法约定 | 标记、注释、运算符、关键字、标点、字面量、文件转换 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/lexical-conventions?view=msvc-170) |
| 基本概念 | 作用域、链接性、程序启动与终止、存储类、类型 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/basic-concepts-cpp?view=msvc-170) |
| 内置类型 | 编译器内建的基本类型及其值范围 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/fundamental-types-cpp?view=msvc-170) |
| 标准转换 | 内置类型之间的转换；算术转换；指针/引用/成员指针转换 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/standard-conversions?view=msvc-170) |
| 声明和定义 | 变量、类型、函数的声明与定义 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/declarations-and-definitions-cpp?view=msvc-170) |
| 运算符、优先级和关联性 | 全部内置运算符及其优先级级别 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/cpp-built-in-operators-precedence-and-associativity?view=msvc-170) |
| 表达式 | 表达式类型与语义、强制转换运算符、RTTI | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/expressions-cpp?view=msvc-170) |
| Lambda 表达式 | 隐式定义函数对象类并构造其对象的编程技术 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/lambda-expressions-in-cpp?view=msvc-170) |
| 语句 | 表达式/空/复合/选择/迭代/跳转/声明语句 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/statements-cpp?view=msvc-170) |
| 类和结构 | 特殊成员函数、数据成员、位域、`this` 指针、嵌套类 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/classes-and-structs-cpp?view=msvc-170) |
| 联合 | 所有成员共享同一内存位置的用户定义类型 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/unions?view=msvc-170) |
| 派生类 | 单继承/多继承、虚函数、抽象类、作用域规则、`__super`、`__interface` | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/inheritance-cpp?view=msvc-170) |
| 成员访问控制 | `public`/`private`/`protected`、友元函数与友元类 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/member-access-control-cpp?view=msvc-170) |
| 重载 | 运算符重载及其规则 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/operator-overloading?view=msvc-170) |
| 异常处理 | C++ 异常处理、结构化异常处理 (SEH) | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/exception-handling-in-visual-cpp?view=msvc-170) |
| 断言和用户提供的消息 | `#error` 指令、`static_assert`、`assert` 宏 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/assertion-and-user-supplied-messages-cpp?view=msvc-170) |
| 模板 | 模板规范、函数模板、类模板、`typename`、模板与智能指针 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/templates-cpp?view=msvc-170) |
| 事件处理 | 声明事件与事件处理程序（MS 扩展） | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/event-handling?view=msvc-170) |
| Microsoft 专用修饰符 | 内存寻址、调用约定、`naked` 函数、`__declspec`、`__w64` | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/microsoft-specific-modifiers?view=msvc-170) |
| 内联汇编程序 | 在 `__asm` 块中混写汇编与 C++ | [链接](https://learn.microsoft.com/zh-cn/cpp/assembler/inline/inline-assembler?view=msvc-170) |
| 编译器 COM 支持 | 支持 COM 类型的 MS 专用类与全局函数 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/compiler-com-support?view=msvc-170) |
| Microsoft 扩展 | MS 对 C++ 的全部扩展 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/microsoft-extensions?view=msvc-170) |
| 非标准行为 | MSVC 与标准不一致之处 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/nonstandard-behavior?view=msvc-170) |
| 欢迎回到 C++ | 现代 C++ 编程实践总纲 | [链接](https://learn.microsoft.com/zh-cn/cpp/cpp/welcome-back-to-cpp-modern-cpp?view=msvc-170) |

相邻支路的入口也在这页给出：[C 语言参考](https://learn.microsoft.com/zh-cn/cpp/c-language/c-language-reference?view=msvc-170) · [预处理器参考](https://learn.microsoft.com/zh-cn/cpp/preprocessor/c-cpp-preprocessor-reference?view=msvc-170) · [生成参考](https://learn.microsoft.com/zh-cn/cpp/build/reference/c-cpp-building-reference?view=msvc-170) · [Visual C++ 库](https://learn.microsoft.com/zh-cn/cpp/standard-library/cpp-standard-library-reference?view=msvc-170)

### 三、这套文档的两个隐含前提

1. **它是给 MSVC 用户看的，不是给标准委员会看的。** 参差排在中间的「事件处理」「编译器 COM 支持」「Microsoft 扩展 / 专用修饰符」三章，在 GCC/Clang 上根本不存在。要移植代码，这三章必须先看。
2. **很多东西由开关决定，而不是由编译器版本决定。** `/std`、`/permissive-`、`/Za` 三个选项会实质改变语言语义（例如运算符的替代拼写 `and`/`or` 到底算不算关键字）。看 MSVC 文档时，必须同时知道自己的编译选项是哪一套。

## 我的理解

- **这个页面最大的用途是「定位」，不是「学习」。** 指望从这一页学到什么 C++ 知识会失望——它的价值在于，当你遇到一个 MSVC 特有的报错或 `__` 开头的关键字时，能在 30 秒内找到唯一权威的那篇文档。所以我把它做成了链接表而不是知识笔记。
- **真正值得离线留存的只有三类东西**：全表的优先级表、全表的关键字清单、MSVC 的确切类型大小。这三样每次查都要翻页，且不会变，已经各自落成 [[03-C++关键字速查]]、[[04-运算符优先级与结合性]]、[[05-内置类型与大小]]。其余内容随用随查在线版即可——在线版永远更新得快。
- **章节顺序暴露了文档的老底子。** 「词法 → 基本概念 → 内置类型 → 转换 → 声明 → 运算符 → 表达式 → 语句 → 类 → 派生类 → 访问控制 → 重载」这条线，和 Bjarne 本人在 ARM 里的排法一致。这意味着它**不适合作为学习路径**（从词法约定开始啃的人基本都放弃了），只适合查阅。**要学现代写法，从 [[02-现代C++十二条要义]] 那篇入手，而不是从头滚这份目录。**
- **一个容易被忽略的细节**：文档反复强调 C++ 「向后兼容 C」，并专门设置了「Microsoft 扩展」「非标准行为」两章来兜住历史包袱。换句话说，**MSVC 默认开启的是「带扩展的兼容模式」，不是「标准模式」**。要写可移植代码，`/permissive-` 基本是必开的——这一点官方文档分散在十几个页面里，这里把它明确记下来。

## 值得追问的问题

- `/permissive-` 和 `/Za` 都叫「关闭语言扩展」，两者差别具体在哪？MSVC 官方为什么不合并它们？
- `long double` 在 MSVC 下与 `double` 完全相同（8 字节），在 Linux/gcc 下却是 80 位扩展精度。跨平台浮点数值不一致的 bug 如何从这里产生？
- 文档说 `asm` 关键字「保留了以便兼容，但未成功」——具体失败在哪里？
- C++20 的 `char8_t`、`concept`、`consteval` 等在 MSVC 里需要 `/std:c++20`；为什么部分特性在 `/std:c++latest` 下才可用？

## 关联

- [[00-C++]] —— 本主题索引
- [[02-现代C++十二条要义]] —— 同一入口下「欢迎回到 C++」支路的展开
- [[03-C++关键字速查]] · [[04-运算符优先级与结合性]] · [[05-内置类型与大小]] —— 三条已落地的速查表
