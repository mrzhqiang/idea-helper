---
layout: default
title: 探索
parent: 遇见
nav_order: 3
permalink: /meet/discover
---


# 探索
{: .no_toc }
原文：[Discover]

本指南旨在帮助您通过 IntelliJ IDEA 提供工作效率，并提供最重要功能以及提示、技巧和热键的概述。

## 目录
{: .no_toc .text-delta }

- TOC
{:toc}

---

## 用户界面
IntelliJ IDEA [Editor] 有许多特殊之处，最值得注意的是，你几乎可以在不离开它的情况下，调用几乎所有的 IDE 特性，这使得你可以组织布局，使其更多的屏幕空间，因为辅助控件是隐藏的，比如工具栏和窗口。

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/idea_editor_layout.png)

要打开一个工具窗口，可以通过它的快捷方式，将输入焦点移动到该窗口中，这样你就可以在它的上下文中，使用所有的键盘命令。当你需要回到编辑器时，请按下 `Escape` 键。

以下是一个常用工具窗口的快捷键列表：

| 工具窗口 | 快捷键 |
| :-:| :-:|
| 项目 | `Alt+1` |
| 版本控制 | `Alt+9` |
| 运行 | `Alt+4` |
| 调试 | `Alt+5` |
| 终端 | `Alt+F12` |
| 编辑器 | `Escape` |

*小提示：当你不知道某个操作的快捷键，尝试通过按下 `Ctrl+Shift+A` 快捷键来使用 __Find action__ 的功能，开始输入通过某个动作的名字来找到它，查看动作的快捷键或直接调用。*

当你想关注代码的时候，可以尝试 [Distraction Free Mode]。它移除了所有的工具栏、工具窗口和编辑选项卡。要切换到这个模式，在主菜单上选择 **View | Enter Distraction Free Mode**。

另一种方法是通过按下 `Ctrl+Shift+F12` 快捷键来隐藏所有的工具窗口。你可以再次按下这个快捷键恢复为默认布局。

[Navigation Bar] 是一个紧凑的 [Project Tool Window] 的替代品，要访问导航栏，请按下 `Alt+Home` 快捷键。

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_2.png)

IntelliJ IDEA 中的大多数组件（包括工具窗口和弹出窗口）都提供了 [speed search] 功能。此功能允许你过滤列表，或使用搜索查询导航到特定项目。

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_7.png)

想要知道更多详情，请参阅：[Guided Tour around the User Interface], [Editor basics] 和 [Working with Tool Windows].


## 编辑器基础
由于在 IntelliJ IDEA 中，你可以撤销重构，并从 [Local History] 中恢复改动，因此每次要求你保存更改是没有意义的。

最有用的编辑器快捷键是：

| 功能 | 快捷键（描述） |
| :-:| :-:|
| 移动当前的代码行 | `Ctrl+Shif+↑` `Ctrl+Shift+↓` |
| 复制代码行 | `Ctrl+D` |
| 删除代码行 | `Ctrl+Y`（事实上使用`Ctrl+X`更舒服） |
| 注释或取消注释代码行 | `Ctrl+/` |
| 注释或取消注释代码块 | `Ctrl+Shift+/` |
| 在当前打开的文件中查找 | `Ctrl+F` |
| 在当前文件中查找并替换 | `Ctrl+R` |
| 下一个查找结果 | `F3` |
| 上一个查找结果 | `Shift+F3` |
| 在打开的选项卡之间导航 | `Alt+←` `Alt+→` |
| 后退/前进导航 | `Ctrl+Alt+←` `Ctrl+Alt+→`（这作为光标的前后定位很舒服） |
| 展开或折叠编辑器中的代码块 | `Ctrl+-` `Ctrl++` |
| 创建新的... | `Alt+Insert` |
| 环绕着（代码块重构） | `Ctrl+Alt+T`（这实际上作为重构很好用） |
| 突出显示符号的用法 | `Ctrl+F7`（就是提供代码优化的建议） |

要扩展基于语法的选择，请按下 `Ctrl+W`，要收缩它，请按下 `Ctrl+Shift+W`。

