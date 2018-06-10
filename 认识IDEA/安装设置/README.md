[认识IDEA]:https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/
[探索]:https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/探索/

[editions comparison matrix]:https://www.jetbrains.com/idea/features/editions_comparison_matrix.html
[下载 IntelliJ IDEA]:https://www.jetbrains.com/idea/download/index.html
[import and export settings]:https://www.jetbrains.com/help/idea/exporting-and-importing-settings.html
[IntelliJ IDEA plugins repository]:https://plugins.jetbrains.com/idea
[create a new project]:https://www.jetbrains.com/help/idea/configuring-projects.html#working-with-projects
[check out an existing project from a version control system (clone from a remote repository)]:https://www.jetbrains.com/help/idea/version-control-with-intellij-idea.html
[Early Access Program]:https://www.jetbrains.com/community/eap/
[lanyu 破解 IntelliJ IDEA]:http://idea.lanyus.com/
[JetBrains Account]:https://account.jetbrains.com/login
[What is JetBrains Account?]:https://sales.jetbrains.com/hc/en-gb/articles/208459005-What-is-JetBrains-Account-
[License Server]:https://www.jetbrains.com/help/license_server/getting_started.html
[JVM option]:https://www.jetbrains.com/help/idea/tuning-the-ide.html#configure-jvm-options
[apply updates one by one]:https://www.jetbrains.com/help/idea/keep-intellij-idea-up-to-date.html#apply_patch
[remove it from the list]:https://www.jetbrains.com/help/idea/keep-intellij-idea-up-to-date.html#manage_ignored_updates
[下载]:https://www.jetbrains.com/toolbox/app/
[silent configuration file]:https://www.jetbrains.com/help/idea/install-and-set-up-intellij-idea.html#silent-config
[https://download.jetbrains.com/idea/silent.config]:https://download.jetbrains.com/idea/silent.config
[snap]:https://snapcraft.io/
[installation guide]:https://docs.snapcraft.io/core/install
[Snapcraft documentation]:https://docs.snapcraft.io/


# 安装设置
- [安装要求](#安装要求)
- [下载和安装](#下载和安装)
- [首次运行](#首次运行)
- [注册](#注册)
- [更新](#更新)
- [工具箱管理](#工具箱管理)
- [静默安装](#静默安装)
- [snap包安装](#snap包安装)


## 安装要求

### 硬件要求
- 最小 2GB 内存，建议 4GB 内存
- 1.5GB 的硬盘空间 + 至少 1GB 的缓存
- 最小屏幕分辨率为 1024 x768

### 软件需求
JRE 1.8 与 IntelliJ IDEA 发行版捆绑在一起，您不需要在计算机上安装 Java 来运行 IntelliJ IDEA。

但进行 Java 开发需要独立的 JDK。

| Windows | macOS | Linux |
| :-:| :-:| :-:|
| 32 位或 64 位版本的微软 Windows 10, 8, 7 (SP1)，或者 Vista (SP2) | macOS 10.8.3 或者更高版本（仅支持 64 位系统）| - OS Linux （请注意，32 位的 JDK 未捆绑，所以建议使用 64 位系统）<br> - 建议使用 KDE，Gnome 或 Unity 桌面环境 |

*译者注（统一使用“——”表示）：IntelliJ IDEA 捆绑的 JRE（例如..\IntelliJ IDEA 2017.3.2\jre64）很有可能导致中文输入法无法正常工作，比如，输入候选框不跟随光标。为解决这个问题，可以通过修改 jre64 目录为其他名字，比如 jre641，然后 IntelliJ IDEA 会寻找系统的 JRE 环境，此时你必须同时安装 JDK 和 JRE。*


## 下载和安装
IntelliJ IDEA 有两个版本：`Ultimate`（终极版） 和 `Community`（社区版）。社区版是一个免费的开源项目，它的功能较少。终极版是商业性的，它提供了一套优秀的工具集和功能。有关详细信息，请参阅 [editions comparison matrix]。

安装 IntelliJ IDEA：

1. 为您的操作系统 [下载 IntelliJ IDEA]。

    *小提示：32 位系统的 JRE 未和 IntelliJ IDEA 捆绑在一起。如果您使用的是 32 位版本的 Windows，请勾选安装向导中的 __Download and install JRE x86 by Jetbrains__ 复选框，以便自动下载和安装 JRE。*

2. 根据您的操作系统，执行以下操作：

    - Windows：
        1. 运行你下载的 **ideaIC.exe** 或 **ideaIU.exe** 文件。
        2. 按照安装向导中的说明进行操作。

    - macOS：
        1. 双击你下载的 **ideaIC.dmg** 或 **ideaIU.dmg** 文件。
        2. 将 IntelliJ IDEA 复制到 **Applications** 文件夹

    - Linux：
        1. 解压你下载的 **ideaIC.gz** 或 **ideaIU.gz** 文件，如果当前 **Downloads** 目录没有执行权限，你可以解压到不同的文件夹：

        ```
        tar xfz ideaIC.tar.gz or ideaIU.tar.gz. <new_archive_folder>
        ```

        *小提示：新实例不能从现有的实例中提取。目标文件夹必须为空。*

        根据文件系统层次结构标准（FHS）推荐的安装位置是 **/opt**。例如，可以输入以下命令：

        ```
        sudo tar xf -*.tar.gz -C /opt/
        ```

        2. 切换到 **bin** 目录，比如：

        ```
        cd /opt/-*/bin
        ```

        3. 从 **bin** 的子目录运行 **idea.sh**


## 首次运行

### 导入设置
当你首次启动 IntelliJ IDEA 时，或者在你从先前版本升级之后，将打开 **Complete Installation** 对话框，你可以在其中选择是否要导入 IDE 设置：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/complete-installation.png)

如果这是你的第一个 IntelliJ IDEA 实例，请选择 `Do not import settings` 选项。

*小提示：您可以稍后使用在主菜单上的 `File | Import Settings` 和 `File | Export Settings` 命令手动 [import and export settings]。*

### 选择用户界面主题
接下来，系统会提示你选择 UI 主题，你可以在 **Default** 和 **Darcula** 主题之间进行选择：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/customize-idea.png)

*——`Darcula` 主题更舒服一些，保护眼睛，拒绝白色背景。*

### 禁用不必要的插件
IntelliJ IDEA 装载了各种插件，可与不同的版本控制系统和应用程序服务器进行集成，增加对各种框架和开发技术的支持等。

下一步，为增加 IntelliJ IDEA 的性能，您可以禁用不需要的插件。如有必要，你可以稍后在 **Settings** 对话框中重新启用它们（`Ctrl+Alt+S` 下的 **Plugins**）。

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/default-plugins.png)

你可以点击每个插件组的 **Disable All** 链接来禁用所有插件，或者点击 **Customize** 禁用单个插件。

### 下载并安装其他插件
下一步，系统会提示你从 [IntelliJ IDEA plugins repository] 下载未捆绑在 IDE 中的其他插件：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/ij_set_featured_plugins.png)

### 在 IntelliJ IDEA 中启动一个项目
完成初始化 IntelliJ IDEA 配置后，有一个 **Welcome** 屏幕将显示，它允许你：

- [create a new project]
- 或 [check out an existing project from a version control system (clone from a remote repository)]

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/ij_welcomeScreen.png)

你可以观看关于如何首次运行 IntelliJ IDEA 的快速视频教程。

如果您想快速了解 IntelliJ IDEA 的主要功能以及如何使用它们，请参考 [探索] 部分。


## 注册
想要尝试和评估 IntelliJ IDEA，你可以免费下载并安装试用版。试用版可以使用 30 天，因此您需要获得并注册许可证。

*——这里描述的似乎是 `Ultimate` 版本*

小提示：IntelliJ IDEA 构建可以作为 [Early Access Program] 的部分下载，不需要注册，并且附带 30 天的许可认证。

1. 执行以下操作之一：
    - 在 **Welcome** 屏幕上，点击 **Configure | Manage Liscense**
    - 如果已经进入 IntelliJ IDEA 界面，从主菜单中选择 **Help | Register**

    ![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/ij_register.png)

    *——图片中的地址并没有尝试过是否可用，但我通过 [lanyu 破解 IntelliJ IDEA] 搭建了一个认证服务器，可用到 2018 年 6 月底：*

    ```
    http://randall.top:41017
    ```

    *——未来还会续费一个全新的服务器，这个域名一直可用，只是不保证 2018 年 7 月期间，能够有效激活 IntelliJ IDEA。*

2. 选择你想要注册 IntelliJ IDEA 的方式：
    - **JetBrains Account：** 如果你有一个 [JetBrains Account] 可以访问你的购买和管理许可证，请选择此选项（请参阅 [What is JetBrains Account?] 以了解更多信息）。
    - **Activation code：** 如果你拥有 IntelliJ IDEA 激活码，请选择此选项，然后将其粘贴到文本区域。
    - **License server：** 选择此选项可通过 [License Server] web 应用程序注册 IntelliJ IDEA，它允许你管理浮动许可证，并向无法直接访问网络的用户颁发许可证。

    要在初始启动 IntelliJ IDEA 的过程中覆盖系统代理的 URL，请使用 **-Djba.http.proxy** 属性，该属性可以作为 [JVM option] 添加 。

    在多台机器上执行静默安装或管理 IntelliJ IDEA 安装时，可以设置 **JETBRAINS_LICENSE_SERVER** 环境变量以将安装指向许可证服务器 URL。


## 更新
开箱即用，独立的 IntelliJ IDEA 会被配置为自动检查更新，当有一个新版本可用时，它会自动通知你：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/ij_update_restart.png)

*小提示：如果您更喜欢集中管理所有开发人员工具（包括更新它们），请使用 [工具箱管理](#工具箱管理) 。*

IntelliJ IDEA 更新通常是 *patch-based*（基于补丁的），它们被应用于现有安装，并只需要你重启 IDE。请注意，这些补丁只能按顺序依次应用，如果更新被忽略或者跳过，则后续更新无法应用。在这种情况下，更新 IntelliJ IDEA 将需要下载并重新安装，或使用 **忽略更新** 列表来 [apply updates one by one]。

如果修补程序的下载需要很长时间，则可以将其发送到后台并继续工作。下载完成后，系统会提示您重新启动，以完成更新。

出于某种原因，你不想安装建议的更新，你可以在更新对话框中，点击 **Ignore This Update** 按钮来忽略它。被忽略的版本号将被添加到 **被忽略的更新** 列表中，并且不会提示你安装这个特定版本，除非您 [remove it from the list]。

*小提示：在 IntelliJ IDEA 中引入重大更改时，将需要按照 [下载和安装](#下载和安装) 中的描述下载和安装新版本。*


## 工具箱管理
**Toolbox App** 是一个控制面板，允许你从单一访问点管理所有 JetBrains 开发人员工具，包括 IntelliJ IDEA 以及项目。它允许你维护同一工具的不同版本，安装更新并在需要时将其回滚。它还会记住你的 JetBrains 帐户，并使用它在你安装和注册新工具时自动登录。

1. [下载] **Toolbox App**。
2. 启动安装文件。
3. 安装完成后，接受 JetBrains 隐私政策并登录 JetBrains 帐户。

现在你可以管理现有工具、安装新工具和下载更新：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/安装设置/image/toolbox_app.png)


## 静默安装
静默安装，即在没有任何用户界面的情况下执行。网络管理员可以使用它来将 IntelliJ IDEA 安装在多台计算机上，并避免中断其他用户。

要执行静默安装，请使用以下开关运行安装程序：

- **/S：** 启用静默安装
- **/D：** 指定安装目录的路径
- **/CONFIG：** 指定 [silent configuration file] 的路径

比如：

```
ideaIU.exe /S /CONFIG=d:\temp\silent.config /D=d:\IDE\IntelliJ IDEA Ultimate
```

### 静默配置文件
你可以在  [https://download.jetbrains.com/idea/silent.config] 下载 IntelliJ IDEA 的静默配置文件。

*小提示：默认的静默配置文件对每个 JetBrains 产品都是唯一的。 您可以修改它以根据需要启用或禁用各种安装选项。*

静默配置文件定义了用于安装 IntelliJ IDEA 的选项。对于默认选项，静默安装只针对当前用户 **(mode=user)** 执行。如果要为所有用户安装 IntelliJ IDEA，请使用文本编辑器打开静默配置文件，更改安装模式选项 **(mode=admin)** 的值，并作为管理员运行安装程序。


## snap包安装
您可以将 Linux 上的 IntelliJ IDEA 作为自包含的 [snap] 软件包进行安装 ，由于快照会自动更新，你的 IntelliJ IDEA 安装将始终是最新的版本。

*小提示：要使用快照，请按照 [installation guide] 中的描述，在您的机器上安装和运行 __snapd__ 服务。在 Ubuntu 16.04 LTS 及更高版本中，这个服务已预先安装。*

IntelliJ IDEA 通过两种渠道分发：

- 稳定的通道只包括稳定版本。要安装 IntelliJ IDEA 的最新稳定版本，请运行以下命令：

    完全版：
    ```
    $ sudo snap install intellij-idea-ultimate --classic
    ```

   *小提示： `--classic` 选项是必需的，因为 IntelliJ IDEA snap 需要对系统进行完全访问，就像传统的打包应用程序一样。*

    社区版：
    ```
    $ sudo snap install intellij-idea-community --classic
    ```

- 边缘通道包括 EAP 发行版。要安装 IntelliJ IDEA 最新的 EAP 版本，请运行以下命令：

    完整版：
    ```
    $ sudo snap install intellij-idea-ultimate --classic --edge
    ```

    社区版：
    ```
    $ sudo snap install intellij-idea-community --classic --edge
    ```

安装快照时，可以通过运行 **intellij-idea-community** 或 **intellij-idea-ultimate** 命令来启动它。

要列出所有已安装的快照，请运行 **sudo snap list** 。

有关更多信息，请参见 [Snapcraft documentation]。


# ——
**返回** [认识IDEA]

**下一步** [探索]
