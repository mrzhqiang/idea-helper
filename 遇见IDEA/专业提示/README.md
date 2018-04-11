# 专业提示
本指南针对的是已经熟悉基本功能，并希望了解更多信息的 IntelliJ IDEA 用户。如果你对 IntelliJ IDEA 还比较陌生，我们建议你先读一下 [探索][] 指南，再深入研究。

- [编码助手](#编码助手)
- [重构](#重构)
- [代码分析](#代码分析)
- [用户界面](#用户界面)
- [编辑器](#编辑器)
- [蚂蚁](#蚂蚁)
- [正则表达式](#正则表达式)
- [版本控制](#版本控制)
- [DCEVM](#DCEVM)
- [更新应用程序](#更新应用程序)
- [工具](#工具)


## 编码助手

### 类型信息
在插入符号时，想要了解更多信息，比如它来自哪里，它的类型是什么，那么 [Quick Documentation][] 可以提供帮助。通过 `Ctrl+Q` 快捷键，将出现展示这些信息的弹窗。如果不需要完整信息，那么就改用 **类型信息** ：它只显示选定表达式的类型，而不占用屏幕空间。

*——通常与 `Ctrl+B` 进行对比：直接跳转到类与方法的实现处，或变量的声明位置。*

### 区分大小写
默认情况下，IntelliJ IDEA 代码补全的大小写敏感性仅受键入的第一个字母影响（匹配首字母），可以在 **Settings/Preferences** 对话框（`Ctrl+Alt+S`）的 **Editor | General | Code Completion** 面板菜单中更改此策略，因此，可以让 IDE 对所有字母的大小写都敏感，或使其不受大小写影响，这取决于你的选择。

![code_completion](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/code_completion.png)

*温馨提示：如果你希望主动调用时才显示代码补全弹窗，你也可以在这个面板菜单中取消勾选 __Autopopup code completion__ 选项，这也是一种好的策略。*

### 禁用插入元素的高亮显示
讨论到关于默认设置，在学习 IntelliJ IDEA 的更多知识后，你可能想要修改它。那么不能错过 **Settings/Preferences** 对话框的 **Editor | General** 页面中 **Highlight usages of element at caret** 选项。如果你知道 `Ctrl+Shift+F7` 快捷键的作用，并且不喜欢每次光标移到插入符号上时，编辑器中的高亮显示都在变化，则不需要勾选此选项。

![highlight_usages_option](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/highlight_usages_option.png)

### 驼峰式
默认情况下，当你在编辑器中选择任何内容时，IntelliJ IDEA 对单词的大小写并不敏感。如果你喜欢根据 **驼峰式** 匹配选择内容，例如，只选择字符串的单词部分，你可以在 **Settings/Preferences** 对话框的 **Editor | General | Smart Keys** 面板菜单中勾选此选项。

![camelHumpsOption](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/camelHumpsOption.png)

### Hippie 完成
IntelliJ IDEA 通过 `Ctrl+Space`、`Ctrl+Shift+Space` 和 `Ctrl+Shift+Enter` 快捷键，提供 [Basic completion][]、[Smart completion][] 和 [Statement completion][] 功能。所有这些功能都是基于对代码结构的实际理解，但是，有时您可能需要一个更简单、但又灵活的逻辑，它会建议在当前文件中使用的单词，甚至是整个项目，而不考虑它们的上下文。此功能称为 [Hippie completion][]，可通过 `Alt+/` 激活。

![expandWord2](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/expandWord2.png)

![expandWord1](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/expandWord1.png)


## 重构

### 撤销重构
有了 IntelliJ IDEA，当你在重构代码时，不必担心任何后果，因为可以通过方便的 `Ctrl+Z` 快捷键，来 [undo][] 任何操作。

### 提取字符串片段
IntelliJ IDEA 不仅能够重构可执行代码，还可以重构字符串。选择字符串的任意片段，调用 *Extract* 将 变量、常量、字段、参数 提取为常量，并在代码中所有用到它的地方进行替换。

### 类型迁移
当你重构时，通常会重命名符号，或在代码中提取和移动语句。然而，重构不仅仅是这些。比如，[Type Migration][] （通过 `Ctrl+Shift+F6` 启用）让你更改 变量、字段、参数或方法返回值（int → String, int → Long, 等等） 等的类型，更新相关代码，并解决可能存在的冲突。

### 反转boolean
如果 IntelliJ IDEA 可以自动化类型迁移，为什么不用语义来做呢？要反转 `boolean` 符号的所有用法，只需要使用 [Invert Boolean refactoring][]。


## 代码分析

### 依赖结构矩阵
IntelliJ IDEA 可以分析代码中的组件的依赖关系，你需要密切关注这一点，因为当存在太多依赖关系时，它很可能会引发各种 [problems][]。[Dependency Structure Matrix action][] （通过 **Analyze |  Dependency Matrix** 菜单启用）将帮你可视化并探索模块、程序包和类之间的依赖关系。

![dsm](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/dsm.png)

尽管看起来复杂，但它其实是一款很容易使用的工具。只需要选择一个类或者包，然后查看它在哪里用，以及用了什么。

### 结构搜索和替换
[Structural Search and Replace, or SSR][] 是很强大的（在你学习了正确用法后），并且可以用于静态代码分析和重构自动化。简而言之，它允许你搜索代码中的特定模式，并用参数化模块替换它们。为此，它配备了自己的语言来定义代码模式，这在 [article][] 中有更详细的描述。

要访问此功能，请使用 **Edit | Find | Search/Replace Structurally...**。如果你想创建自己的模版或模式，打开 **Settings/Preferences** 对话框，点击 [Editor | Inspections][]，并在 General 节点下激活结构搜索检查。

![ssr_inspection](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/ssr_inspection.png)


## 用户界面

### 禁用 breadcrumbs 和 tag tree 突出显示
如果你打开大量的 HTML 和 XML 文件，并希望避免不必要的干扰，你可能需要在 [Editor | General | Appearance][] 中禁用 **HTML/XML tag tree** 以及在 **Editor | General | Breadcrumbs** 中禁用 **breadcrumbs** 的高亮显示。

### 禁用不必要的小图标
**Gutter 图标** 在编辑器栏的最左边，通常显示与代码关联的有用信息。有时，你如果感觉它是多余的，那么可以在 **Settings/Preferences** 对话框（`Ctrl+Alt+S`）中的 [Editor | General | Gutter Icons][]，去配置你想看到的图标。

### 禁用烦人的提示灯泡
还有一件可能令人讨厌的事情是，每当插入符号中有可用的信息时，编辑器中总是出现提示灯泡。禁用该功能有点麻烦：你需要手动编辑 **<Intelli IDEA preferences folder>/options/editor.xml** 文件，并添加下面的一行内容：

```
<option name="SHOW_INTENTION_BULB" value="false" />
```

### 任意搜索的使用
借助 [Search Everywhere][] （双击 `Shift` 触发），你可以找到任何地方的任意文本片段：比如在代码、库、界面、设置（通过 **#** 前缀）中搜索，甚至是操作名称。如果你经常使用这个功能，你可以在弹窗中，按下 `Enter` 来访问 IntelliJ IDEA 的设置开关，这是值得了解的功能。比如，我们在这里访问编辑器的设置：

![search_everywhere_settings](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/search_everywhere_settings.png)

如果你准备用 **#plugins** 搜索查询，那么你可以直接打开和关闭它们：

![search_everywhere_plugins](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/search_everywhere_plugins.png)

其他标签包括：**#appearance**，**#system**，**#inspections**，**#registry**，**#intentions**，**#templates** 和 **#vcs**。

另一个有趣的事实是，**Search Everywhere** 支持缩写。你可以用 **Settings/Preferences** 对话框中的 [Keymap page][] 为任何操作分配缩写文本，然后通过输入以下文字从 **Search Everywhere** 处调用这个功能：

![search_everywhere_abbreviation](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/search_everywhere_abbreviation.png)

### 隐藏编辑器标签
当你需要关闭除了当前标签之外的所有编辑器标签时，请按住 **Alt** 键并在当前标签上点击关闭图标 ![close1](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/close1.png)：

![close_others](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/close_others.png)

如果你不想看到所有的编辑器标签，跳到 **Settings/Preferences | Editor | General** 对话框的 [Editor Tabs][] 页面，然后在 **Placement** 下拉菜单中选择 **None**。

### 在新窗口中打开文件
一个不容易找到但却很方便的功能是，在 [Project Tool Window][] 中选择目标文件，然后按一下 `Shift+Enter` 快捷键，便会在新窗口中打开这个文件。

### 使用路径补全
路径补全可以帮你加快文件、目录等的选择。通常用于在 **Project Structure** 对话框中添加一个新的 SDK，或者指定应用程序服务的主目录。

当你开始输入路径时，按下 `Ctrl+Space` 快捷键去调用建议列表：

![completePath](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/completePath.png)

### 将停止和恢复按钮添加到工具栏
将 **Stop** ![stop](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/stop.gif) 和 **Resume** ![debug_resume](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/debug_resume.png) 按钮添加到 [Navigation Bar][] 的工具栏上可能会很方便，你可以通过 **Settings/Preferences** 对话框中的 [Appearance and Behavior | Menus and Toolbars][] 页面进行操作。

如果你更喜欢使用鼠标而不是键盘快捷键，这样你就不需要打开 **Debug** 工具窗口来管理当前的调试会话。

![buttons_on_navbar](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/buttons_on_navbar.png)


## 编辑器

### 与剪切板比较
IntelliJ IDEA 有一个用于代码、jar 文件、版本控制甚至平面图形的内置 Diff 查看器。要调出它，请先选择任意一对文件，然后按下 `Ctrl+D` 快捷键。

如果你选择的是单个文件，那么按下快捷键时， IDE 会提示你选择另一个要比较的文件。要快速比较活动编辑器和剪贴板中的内容，从菜单栏选择 **View | Compare with Clipboard** 即可。

### 历史粘贴
说到剪贴板，IntelliJ IDEA 会跟踪你放在剪切板里面的所有内容。任何时候你想粘贴一个以前复制过的项目，只需要按下 `Ctrl+Shift+V` 快捷键。

### 多选
[Multiple selection][] 是一个相对较新的非常强大的编辑器功能，它允许你立即进行快速选择和编辑多个（相邻或不相关）代码段。

简而言之，就是这样：你可以先从按下 `Alt+J` 快捷键开始（然后 IntelliJ IDEA 选择了一个插入符号），或者就像平时一样选择某些内容。

然后按 `Alt+J` 快捷键，IntelliJ IDEA 将向前搜索当前文件，直到它找到一段匹配的文本，并将其添加到已选择的内容中。您可以再按 `Alt+J` 一次继续前进，或用 `Shift+Alt+J` 返回选择，但请注意，当搜索到达文件末尾时，将从文件的开头重新开始搜索。

![multiselection1](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/multiselection1.png)

选择完成后，您可以开始编辑所有片段，就好像它们是一个个体。

*温馨提示：克隆插入符号的另一种方法是按两次 `Ctrl` （在 macOS 中是 `Alt`），然后用方向键或者鼠标，简单地向上/向下移动插入符号。*

### 蚂蚁
以防你不知道，[Emmet][] 是编写 HTML，XML 和 CSS 代码的好方法。IntelliJ IDEA 支持 [out of the box][]：只需编写 Emmet 表达式并按下 `Tab` 快捷键，即可展开它。

使用 Emmet 预览操作（可通过 **Find Action** 或 **Search Everywhere** - 因此请确保将其分配给便捷的快捷方式）可以得到一段代码的预览弹窗。

![emmet_preview](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/emmet_preview.png)

### 正则表达式
正则表达式功能强大且被广泛使用，但有时很难正确编写它们。IntelliJ IDEA 将帮助你检查代码中的任何正则表达式：只需在其中放入插入符号并按下 `Alt+Enter`快捷键，即可使用 [Check Regex][] 意图：

![check_regexp1](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/check_regexp1.png)

### 通过正则表达式组合查找及替换
IntelliJ IDEA 帮助 Regex 的另一个地方是 [Find and Replace feature][]。值得知道的是，它支持替换表达式中的捕获组。

![replaceText](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/replaceText.png)

查找和替换也可以让你从搜索中排除注释和文字：要做到这一点，请使用齿轮图标 ![](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/cogwheel_blue_no_arrow.png)。

### 字节码查看器
有时看到程序生成的实际字节码非常 [insightful][]。

在 IntelliJ IDEA 中，你始终可以通过 **View | Show Bytecode** 做到这一点。


## 版本控制

### 修订提交
在 [Commit Changes dialog][] 弹窗中，IntelliJ IDEA 提供执行各种操作的选项，其中之一是 **修订提交**，当你想要改动上次提交的内容，并将你当前的修改加入其中时，这是很有用的。

### 货架和补丁
*Shelves* 是一种类似于 [Git Stash][] 的 IDE 功能，但它适用于所有的 VCS：当你需要暂停当前工作，并从存储库中 pull 某些内容以便于尽快修复时，它会有所帮助，然后继续处理你正在进行的任何内容。该功能可以在不提交的情况下，处理本地更改的文件，因此不会再有丢失的改动或匆忙地进行合并提交。

有关更多细节，请参考此页面：[Git-Stash][] ，以及此部分：[Stashing and Unstashing][] 内容。

*Patches* 允许你将一系列更改保存到可通过电子邮件（或任意其他古老媒介）传输的文本文件中，然后应用于此代码。当你的飞机坠毁在一个荒岛上时，你很需要去 **commit** 某些内容，或者你在某种情况下使自己陷入没有可靠宽带连接的困境时，这将有很大的帮助。

有关更多细节，请参考：[Using Patches][] 部分。


## 调试

### 动作断点或方法断点
有时，你可能想要在特定的代码行上，评估某些东西，而没有真正停下来。你可以通过使用 [Method breakpoint][] 来完成这个操作。要创建一个方法断点，只需要在长按 `Shift` 时点击排水槽。

*——排水槽：即编辑器左侧的空栏*

![ij_breakpoint_action](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/ij_breakpoint_action.png)

这样，你可以在不改变代码的情况下，将任何表达式打印输出。这在调试库或远程应用程序时，特别有用。

### 字段断点或字段观察点
除了上面提到的动作断点外，你还可以使用 [Field watchpoints][]。当访问与其关联的字段时，这个断点将停止执行。要创建字段观察点，只需要长按 `Alt`（在 macOS 中是长按 `Ctrl+Cmd`）并点击排水槽即可。

![ij_breakpoint_field](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/ij_breakpoint_field.png)

### 对象标记
当在调试应用程序时，IntelliJ IDEA 允许你通过 [Mark Object][] 操作（可用于 [Evaluate Expression][]，[Variables][]，[Watches][] 视图菜单）来标记带有颜色标签的任意对象的特定实例，以便其更容易识别。

如果你有任何标记了标签的实例，你也可以在条件表达式中使用它：

![ij_breakpoint_debug_label](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/ij_breakpoint_debug_label.png)

### 自定义数据渲染器
[Evaluate Expression][]，[Variables][]，[Watches][] 和 [inline debugger][] 都使用标准的方式呈现变量值，主要基于类中的 **toString** 方法的实现。并不是每个人都知道，你可以为任何类定义自己的自定义渲染器。为此，请从 [Debug][] 工具窗口的上下文菜单中，选择 **Customize Data Views**。

![ij_type_renderer](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/ij_type_renderer.png)

当你使用的库中，某些类没有提供有意义的 **toString** 方法实现时，这是特别有用的，因此你可以在这个库外面，自己定义一个实现。

### 丢帧
如果你想在调试的时候“回到过去”，你可以通过 **Drop Frame** 操作来完成。如果你错误地走得太远，这是很大的帮助。这将不会恢复你的应用程序的全局状态，但至少能让你从帧堆中恢复过来。

### 强制返回
如果你想跳到未来，并强制从当前方法返回，而不执行其他任何指令，请使用 **Force Return** 操作（要调用它，请按下 `Ctrl+Shift+A` 并输入：**Force Return**）。如果这个方法返回一个值，那么你必须指定这个值。


## DCEVM
有时，当你快速修改代码时，你想立即看到它在一个工作中的应用程序里的表现。不幸的是，Java HotSwap 虚拟机有很多限制：比如，你不能为类添加新的方法或新的字段，并执行热交换；在热交换过程中，唯一可以改变的是方法体。

有关细节，请参考：[Altering the program's execution flow][] 和 [HotSwap][] 部分。

幸运的是，有一种方式可以用新的开源项目 **Dynamic Code Evolution VM** 来改善这种情况，这是对 **Java HotSwap** 虚拟机的修改，无条件支持运行时重新加载类。

在 IntelliJ IDEA 中通过专用 [plugin][] 来使用这个方式很简单。当你启用这个插件时，IDE 将为你提供下载适用于你的开发环境的 DCEVM JRE。然后，你必须在可选的 JRE 列表中选择它。


## 更新应用程序
如果你正在应用服务器上运行你的程序（例如，Tomcat，JBoss等等），你是否可以通过 `N/A` 来使用 **Update application** 操作重新加载已改变的类和资源？

*——这个功能只在 完全版 上有提供，并且好像是 JavaEE 工程才有更新的按钮。*

有关细节，请参考：[Updating Applications on Application Servers][]。


## 工具

### 外部工具
IntelliJ IDEA 有许多开发工具集成在一起，并可以直接使用。如果你需要的工具未集成，但你想通过快捷方式来使用它，请转到 **Settings/Preferences | Tools | [External Tools][]**，并配置如何运行此工具。然后，你就可以通过 **Tools | External Tools** 主菜单来运行这个工具。

请参考：[Configuring Third-Party Tools][] 部分。


# ——
**返回** [遇见IDEA][]

**下一步** [保持更新][]


[遇见IDEA]: https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/
[保持更新]: https://github.com/mrzhqiang/idea-helper/tree/master/遇见IDEA/保持更新

[探索]: https://github.com/mrzhqiang/idea-helper/tree/master/遇见IDEA/探索
[Quick Documentation]: https://www.jetbrains.com/help/idea/using-code-editor.html#quick_popups
[Basic completion]: https://www.jetbrains.com/help/idea/auto-completing-code.html#basic_completion
[Smart completion]: https://www.jetbrains.com/help/idea/auto-completing-code.html#smart_completion
[Statement completion]: https://www.jetbrains.com/help/idea/auto-completing-code.html#statements_completion
[Hippie completion]: https://www.jetbrains.com/help/idea/auto-completing-code.html#hippie_completion
[undo]: https://www.jetbrains.com/help/idea/using-code-editor.html#editor_code_selection
[Type Migration]: https://www.jetbrains.com/help/idea/type-migration.html
[Invert Boolean refactoring]: https://www.jetbrains.com/help/idea/invert-boolean-refactoring.html
[problems]: https://en.wikipedia.org/wiki/Coupling_(computer_programming)
[Dependency Structure Matrix action]: https://www.jetbrains.com/help/idea/dsm-analysis.html
[Structural Search and Replace, or SSR]: https://www.jetbrains.com/help/idea/structural-search-and-replace.html
[article]: https://www.jetbrains.com/idea/docs/ssr.pdf
[Editor | Inspections]: https://www.jetbrains.com/help/idea/inspections-settings.html
[Editor | General | Appearance]: https://www.jetbrains.com/help/idea/settings-editor-appearance.html
[Editor | General | Gutter Icons]: https://www.jetbrains.com/help/idea/settings-gutter-icons.html
[intention bulb]: https://www.jetbrains.com/help/idea/intention-actions.html
[Search Everywhere]: https://www.jetbrains.com/help/idea/searching-everywhere.html
[Keymap page]: https://www.jetbrains.com/help/idea/settings-keymap.html
[Editor Tabs]: https://www.jetbrains.com/help/idea/settings-editor-tabs.html
[Project Tool Window]: https://www.jetbrains.com/help/idea/project-tool-window.html
[Navigation Bar]: https://www.jetbrains.com/help/idea/navigation-bar.html
[Appearance and Behavior | Menus and Toolbars]: https://www.jetbrains.com/help/idea/menus-and-toolbars-appearance-settings.html
[Multiple selection]: https://www.jetbrains.com/help/idea/using-code-editor.html#edit_code
[Emmet]: http://emmet.io/
[out of the box]: https://www.jetbrains.com/help/idea/settings-emmet.html
[Check Regex]: https://www.jetbrains.com/help/idea/regular-expression-syntax-reference.html#check_regexp
[Find and Replace feature]: https://www.jetbrains.com/help/idea/finding-and-replacing-text-in-file.html
[insightful]: http://www.ibm.com/developerworks/library/it-haggar_bytecode/
[Commit Changes dialog]: https://www.jetbrains.com/help/idea/commit-changes-dialog.html
[Git Stash]: http://git-scm.com/book/en/v1/Git-Tools-Stashing
[Git-Stash]: http://git-scm.com/docs/git-stash
[Stashing and Unstashing]: https://www.jetbrains.com/help/idea/work-on-several-features-simultaneously.html
[Using Patches]: https://www.jetbrains.com/help/idea/using-patches.html
[Method breakpoint]: https://www.jetbrains.com/help/idea/using-breakpoints.html#method_breakpoint
[Field watchpoints]: https://www.jetbrains.com/help/idea/using-breakpoints.html#field_watchpoint
[Mark Object]: https://www.jetbrains.com/help/idea/setting-labels-to-variables-objects-and-watches.html
[Evaluate Expression]: https://www.jetbrains.com/help/idea/evaluate-expression.html
[Variables]: https://www.jetbrains.com/help/idea/debug-tool-window-variables.html
[Watches]: https://www.jetbrains.com/help/idea/debug-tool-window-watches.html
[inline debugger]: https://www.jetbrains.com/help/idea/inline-debugging.html
[Debug]: https://www.jetbrains.com/help/idea/debug-tool-window.html
[Altering the program's execution flow]: https://www.jetbrains.com/help/idea/altering-the-program-s-execution-flow.html#reload_classes
[HotSwap]: https://www.jetbrains.com/help/idea/debugger-hotswap.html
[plugin]: http://plugins.jetbrains.com/plugin/7245
[Updating Applications on Application Servers]: https://www.jetbrains.com/help/idea/updating-applications-on-application-servers.html
[External Tools]: https://www.jetbrains.com/help/idea/settings-tools-external-tools.html
[Configuring Third-Party Tools]: https://www.jetbrains.com/help/idea/configuring-third-party-tools.html
