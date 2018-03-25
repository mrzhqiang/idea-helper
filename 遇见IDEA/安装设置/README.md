# 安装设置
- [安装要求](#安装要求)
- [下载和安装](#下载和安装)
- [首次运行](#首次运行)
- [注册/登记](#注册/登记)
- [更新](#更新)
- [工具箱管理](#工具箱管理)
- [静默安装](#静默安装)
- [snap包安装](#snap包安装)

## 安装要求

### 硬件要求
- 最小 1GB 内存，推荐 2GB 内存
- 1.5GB 硬盘空间，至少 1GB 用于缓存
- 最低屏幕分辨率 1024 x768

### 软件要求
JRE 1.8 与 IDEA 发行版捆绑在一起，您不必在计算机上安装 Java 来运行 IDEA，但需要安装对应版本的 JDK 来进行 Java 开发。

| Windows | macOS | Linux |
| :-: | :-: | :-: |
| Microsoft Windows 10/8/7/Vista/2003/XP (32 or 64 bit) | macOS 10.8 or later (only 64-bit systems are supported) | OS Linux (note that a 32-bit JDK is not bundled, so a 64-bit system is recommended)KDE, Gnome or Unity DE desktop |

*译者注：（统一使用“——”表示译者注）通常 IDEA 捆绑的 JRE（例如..\IntelliJ IDEA 2017.3.2\jre64）会导致中文输入法无法正常工作，最明显的一个表现是，候选框将无法跟随光标。要解决这个问题，可以通过修改目录名 jre64 为其他不同的名字即可。*

## 下载和安装
IDEA 有两个版本: `Ultimate` 和 `Community`。`Community` 版是一个开源项目，它是免费的，但它的功能更少。`Ultimate` 版是商业性的，并提供了一套出色的工具和功能。有关详细信息，请参阅 [editions comparison matrix](https://www.jetbrains.com/idea/features/editions_comparison_matrix.html)。

安装 IDEA：

1. 根据您的操作系统 [下载 IDEA](https://www.jetbrains.com/idea/download/index.html)。

    *小提示：32位系统的 JRE 不与 IntelliJ IDEA 捆绑在一起。如果您使用的是32位版本的 Windows，请选择安装向导中的 Jetbrains 复选框下载并安装 JRE x86，以便自动下载和安装 JRE。*

2. 在您的操作系统中，执行以下操作：

    - Windows：
        1. 运行下载的安装文件，比如：`ideaIC-2017.3.2.exe` 或者 `ideaIU-2017.3.2.exe`
        2. 按照安装向导中的说明操作

    - macOS：
        1. 双击 `ideaIC.dmg` 或者 `ideaIU.dmg` 文件，您已经下载了安装 macOS 磁盘映像——这句翻译可能不准确，因为没有用过 macOS
        2. 将 IDEA 复制到 `Applications` 文件夹

    - Linux：
        1. 解压 `ideaIC.gz` 或 `ideaIU.gz`，如果你当前下载文件夹不支持文件执行，你可以下载到一个不同的文件夹：

        ```
        tar xfz ideaIC.tar.gz or ideaIU.tar.gz. <new_archive_folder>
        ```

        推荐的安装位置根据文件系统层次标准（FHS）是 /opt。例如，可以输入以下命令：

        ```
        sudo tar xf -*.tar.gz -C /opt/
        ```

        2. 切换到 `bin` 目录，比如：

        ```
        cd /opt/-*/bin
        ```

        3. 从 bin 的子目录运行 `idea.sh`

        *小提示：一个新的实例不能从现有的实例中提取出来。目标文件夹必须为空。*


## 首次运行

### 导入设置
当你第一次启动 IDEA，或者你从以前的版本升级它之后，`Complete Installation` 的对话框将打开，您可以选择是否要导入 IDE 设置：

![complete-installation](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/complete-installation.png)

如果你是第一次使用 IDEA，只需要选择 `Do not import settings` 选项就行。

*小提示：您可以在以后某个时间，通过主菜单上的 `File | Import Settings` 和 `File | Export Settings` 命令手动 [import and export settings](https://www.jetbrains.com/help/idea/exporting-and-importing-settings.html)。*

### 选择用户界面主题
接下来，将提示你选择 UI 主题，你可以在 `Default` 和 `Darcula` 主题之间选择一个：

![Customize IntelliJ IDEA](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/customize-idea.png)

*——通常来说，`Darcula` 主题更适合编程，它是黑色背景，不会太刺眼。*

### 禁用多余插件
IDEA 装载了各种插件，这些插件提供了不同的版本控制系统和应用服务器的集成，为各种框架和开发技术提供了支持。

下一步，为了增加 IDEA 的性能，您可以禁用插件（——*这里翻译可能不准确，但原文的意思更加晦涩*）。如果有必要，你可以在 `Settings` 对话框中重新启用它们（Ctrl+Alt+S 下的 `Plugins`）。

![default-plugins](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/default-plugins.png)

你可以点击 `Disable All` 链接来禁用插件组中的所有插件，或者点击 `Customize` 来禁用个别插件。

### 下载和安装额外插件
下一步，你会被提示下载额外的插件，它们没有和 [IntelliJ IDEA plugins repository](https://plugins.jetbrains.com/idea) 相绑定：

![ij_set_featured_plugins](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/ij_set_featured_plugins.png)

### 在 IDEA 中启动工程
在你完成初始化 IDEA 的配置之后，有一个 `Welcome` 屏幕将显示出来，它告诉你可以做：

- [create a new project](https://www.jetbrains.com/help/idea/configuring-projects.html#working-with-projects)
- 或者 [check out an existing project from a version control system (clone from a remote repository)](https://www.jetbrains.com/help/idea/version-control-with-intellij-idea.html)

![ij_welcomeScreen](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/ij_welcomeScreen.png)

你可以观看一个关于如何第一次运行 IDEA 的视频教程。

如果您想快速了解 IDEA 的主要功能以及如何使用它们，请参考 [探索](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/探索/) 部分。


## 注册/登记
想要评估 IDEA，你可以免费下载并安装试用版。试用版可以使用 30 天，因此您需要获得并注册一个许可证。

*——这里描述的似乎是 Web/JavaEE 开发，也就是 `Ultimate` 版本*

小提示：IDEA 构建可以作为 [Early Access Program](https://www.jetbrains.com/community/eap/) 的部分下载，不需要注册，并且附带 30 天的许可认证。

1. 做以下之一的事情：
    - 在 `Welcome` 屏幕上，点击 `Configure | Manage Liscense`
    - 如果已经进入 IDEA 界面，从主菜单中选择 `Help | Register`

    ![ij_register](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/ij_register.png)

    *——图片中的地址并没有尝试过是否可用，但我通过 [lanyu 破解 IDEA](http://idea.lanyus.com/) 搭建了一个认证服务器，可用到 2018 年 6 月底：*

    ```
    http://randall.top:41017
    ```

    *——未来还会续费一个全新的服务器，这个域名一直可用，只是不保证 2018 年 7 月期间，能够有效激活 IDEA。*

2. 选择你希望的一种注册方式：
    - `JetBrains Account`：如果你有一个 [JetBrains Account](https://account.jetbrains.com/login) 可以允许你访问你购买和管理的许可，那么你可以选择这个选项（参考 [What is JetBrains Account?](https://sales.jetbrains.com/hc/en-gb/articles/208459005-What-is-JetBrains-Account-) 学习更多）
    - `Activation code`：如果你有一个 IDEA 激活码，请选择此项，并将之粘贴到文本区域
    - `License server`：选择这个选项，你可以通过 [License Server](https://www.jetbrains.com/help/license_server/getting_started.html) web 应用注册 IDEA，它允许你管理浮动许可，并向没有直接网络访问权限的用户颁发许可证


## 更新
在 box 之外，单独安装的 IDEA 会被配置为自动检查更新，当有一个新版本可用时，它会自动通知你：

![ij_update_restart](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/ij_update_restart.png)

IDEA 的更新通常是基于补丁，它们应用于现有的安装，并只要求你重启 IDE。需要注意的是，这些补丁只能逐个按顺序执行，如果这些更新被忽略或者跳过，后面的更新将不会被应用。在这种情况下，更新 IDEA 需要下载和重新安装，或者使用 `忽略更新` 列表来 [apply updates one by one](https://www.jetbrains.com/help/idea/keep-intellij-idea-up-to-date.html#apply_patch)。

出于某种原因，你不想安装建议的更新，你可以在更新对话框中，点击 `Ignore This Update` 按钮来忽略它。被忽略的构建的数字将被添加到被忽略的更新列表中，并且您将不会被提示安装这个特定的构建，直到您 [remove it from the list](https://www.jetbrains.com/help/idea/keep-intellij-idea-up-to-date.html#manage_ignored_updates) 它。

*小提示：如果您喜欢集中式的方法来管理所有开发工具(包括更新它们)，请使用 [工具箱管理](#工具箱管理) 。*


## 工具箱管理
`Toolbox App` 是一个控制面板，它允许您从一个单一的访问点管理所有 JetBrains 开发工具，包括 IDEA 以及您的项目。它允许您维护相同工具的不同版本，安装更新，并在需要时将其回滚。它还记得您的 JetBrains 帐户，并使用它在您安装和注册新工具时自动记录您的信息。

*小提示：在 IntelliJ IDEA 中引入了重大的变化时，您将需要下载并安装新版本，如[下载安装](#下载安装)。*

1. [下载](https://www.jetbrains.com/toolbox/app/) Toolbox App
2. 启动安装文件
3. 当安装完成后，接受JetBrains隐私策略并登录到您的 JetBrains 帐户

现在，你可以管理已经存在的工具，安装新工具和下载更新：

![toolbox_app](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/安装设置/image/toolbox_app.png)


## 静默安装
静默安装没有任何用户界面。它可以被网络管理员用来在一些机器上安装 IntelliJ IDEA，避免打断其他用户。

要执行静默安装，请使用以下开关运行安装程序：

- **/S**：启用静默安装
- **/D**：指定安装目录的路径
- **/CONFIG**：指定 [silent configuration file](https://www.jetbrains.com/help/idea/install-and-set-up-intellij-idea.html#silent-config) 的路径

比如：

```
ideaIU.exe /S /CONFIG=d:\temp\silent.config /D=d:\IDE\IntelliJ IDEA Ultimate
```

### 静默配置文件
你可以在  [https://download.jetbrains.com/idea/silent.config](https://download.jetbrains.com/idea/silent.config) 下载 IntelliJ IDEA 的静默配置文件。

静默配置文件定义了安装 IntelliJ IDEA 的选项。对于默认选项，静默安装只针对当前用户 (mode=user) 执行。如果您想为所有用户安装 IntelliJ IDEA，请使用文本编辑器打开静默配置文件，更改安装模式选项 (mode=admin) 的值，并作为管理员运行安装程序。

*小提示：默认的静默配置文件对每个 JetBrains 产品都是唯一的。 您可以修改它以根据需要启用或禁用各种安装选项。*

## snap包安装
您可以在 Linux 上作为一个独立的 [snap](https://snapcraft.io/) 包来安装 IntelliJ IDEA，由于快照会自动更新，您的 IntelliJ IDEA 安装将始终是最新的版本。

*小提示：如 [installation guide](https://docs.snapcraft.io/core/install) 中所述，在您的机器上使用快照、安装和运行 `snapd` 服务。在 Ubuntu 16.04 LTS 和之后，这个服务是预先安装的。*

IntelliJ IDEA 通过两个渠道发布：

- 稳定的通道只包括稳定的版本。要安装 IntelliJ IDEA 最新的稳定版本，运行以下命令：

    完整版：
    ```
    $ sudo snap install intellij-idea-ultimate --classic
    ```

    社区版：
    ```
    $ sudo snap install intellij-idea-community --classic
    ```

- 边缘通道包括 EAP 发行版。要安装 IntelliJ IDEA 最新的 EAP 版本，运行以下命令：

    完整版：
    ```
    $ sudo snap install intellij-idea-ultimate --classic --edge
    ```

    社区版：
    ```
    $ sudo snap install intellij-idea-community --classic --edge
    ```

    *小提示： `--classic` 选项是必需的，因为 IntelliJ IDEA snap 需要对系统进行完全访问，就像传统的打包应用程序一样。*

安装 snap 时，可以运行 **intellij-idea-community** 或 **intellij-idea-ultimate** 命令来启动它。

要列出所有已安装的快照，请运行 **sudo snap list** 。有关更多信息，请参见 [Snapcraft documentation](https://docs.snapcraft.io/)。


# ——
**向前** [遇见IDEA](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/)

**下一步** [探索](https://github.com/mrzhqiang/idea-helper/blob/master/遇见IDEA/探索)