*——比如要选择一个方法块，首先将光标置于方法块之中，然后按下快捷键即可。多次按下将扩展选择的空间，会从方法延伸到类，或者从方法内的 for 循环语句块延伸到方法块。*

IntelliJ IDEA 一次可以选择多个代码块，你可以通过 `Alt+J` 选择/取消任何一段代码块，或者通过点击代码选择并按下 `Shift+Alt+J`。

*——首先你要选择一段代码，通常你会对类、接口、枚举以及它们的属性和方法名字进行选择，然后按下快捷键，将自动选择多个相同的字符，这对重构来说很有帮助。*

了解更多细节，请参阅：[Editor basics]。


## 代码补全
当你通过按下 `Ctrl+空格` 快捷键访问 [Basic Completion] 时，可以获得有关变量、类型、方法、表达式等等的基本建议。当你调用 *Basic Completion* 两次时，它会显示更多结果，包括私有成员和非导入的静态成员。

*——很不幸的是，中文输入法，或者在整个 Windows 系统中，`Ctrl+空格` 这个快捷键，已被用于输入法的全局切换。要改变这一点，你将需要花费更多的精力在系统设置中。为了避免习惯上的改动，我们可以在 IntelliJ IDEA 的设置中，从 __keymap__ 模块搜索 __basic completion__，并为其增加快捷键 `Alt+B`。__B__ 取自 __Basic__，是为了防止 `Alt+C` 只响应 __Code__ 菜单。当然，你可以优先搜索其他的快捷键是否在 IntelliJ IDEA 中被占用，再决定增加那些你更习惯的快捷键组合。*

[Smart Completion] 功能可以感知预期的类型和数据流，并提供相关的上下文选项。要使用 *智能补全*，请按下 `Ctrl+Shift+Space` 快捷键。当你两次调用 *智能补全* 时，它会显示更多结果，包括链接。

*——抱歉的是，两次使用基础补全和智能补全，我都没有得到更多的结果！*

让 IntelliJ IDEA 为你完成一个语句，请按下 `Ctrl+Shift+Enter` 快捷键。[Statement Completion] 将自动添加缺失的括号、方括号、花括号以及必要的格式，比如分号 `;` 和空格间距。

如果你想查看任何方法（包括构造方法）的建议参数，请按下 `Ctr+P` 快捷键。IntelliJ IDEA 为每个重载的方法或构造函数显示参数信息，并突出显示已经键入的参数的最佳匹配。

使用 [Postfix Completion] 功能，可以根据你在小数点之后键入的后缀，将已经输入的表达式转换为另一种表达式。

*——后缀补全，用来避免拿起鼠标改变光标位置的情况。*

了解更多细节，请参阅：[Auto-Completing Code]。


## 导航

### 最近的文件
大多数时候你用的是一组有限的文件，并且需要在它们之间快速切换。这里真正节省时间的方法是一个称之为 *最近文件* 的操作，通过按下 `Ctrl+E` 快捷键来调用它。默认情况下，焦点在最后一个访问的文件上。请注意，你也可以通过此操作打开任何工具窗口：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_4.png)

导航到类：按 `Ctrl+N` 快捷键，支持复杂的表达式，导航到包括驼峰、路径、行等的中间名匹配。如果你两次调用它，将显示项目类别中的结果。

