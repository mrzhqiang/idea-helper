# 专业提示
本指南针对的是已经熟悉基本功能，并希望了解更多信息的 IntelliJ IDEA 用户。如果你对 IntelliJ IDEA 还比较陌生，我们建议你先读一下 [探索][] 指南，再深入研究。

- [编码助手](#编码助手)
- [重构](#重构)
- [代码分析](#代码分析)
- [用户界面](#用户界面)
- [编辑器](#编辑器)


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

## 编辑器

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
