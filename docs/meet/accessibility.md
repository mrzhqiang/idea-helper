---
layout: default
title: 无障碍
parent: 遇见
nav_order: 2
permalink: /meet/accessibility
---


# 无障碍
{: .no_toc }
原文：[Accessibility]。

IntelliJ IDEA 允许您启用各种辅助功能以满足您的需求。您可以使用屏幕阅读器或调整字体大小、颜色以及某些 UI 元素的行为，以便更轻松地使用 IntelliJ IDEA。

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——无障碍功能正常情况下很少用到，所以没有特殊需求的话，建议跳过这部分内容。
</span>

## 目录
{: .no_toc .text-delta }

- TOC
{:toc}

---

## 安装屏幕阅读器
目前，我们完全支持 Windows 上的 IntelliJ IDEA 屏幕阅读器。您可以在 macOS 上使用某种程度上的 IntelliJ IDEA 屏幕阅读器。然而，为了充分利用屏幕阅读器的支持，我们推荐 Windows 系统。

对于 *macOS*，请打开 [VoiceOver] 然后 [安装和设置](#安装和设置)。

### 为 Windows 启用屏幕阅读器
1. 下载和启用您首选的屏幕阅读器。

    检查以下推荐的屏幕阅读器：
    
    \- [NVDA] - 使用 NVDA 2015 或更高版本。如果你使用 32 位的 NVDA 版本，你必须安装 32 位 JRE，因为这个 NVDA 版本必须有 `C:\Windows\SysWOW64\WindowsAccessBridge-32.DLL` 才能使用 IntelliJ IDEA。如果 NVDA 不能找不到此文件，NVDA 事件日志窗口将显示相应的消息。
    
    \- [JAWS] - 下载你需要的版本并重启计算机来启用 JAWS 屏幕阅读器。

2. 确保已为屏幕阅读器安装了[Java Access Bridge] 和正确的 Java 版本，如下所示：

    \- 要启用 [Java Access Bridge]，请打开命令提示符并键入 `[JRE_HOME]\bin\jabswitch -enable`，其中 `[JRE_HOME]` 是计算机上的 JRE 目录。对于 Java1.8，Java Access Bridge 是 JDK 的一部分，您无需单独下载或启用它。
 
    \- 如果您的屏幕阅读器是 32 位，请安装 *32-bit JRE1.7* 或更高版本。如果您的屏幕阅读器是 64 位，请安装 *64-bit JRE1.7* 或更高版本。

### 安装和设置
1. [下载和安装][11] IntelliJ IDEA。

2. 要在 IntelliJ IDEA 首次启动之前启用屏幕阅读器支持，请执行以下操作：

    1. 打开 `configuration` 目录下包含个人设置的文件，例如 keymaps、color schemes 等等。
    
        **Windows**
        ```
        Syntax
                %HOMEPATH%\.<product><version>\config
        Example
                C:\Users\JohnS\.IntelliJIdea2018.3\config
        ```
        
        **macOS**
        ```
        Syntax
                ~/Library/Preferences/<product><version>
        Example
                ~/Library/Preferences/IntelliJIdea2018.3
        ```
        
        **Linux**
        ```
        Syntax
                ~/.<product><version>/config
        Example
                ~/.IntelliJIdea2018.3/config
        ```
        
    2. 创建名为 `idea.properties` 的文件。
    
    3. 将 `ide.support.screenreaders.enabled=true` 属性添加到创建的文件中。
    
3. 启动 IntelliJ IDEA，位于 **Settings / Preferences \| Appearance & Behavior \| Appearance** 的 **Support screen readers** 选项将启用。

## 自定义 IDE
您可以根据您的无障碍需求自定义 IDE。

### 调整颜色以适应红绿色视觉缺陷
如果您有红绿色视觉缺陷，您可以调整颜色。在这种情况下，代码片段（例如通常以红色突出显示的错误或通常为绿色的字符串）将更改颜色以满足您的需求（红色将更改为橙色，绿色将更改为蓝色）。测试运行器中进度条的颜色也将进行调整，以便轻松识别。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Appearance and Behavior \| Appearance**。

2. 从右侧的选项中，选择 **Adjust colors for red-green vision deficiency (protanopia, deuteranopia)** 选项并点击 **OK** 按钮以保存改动。

检查以下示例，其中 **Before** 包含以绿色高亮显示的 *String* 和以红色高亮显示的 *Error*，而 **After** 包含颜色调整的地方：

**Before**

  ![]({{ site.baseurl }}{% link assets/images/before_color_adjustment.png %})

**After**

  ![]({{ site.baseurl }}{% link assets/images/after_color_adjustment.png %})
  
### 配置代码元素、编辑器、超链接等的颜色
您可以调整代码元素、错误、编辑器元素和工具窗口的颜色。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| Color Scheme \| General**。

2. 从右侧的选项列表中，选择要为其调整颜色的内容。例如，您可以选择 **Code** 并调整注入语言片段或匹配大括号等的颜色。点击 **OK** 保存改动。

您还可以调整 IDE 的调试器、控制台和其他部分的颜色：只需在位于 **Settings / Preferences \| Editor \| Color Scheme** 的选项列表中选择适当的节点即可。

### 覆盖默认的 UI 字体
您可以覆盖 UI 元素的默认字体。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Appearance and Behavior \| Appearance**。

2. 从右侧选项的 **UI options** 片段中，选择 **Override default fonts by (not recommended)** 以及指定的字体名字和大小。点击 **OK** 保存改动。

### 调整工具窗口的大小
您可以使用快捷方式垂直或水平调整实际工具窗口的大小。

1. 垂直向上或向下调整大小，请按 `Ctrl+Shift+Up` 或者 `Ctrl+Shift+Down`。

2. 要向左或向右水平调整大小，请按 `Ctrl+Shift+Left` 或者 `Ctrl+Shift+Right`。

### 在编辑器中调整文本大小
您可以在编辑器中更改文本的字体和大小。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| General**。

2. 从右侧选项的 **UI options** 片段中，选择 **Change font size (Zoom) with Ctrl+Mouse Wheel** 选项，以便在编辑器中工作时快速更改文本大小（转动鼠标滚轮）。

3. 如果需要指定确切的字体大小，选择 **Editor \| Font**。

4. 从右侧选项中，指定字体、大小、行间距和其他可用选项。点击 **OK** 保存改动。

### 自定义快捷方式
您可以为经常使用的操作配置自定义快捷方式。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Keymap**。

2. 从右侧的选项列表（如菜单、操作和工具）中，选择所需的操作。

3. 右键单击所选项目，然后从上下文菜单中选择要执行的操作，例如 **Add keyboard shortcut**，**Add mouse shortcut**，或者 **Add abbreviation**。

4. 在打开的对话框中，指定快捷方式。如果需要，请选择 **Second stroke** 选项，并为快捷方式指定其他键。单击 **OK** 保存改动。请注意，您需要使用鼠标单击 **OK** 按钮。如果按 `Enter` 键，IntelliJ IDEA 会将其视为快捷方式。

请注意，您可以忽略冲突并为多个操作指定快捷方式。但是，强烈建议您避免使用相同的快捷方式绑定两个操作，因为未定义这些操作的优先级。

### 自定义智能键行为
您可以配置智能键的行为。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| General \| Smart keys**。

2. 从右侧的选项中，选择或清除智能键选项，例如，您可以清除 **Insert paired brackets** 或 **Insert paired quotes** 选项，该选项会自动插入右括号或引号，因为它在您使用屏幕阅读器时可能没用。单击 **OK** 保存改动。

### 禁用自动代码完成
您可以禁用自动代码完成，以避免在使用屏幕阅读器的编辑器中工作时自动插入代码元素。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| General \| Code completion**。

2. 从右侧的选项中，清除 **Smart Type Completion** 选项。如果需要，请清除 **Basic Completion** 以禁用基本完成。

### 自定义代码折叠
您可以控制代码折叠行为并指定应折叠或不折叠的内容。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| Code Style \| \[Language]**。

2. 从右侧的选项中，单击 **Tabs and Indents** 以配置选项卡，或者单击 **Spaces** 以配置空格的位置和方式。

3. 单击 **OK** 保存改动。

### 管理鼠标指针焦点模式
您可以配置打开对话框时鼠标指针的行为方式。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Appearance and Behavior \| Appearance**。

2. 从右侧的选项中，选中 **Automatically position mouse cursor on default button** 复选框。选中此复选框可在对话框打开时将鼠标指针置于默认按钮。如果未选中该复选框，则指针位置不会更改。

3. 单击 **OK** 保存改动。

### 在编辑器中读取装订线图标和行号
您可以配置屏幕阅读器以读取位于编辑器左侧装订线中的行号、VCS 注释、调试器和其他图标。

1. 在编辑器中打开文件。

2. 在编辑器中，按下双重快捷键 `Shift + Alt + 6` 和 `F` 将焦点放在装订线上。IntelliJ IDEA 从您的插入符号当前所在的行开始读取。

3. 使用 *Up* 和 *Down* 箭头键在行之间移动。如果需要移动到行中的下一个或上一个 gutter 元素，请分别使用 *Right* 和 *Left* 箭头键。

  虽然重点在于装订线，但是如果可用，屏幕阅读器可以读取装订线图标工具提示。
  
  要访问工具提示，请按下双重快捷键 `Shift + Alt + 6` 和 `T`。要浏览工具提示的内容（逐个符号），请使用 *Right* 和 *Left* 箭头键。
  
4. 按 `Escape` 键将焦点切换回编辑器。

### 高对比度的主题颜色
您可以设置高对比度主题以在 IntelliJ IDEA 中工作。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Appearance and Behavior \| Appearance**。

2. 在 **Appearance** 页面的 *UI Options area*，从 **Theme** 下拉列表中选择 **High Contrast**，然后点击 **OK** 应用改动。

### 高对比度配色方案
您可以为编辑器设置高对比度方案。

1. 在 **Settings/Preference** 对话框（`Ctrl+Alt+S`）中，跳转到 **Editor \| Color Scheme**。

2. 在 **Color Scheme** 页面，从 **Scheme** 下拉列表中选择 **High Contrast**。

3. 点击 **OK** 应用改动。

您可以检查 [Editor basics] 和 [Guided Tour around the User Interface]，以熟悉其他有用的快捷方式。



[Accessibility]:https://www.jetbrains.com/help/idea/accessibility.html
[VoiceOver]:https://www.apple.com/voiceover/info/guide/_1124.html
[NVDA]:https://www.nvaccess.org/
[JAWS]:https://www.freedomscientific.com/Products/Blindness/JAWS
[Java Access Bridge]:https://docs.oracle.com/javase/7/docs/technotes/guides/access/enable_and_test.html
[Editor basics]:https://www.jetbrains.com/help/idea/using-code-editor.html
[Guided Tour around the User Interface]:https://www.jetbrains.com/help/idea/guided-tour-around-the-user-interface.html


[11]:{{ site.baseurl }}{% link docs/meet/install-and-set-up.md %}