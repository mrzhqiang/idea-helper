[认识IDEA]:https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/
[专业建议]:https://github.com/mrzhqiang/idea-helper/tree/master/认识IDEA/专业建议/

[possible conflicts]:https://www.jetbrains.com/help/idea/configuring-keyboard-and-mouse-shortcuts.html#shortcut_conflicts
[predefined keymap]:https://www.jetbrains.com/help/idea/configuring-keyboard-shortcuts.html#predefined
[modify a copy]:https://www.jetbrains.com/help/idea/configuring-keyboard-shortcuts.html#configure
[transfer it to your installation]:https://www.jetbrains.com/help/idea/configuring-keyboard-shortcuts.html#user_defined_keymap_storage
[Find Action]:https://www.jetbrains.com/help/idea/navigating-to-action.html
[Key Promoter X]:https://plugins.jetbrains.com/plugin/9792-key-promoter-x
[default keymap reference card]:https://resources.jetbrains.com/storage/products/intellij-idea/docs/IntelliJIDEA_ReferenceCard.pdf
[Keyboard Shortcuts and Mouse Reference]:https://www.jetbrains.com/help/idea/keyboard-shortcuts-and-mouse-reference.html
[Find class, file, or symbol]:https://www.jetbrains.com/help/idea/navigating-to-class-file-or-symbol-by-name.html
[View recent files]:https://www.jetbrains.com/help/idea/navigating-to-recent.html
[Show intention actions]:https://www.jetbrains.com/help/idea/intention-actions.html
[Basic code completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#basic_completion
[Smart code completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#smart_completion
[Smart statement completion]:https://www.jetbrains.com/help/idea/auto-completing-code.html#statements_completion
[Extending or shrinking selection]:https://www.jetbrains.com/help/idea/editor-basics.html#edit_code
[Add/remove line or block comment]:https://www.jetbrains.com/help/idea/editor-basics.html#editor_lines_code_blocks
[Highlight usages in file]:https://www.jetbrains.com/help/idea/highlighting-usages.html
[Quick Lists]:https://www.jetbrains.com/help/idea/configuring-quick-lists.html
[Smart Keys]:https://www.jetbrains.com/help/idea/smart-keys.html
[Speed search]:https://www.jetbrains.com/help/idea/speed-search-in-the-tool-windows.html


# 智能快捷键
IntelliJ IDEA 的大多数命令都有键盘快捷键，它与编辑、导航、重构、调试和其他任务有关。记住这些热键可以帮助你保持双手在键盘上的效率。
*小提示：建议使用英文版的键盘。IntelliJ IDEA可能无法正确检测其他国家布局的某些快捷方式。*

- [选择正确的热键](#选择正确的热键)
- [在工作中学习快捷键](#在工作中学习快捷键)
- [使用高级特性](#使用高级特性)


## 选择正确的热键
要检索热键配置，请打开 `Settings/Preferences` 对话框 (`Ctrl+Alt+S`) 以及选择 `Keymap` 子菜单。
*小提示：启用功能键并检查与全局 OS 快捷键 [possible conflicts]。*

- 使用预定义热键

    IntelliJ IDEA 会基于你的开发环境，自动选择一个 [predefined keymap]。确保它与您正在使用的操作系统相匹配，或者选择一个与您所使用的另一个 IDE（例如，Eclipse 或 NetBeans）匹配的快捷键。

- 优化你的热键

    你可以 [modify a copy] 任何预定义的热键映射，以便为您经常使用的命令分配自己的快捷键。

    *小提示：对于 macOS 系统，选择 Mac OS X 10.5+ 的快捷键而不是 Mac OS X。*

- 导入自定义热键

    如果你有习惯上的自定义热键，你可以 [transfer it to your installation]。


## 在工作中学习快捷键
IntelliJ IDEA 提供了几种学习快捷键的可能性：

- [Find Action] 是最重要的命令，它使您能够在所有菜单和工具中搜索命令和设置。

    按下 `Ctrl+Alt+A` 快捷键，然后开始键入，以获取建议动作的列表。

    ![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/智能快捷键/image/gotoAction.png)

    你可以选择必要的命令并按 `Enter` 执行它。

- [Key Promoter X] 是一个插件，当使用鼠标执行命令时，它会显示相应的键盘快捷键，并建议为频繁执行的命令创建快捷方式。

- 如果您正在使用一个操作系统相关的预定义热键，您可以打印 [default keymap reference card]，并将它放在您的办公桌上，以便在必要时查阅。这个备忘单也可以在 `Help | Keymap Reference` 下使用。完整的引用记录在 [Keyboard Shortcuts and Mouse Reference] 中。

下表列出了最常用的快捷键以备学习。

| 快捷键 | 相关动作 |
| :-:| :-:|
| `Ctrl+Shift+A` | [Find Action] <br> 使用关键字搜索命令并执行它 |
| `Ctrl+N` <br> `Ctrl+Shift+N` <br> `Ctrl+Shift+Alt+N` | [Find class, file, or symbol] <br> 使用关键字去寻找并跳跃到期望的类、文件或符号 |
| `Ctrl+E` | [View recent files] <br> 从列表中选择最近打开的文件 |
| `Alt+Enter` | [Show intention actions] <br> 改进或优化代码结构 |
| `Ctrl+Space` | [Basic code completion] <br> 在可见的范围内，补全类、方法、字段和关键字的名字 |
| `Ctrl+Shift+Space` | [Smart code completion] <br> 基于类型的适用于当前上下文的代码补全 |
| `Ctrl+Shift+Enter` | [Smart statement completion] <br> 根据正确语法的代码结构完成一条语句 |
| `Ctrl+W` <br> `Ctrl+Shift+W` | [Extending or shrinking selection] <br> 根据特定的代码结构，增加或减少选择范围 |
| `Ctrl+Slash` <br> `Ctrl+Shift+Slash` | [Add/remove line or block comment] <br> 注释一行或一段代码 |
| `Ctrl+Shift+F7` | [Highlight usages in file] <br> 将当前文件中所选择的片段全部显现出来 |


## 使用高级特性
您可以通过以下有用的功能进一步提高您的效率：

- [Quick Lists]

    如果有一组您经常使用的操作，创建一个快速列表以使用自定义快捷方式访问它们。例如，您可以尝试使用以下预定义的快速列表:
    - **重构它们** `Ctrl+Shift+Alt+T`
    - **VCS 操作** `Alt+Back Quote`

- [Smart Keys]

    IntelliJ IDEA 提供了各种各样的帮助，例如自动添加配对标签和引用，以及检测 *CamelHump*（驼峰式命名） 字样。

- [Speed search]

    当焦点放在带有树、列表或表的工具窗口时，开始键入以查看匹配项。

- **连续按两次**

    在 IntelliJ IDEA 中的许多动作在执行多次时提供了更多的结果。例如，当您在字段、参数或变量声明的某个部分上，使用 `Ctrl+Space` 调用基本代码完成时，它会根据当前范围内的项目类型提供一些建议名称。如果您再次调用它，将包含通过模块依赖关系可用的类。在连续第三次调用时，建议列表将包括整个项目。

- **调整工具窗口**

    你可以在没有鼠标的情况下调整工具窗口的大小：

    - 要调整垂直工具窗口的大小，请使用 `Ctrl+Shift+Left` 和 `Ctrl+Shift+Right`
    - 要调整水平工具窗口的大小，请使用 `Ctrl+Shift+Up` 和 `Ctrl+Shift+Down`

# ——
**返回** [认识IDEA]

**下一步** [专业建议]
