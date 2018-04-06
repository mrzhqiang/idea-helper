# 专业提示
本指南针对的是已经熟悉基本功能，并希望了解更多信息的 IntelliJ IDEA 用户。如果你对 IntelliJ IDEA 还比较陌生，我们建议你先读一下 [探索][] 指南，再深入研究。

- [编码助手](#编码助手)
- [重构](#重构)
- [代码分析](#代码分析)


## 编码助手

### 类型信息
在插入符号时，想要了解更多信息，比如它来自哪里，它的类型是什么，那么 [Quick Documentation][] 可以提供帮助。通过 `Ctrl+Q` 快捷键，将出现展示这些信息的弹窗。如果不需要完整信息，那么就改用 **类型信息** ：它只显示选定表达式的类型，而不占用屏幕空间。

*——通常与 `Ctrl+B` 进行对比：直接跳转到类与方法的实现处，或变量的声明位置。*

### 区分大小写
默认情况下，IntelliJ IDEA 代码补全的大小写敏感性仅受键入的第一个字母影响（匹配首字母），可以在 **Settings/Preferences** 对话框（`Ctrl+Alt+S`）的 **Editor | General | Code Completion** 面板菜单中更改此策略，因此，可以让 IDE 对所有字母都敏感（匹配单词），或使其都不敏感（匹配所有字母），这取决于你的选择。

![code_completion](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/code_completion.png)

*温馨提示：在这个面板菜单中，如果你希望以主动方式显示代码补全弹窗，你也可以取消勾选 __Autopopup code completion__ 选项，这也是一种好的策略。*

### 禁用在插入符号处突出显示元素的用法
讨论到关于默认设置，在学习 IntelliJ IDEA 的更多知识后，你可能想要修改它。那么不能错过 **Settings/Preferences** 对话框的 **Editor | General** 页面中 **Highlight usages of element at caret** 选项。如果你知道 `Ctrl+Shift+F7` 快捷键，并且不喜欢在每次简单移动插入符号时，编辑器中的高亮显示都在出现和消失，则不需要勾选此选项。

![highlight_usages_option](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/专业提示/image/highlight_usages_option.png)

### 驼峰式
默认情况下，当你在编辑器中选择任何内容时，IntelliJ IDEA 对单词的大小写并不敏感。如果你喜欢根据 **驼峰式** 匹配选择单词，例如，只选择单词的一部分，你可以在 **Settings/Preferences** 对话框的 **Editor | General | Smart Keys** 面板菜单中勾选此选项。

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
如果 IntelliJ IDEA 可以自动化类型迁移，为什么不用语义做同样的事情呢？要反转 `boolean` 符号的所有用法，只需要使用 [Invert Boolean refactoring][]。


## 代码分析

### 依赖关系结构矩阵
IntelliJ IDEA 让你分析代码中的组件是如何互相依赖的，你需要密切关注这一点，因为存在太多依赖关系时，它很可能会引发各种 [problems][]。


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