导航到文件：按 `Ctrl+Shift+N` 快捷键，仅用于文件和文件夹。要导航到文件夹，末尾要加上 `\` 字符。

导航到名称：按 `Ctrl+Shift+Alt+N` 快捷键，允许通过名字查找方法和字段。

### 结构
当你不在文件之间切换时，你很可能只在一个文件中导航。最简单的方法是按下 `Ctrl+F12` 快捷键。弹出一个窗口显示文件结构，并允许你快速导航到任何位置：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_5.png)

### 选择
如果你需要在一个特定的工具窗口（或取景器/浏览器）中打开一个文件，你可以通过 `选择输入` 操作来完成，请按下 `Alt+F1` 快捷键：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_6.png)

导航的快捷键包括：

| 功能 | 快捷键 |
| :-:| :-:|
| 全局搜索 | 双击`Shift` |
| 导航到类 | `Ctrl+N` |
| 导航到文件 | `Ctrl+Shift+N` |
| 导航到符号 | `Ctrl+Shift+Alt+N` |
| 最近的文档 | `Ctrl+E` |
| 文件结构 | `Ctrl+F12` |
| 选择 | `Alt+F1` |
| 导航到声明 | `Ctrl+B` |
| 导航到类型层次结构 | `Ctrl+H` |
| 显示UML弹窗 | `Ctrl+Alt+U`（这里的快捷键可能存在问题） |

了解更多细节，请参阅：[Navigating Through the Source Code.]


## 快捷弹出窗口
*快捷弹出窗口* 有助于检查与插入符号相关的附加信息，如果你想提高效率，下面列出了你应该知道的弹出窗口：

| 功能 | 快捷键 |
| :-:| :-:|
| API文档 | `Ctrl+Q` |
| 快速预览 | `Ctrl+Shift+I` |
| 显示使用情况 | `Ctrl+Alt+F7` |
| 显示实现情况 | `Ctrl+Alt+B` |

*小提示：快速弹出框可用于编辑器中的符号；但是，它们也可以通过相同的快捷方式在任何其他列表中使用。*


## 重构基础
IntelliJ IDEA 提供了一套全面的自动代码重构，在正确使用时可以显著提高生产力。首先，在应用重构之前，请不要选择任何东西。IntelliJ IDEA 非常聪明，能够确定要重构的语句，并且只有在可以进行多种选择的情况下，才会询问确认。

*小提示：要撤销最后一次的重构，请将焦点切换到 [Project Tool Window]，并按下 `Ctrl+Z` 快捷键。*

*小提示：一个真正的节省时间的能力是在 `Extract(提取)` 重构的帮助下提取部分字符串表达式的能力。 只需选择一个字符串片段并应用重构来将所选的片段用法替换为引入的常量或变量。*

| 功能 | 快捷键 |
| :-:| :-:|
| 重命名 | `Shift+F6`（有时，你需要解决其他相同名字的重命名，这在 IntelliJ IDEA 里很常见也很有效） |
| 提取变量 | `Ctrl+Alt+V`（通常在一个对象上使用，可以立即声明变量，并将此对象复制给所声明的变量） |
| 提取字段 | `Ctrl+Alt+F`（通常在一个局部对象声明上使用，可以立即转换类的字段） |
| 提取常量 | `Ctrl+Alt+C`（通常在字段、局部对象声明上使用，可以立即转为常量） |
| 提取方法 | `Ctrl+Alt+M`（通常在一段逻辑上使用，可以立即转为一个方法） |
| 提取参数 | `Ctrl+Alt+P`（通常在局部变量上使用，可以立即转为一个参数） |
| 内联 | `Ctrl+Alt+N`(暂时不知道用于什么地方） |
| 拷贝 | `F5` |
| 移动 | `F6` |
| 重构当前 | `Ctrl+Shift+Alt+T` |

了解更多细节，请参阅：[Refactoring Source Code]。


## 查找使用情况
**查找使用情况** 帮助你快速找到所有引用符号的代码片段（游标），无论符号是类、方法、字段、参数还是其他语句。只需要按下 `Alt+F7` 快捷键，就可以得到一个按使用类型、模块和文件分组的引用列表。

如果你想自定义查找使用情况的算法规则，请按下 `Ctrl+Shift+Alt+F7` 快捷键，或者点击右面侧板上的第一个按钮搜索结果。

*——上面有一个地方有错误，右面侧板实际上是左边的面板，需要有查找使用情况的结果，再从左边点击设置按钮自定义算法规则。*

如果你想要检索纯文本，请按下 `Ctrl+Shift+F` 来 **找到路径**。

了解更多细节，请参阅：[Finding Usages]。


## 检查
**检查** 是内置的静态代码分析工具，可帮助您查找可能的错误，找到死代码，检测性能问题并改进整体代码结构。

大多数检查不仅可以告诉你问题出在哪里，还可以立即提供快速解决方案。 按 `Alt + Enter` 选择一个快速修复。

当您对整个项目执行代码分析时，检查过于复杂而无法正常运行。 您可以通过以下两种方法之一完成此操作：从主菜单中选择 `Analyze | Inspect Code`，或选择 `Analyze| Run Inspection by Name` 以按名称运行检查。

请注意，虽然检查能为可能存在问题的代码提供快速修复，但意图可帮助您对代码进行自动更改，这是正确的。 要获取适用于插入代码的意向列表，请按 `Alt + Enter`。

了解更多细节，请参阅：[Code Inspection]。

*小提示：该编辑器可让您通过键盘快捷键快速导航突出显示的问题。 按 `F2` 进入下一个问题，按 `Shift + F2` 进入上一个问题。*

## 代码风格和格式
IntelliJ IDEA 会在您编辑时自动应用您在 [Code Style settings] 中配置的代码样式，并且在大多数情况下，您无需显式调用 *重新格式代码* 操作。

有用的格式化快捷键：

| 操作 | 快捷键 |
| :-:| :-:|
| 重新格式化代码 | `Ctrl+Alt+L` |
| 自动缩进行 | `Ctrl+Alt+I`（这里不知道具体作用） |
| 最佳化导入 | `Ctrl+Alt+O` |

请注意，默认情况下，IntelliJ IDEA 使用常规空格缩进而不是制表符。

如果您的文件有很多缩进，则可以通过在 [Java code style settings] 中启用 **Use tab character** 选项来优化其大小。

了解更多细节：请参阅：[Reformatting Source Code]。


## 版本控制基础
要检出版本控制系统（VCS）中的项目，请在 [Welcome Screen] 上或在主菜单的 VCS 中，点击 **版本控制检出** 。

要在当前文件、目录或整个项目上快速执行 VCS 操作，请按 `Alt + ~` 快捷键使用 [VCS operations pop-up]。

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refcard_3.png)

配置完VCS设置后，您将看到 [Version Control tool window]。 您可以随时按下 `Alt + 9` 进行切换。

**版本控制** 工具窗口的 [Local Changes] 选项卡显示本地更改：已启动和未启动。

*小提示：_注释_（可从快速列表，主菜单和上下文菜单中获得）允许您查看谁和何时更改了任何文件的一行代码。*

有用的 VCS 快捷键：

| 功能 | 快捷键 |
| :-:| :-:|
| 版本控制工具窗口 | `Alt+9` |
| VCS操作弹窗 | `Alt+~` |
| 提交改动 | `Ctrl+K` |
| 更新项目 | `Ctrl+T` |
| 推送提交 | `Ctrl+Shift+K` |

了解更多细节，请参阅：[Version Control with IntelliJ IDEA]。


### 分支
要在分支上执行操作，请从主菜单或上下文菜单中的 **VCS** 选择 **Branches**，弹出 **VCS操作弹窗** 或状态栏右侧的小部件。

请注意，对于多个存储库，IntelliJ IDEA 同时在所有分支上执行所有 VCS 操作，因此您无需手动在它们之间切换。

当您需要存储一些本地更改而不将它们提交到存储库时，[Shelves]，[stashes] 和 [patches] 可以帮助您。 然后，您可以切换到这些文件的存储库版本，然后再返回到您的更改。

了解更多细节，请参阅：[Manage branches]。


## 编译
默认情况下，IntelliJ IDEA 不会在保存时自动编译项目。 要编译项目，请从主菜单选择 `Build | Make Project `，或按 `Ctrl + F9`。

了解更多细节，请参阅：[Compiling Applications]。


## 运行和调试
一旦您从主菜单通过选择 `Run | Edit Configurations` 创建一个 [Run/Debug configuration]，你就可以开始运行和调试你的代码。

| 功能 | 快捷键 |
| :-:| :-:|
| 运行 | `Shift+F10` |
| 调试 | `Sfhit+F9` |

当在调试模式时，你可以通过使用 *Evaluate expression tool* 来 [evaluate any expression]，通过按 `Alt+F8` 快捷键可以访问它。该工具以与编辑器相同的方式提供代码完成，因此很容易输入任何表达式。

有时候，你可能想要进入一个特定的方法，但不是第一个将被调用的方法。在这种情况下，通过按 `Shift+F7` 选择特定的方法，使用 *智能进入*。

| 功能 | 快捷键 |
| :-:| :-:|
| 切换断点 | `Ctrl+F8` |
| 进入 | `F7` |
| 智能进入 | `Shift+F7` |
| 单步执行 | `F8` |
| 跳出 | `Shift+F8` |
| 重新开始 | `F9` |
| 评估表达 | `Alt+F8` |

如果你想在调试时“倒带”，你可以通过 *Drop Frame* 功能来完成。 如果你错误地走得太远，这特别有用。 这将不会恢复应用程序的全局状态，但至少会让您恢复到之前的堆栈帧。

*小提示：任何断点都可以在按住 `Alt` 键的同时单击排水槽来快速禁用。要更改断点详细信息（例如条件），请按 `Ctrl + Shift + F8`。*

了解更多细节，请参阅：[Running] 和 [Debugging]。

### 重新加载改动和热交换
有时，您需要在代码中插入较小的更改，而不需要关闭流程。由于 Java VM 有一个 HotSwap 功能，IntelliJ IDEA 在调用 **Make** 时自动处理这些情况。


## 应用服务器
将应用部署到服务器：

1. 通过选择 **File | Project Structure | Artifacts**（Maven 和 Gradle项目可以自动完成）来配置你的工件。
2. 通过点击 **Settings/Preferences** 对话框中的 **Application Servers** 页面来配置应用服务器。
3. 通过选择 **Run | Edit Configurations** 来配置一个运行配置，然后指定要部署的配件和它们的服务器。

通过选择 **Build | Build Artifacts**，你总是可以告诉 IntelliJ IDEA build/rebuild 你的构件（一旦它们被配置完毕）。

*小提示：当您需要将代码中的更改应用到正在运行的应用程序时，除了 Make，您可以通过按 `Ctrl + F10` 来使用更新操作。 此操作仅适用于分解的工件类型。 根据您的选择，它可以更新资源或更新班级和资源。 在调试模式下应用 Update 操作时，它使用 HotSwap; 否则，它使用 Hot 重新部署。*

了解更多细节，请参阅：[Working with Application Servers]。


## 使用构建工具
一旦你导入/创建了 Maven/Gradle 项目，你就可以直接在编辑器中编辑它的 `pom.xml` 或 `build.gradle` 文件。 最终需要与 IntelliJ IDEA 中的项目模型同步，才能对底层构建配置进行任何更改。

如果您希望 IDE 立即同步更改，请执行以下操作：

- 对于 `pom.xml`，在 `File | Settings | Build, Execution, Deployment | Build Tools | Maven | Importing`（Windows和Linux系统）或 `IntelliJ IDEA | Preferences | Build, Execution, Deployment | Build Tools | Maven | Importing`（maxOS系统）中，应用 `Import Maven projects automatically` 选项。
- 对于 `build.gradle`，在 `Build, Execution, Deployment | Build Tools | Gradle` 中，应用 `Use auto-import` 选项。

对于手动同步，请使用Maven / Gradle工具窗口的工具栏上相应操作：![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/image/refresh.png)。

请注意，任何目标或任务都可以附加在运行配置之前运行。

了解更多细节，请参阅：[Gradle]。


## 迁移
如果您正在考虑从 Eclipse 或 NetBeans 迁移到 IntelliJ IDEA 的可能性，请参阅 [Eclipse] 或 [NetBeans] 的迁移指南。


## 接下来
您可以观看 IntelliJ IDEA 概述的[快速视频]，了解 IntelliJ IDEA 在代码完成、检查、格式化等方面提供的内容。

有关更详细的信息，我们强烈建议您阅读文档。 另外，您可能会发现在 [Java SE] 下参考 Java 教程以及在 [Java EE] 上的教程也很有用。


# ——
**返回** [认识IDEA]

**下一步** [智能快捷键]


[认识IDEA]:https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/
[智能快捷键]:https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/智能快捷键/

[Editor]:https://www.jetbrains.com/help/idea/editor-basics.html
[Distraction Free Mode]:https://www.jetbrains.com/help/idea/intellij-idea-viewing-modes.html#distraction_free
[Navigation Bar]:https://www.jetbrains.com/help/idea/navigation-bar.html
[Project Tool Window]:https://www.jetbrains.com/help/idea/project-tool-window.html
[speed search]:https://www.jetbrains.com/help/idea/speed-search-in-the-tool-windows.html
[Guided Tour around the User Interface]:https://www.jetbrains.com/help/idea/guided-tour-around-the-user-interface.html
[Editor basics]:https://www.jetbrains.com/help/idea/editor-basics.html
[Working with Tool Windows]:https://www.jetbrains.com/help/idea/working-with-tool-windows.html
[Local History]:https://www.jetbrains.com/help/idea/local-history.html
[Editor basics]:https://www.jetbrains.com/help/idea/editor-basics.html
[Basic Completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#basic_completion
[Smart Completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#smart_completion
[Statement Completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#statements_completion
[Postfix Completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#postfix_completion
[Auto-Completing Code]:https://www.jetbrains.com/help/idea/auto-completing-code.html
[Navigating Through the Source Code.]:https://www.jetbrains.com/help/idea/navigating-through-the-source-code.html
[Project Tool Window]:https://www.jetbrains.com/help/idea/project-tool-window.html
[Refactoring Source Code]:https://www.jetbrains.com/help/idea/refactoring-source-code.html
[Finding Usages]:https://www.jetbrains.com/help/idea/finding-usages.html
[Code Inspection]:https://www.jetbrains.com/help/idea/code-inspection.html
[Code Style settings]:https://www.jetbrains.com/help/idea/code-style.html
[Java code style settings]:https://www.jetbrains.com/help/idea/code-style-java.html
[Reformatting Source Code]:https://www.jetbrains.com/help/idea/editor-basics.html#reformat_rearrange_code
[Welcome Screen]:https://www.jetbrains.com/help/idea/welcome-screen.html
[VCS operations pop-up]:https://www.jetbrains.com/help/idea/accessing-vcs-operations.html
[Version Control tool window]:https://www.jetbrains.com/help/idea/version-control-tool-window.html
[Local Changes]:https://www.jetbrains.com/help/idea/local-changes-tab.html
[Version Control with IntelliJ IDEA]:https://www.jetbrains.com/help/idea/version-control-with-intellij-idea.html
[Shelves]:https://www.jetbrains.com/help/idea/shelved-changes.html
[stashes]:https://www.jetbrains.com/help/idea/using-git-integration.html#stash
[patches]:https://www.jetbrains.com/help/idea/patches.html
[Manage branches]:https://www.jetbrains.com/help/idea/using-git-integration.html#manage-branches
[Compiling Applications]:https://www.jetbrains.com/help/idea/compiling-applications.html
[Run/Debug configuration]:https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html
[evaluate any expression]:https://www.jetbrains.com/help/idea/evaluating-expressions.html
[Running]:https://www.jetbrains.com/help/idea/running-applications.html
[Debugging]:https://www.jetbrains.com/help/idea/debugging.html
[Working with Application Servers]:https://www.jetbrains.com/help/idea/working-with-application-servers.html
[Gradle]:https://www.jetbrains.com/help/idea/gradle.html
[Eclipse]:https://www.jetbrains.com/help/idea/eclipse.html
[NetBeans]:https://www.jetbrains.com/help/idea/netbeans.html
[快速视频]:https://youtu.be/GSKERVTMWqs
[Java SE]:https://www.jetbrains.com/help/idea/java-se.html
[Java EE]:https://www.jetbrains.com/help/idea/developing-a-java-ee-application.html
