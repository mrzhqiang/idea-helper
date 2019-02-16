---
layout: default
title: 安装和设置
parent: 遇见 IDEA
nav_order: 1
permalink: /meet/install-and-set-up
---


# 安装和设置
{: .no_toc }
原文：[Install and set up IntelliJ IDEA]。

## 目录
{: .no_toc .text-delta }

- TOC
{:toc}

---

## 安装要求
### 硬件要求
\- 最小 2GB 内存，推荐 4GB 内存

\- 1.5GB 的硬盘空间 + 至少 1GB 用于缓存

\- 最小屏幕分辨率为 1024 x768

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——缓存实际上就是硬盘空间
</span>

### 软件要求
JRE 1.8 与 IntelliJ IDEA 发行版捆绑在一起，您不需要在计算机上安装 Java 来运行 IntelliJ IDEA。

独立的 JDK 是用来开发 Java 程序。

| Windows | macOS | Linux |
|:--------|:-----:|:------|
| 32 位或 64 位版本 Windows 10, 8, 7 (SP1)，或者 Vista (SP2) | macOS 10.8.3 或者更高版本（仅支持 64 位系统）| - OS Linux （注意，32 位 JDK 未捆绑，所以推荐使用 64 位系统）<br> - 推荐使用 KDE，Gnome 或 Unity 桌面环境 |

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——IntelliJ IDEA 捆绑的 JRE（例如..\IntelliJ IDEA 2017.3.2\jre64）有可能导致中文输入法的候选框不跟随光标。为解决这个问题，可以通过修改 \jre64 目录为其他名字，比如 \jre641，然后 IntelliJ IDEA 会寻找系统级别的 JRE 环境，此时你必须同时安装 JDK 和 JRE。
</span>

---

## 下载和安装
IntelliJ IDEA 有两个版本：**Ultimate** 和 **Community**。**Community** 是一个免费的开源项目，它的功能较少。**Ultimate** 是商业的，它提供了一套优秀的工具集和功能。有关详细信息，请参阅 [editions comparison matrix]。

要安装 IntelliJ IDEA：

1. 为您指定的操作系统 [下载 IntelliJ IDEA]。

2. 根据您的操作系统，执行以下操作：

    \- **Windows**：
    1. 运行已下载的 **ideaIC.exe** 或 **ideaIU.exe** 文件。
    2. 按照安装向导中的说明进行操作。

    \- **macOS**：
    1. 双击已下载的 **ideaIC.dmg** 或 **ideaIU.dmg** 文件以装入 macOS 磁盘映像。
    2. 复制 IntelliJ IDEA 到 **Applications** 文件夹。

    \- **Linux**：
    1. 解压已下载的 **ideaIC.gz** 或 **ideaIU.gz** 文件，如果当前 **Downloads** 目录没有文件执行权限，你可以解压到其他目录：
        ```bash
        tar xfz ideaIC.tar.gz or ideaIU.tar.gz. <new_archive_folder>
        ```
        根据文件系统层次结构标准（FHS）推荐的安装位置是 **/opt**。例如，可以输入以下命令：
        ```bash
        sudo tar xf -*.tar.gz -C /opt/
        ```
    2. 切换到 **bin** 目录，比如：
        ```
        cd /opt/-*/bin
        ```
    3. 从 **bin** 的子目录运行 **idea.sh**。

<span class="d-inline-block p-3 bg-yellow-000">
注意：32 位系统的 JRE 未和 IntelliJ IDEA 捆绑在一起。如果您使用的是 32 位版本的 Windows，请勾选安装向导中的 __Download and install JRE x86 by Jetbrains__ 复选框，以便自动下载和安装 JRE。
</span>

<span class="d-inline-block p-3 bg-yellow-000">
注意：新实例不能从现有的实例中提取。目标文件夹必须为空。
</span>

---

## 首次运行
### 导入设置
当你首次启动 IntelliJ IDEA 时，或者你从上一个版本升级之后，将打开 **Complete Installation** 对话框，你可以在其中选择是否要导入 IDE 设置：

![]({{ site.baseurl }}{% link assets/images/complete-installation.png %})

如果这是你的第一个 IntelliJ IDEA 实例，请选择 `Do not import settings` 选项。

<span class="d-inline-block p-3 bg-yellow-000">
注意：您稍后可以使用在主菜单上的 `File | Import Settings` 和 `File | Export Settings` 命令，手动 [import and export settings]。
</span>

### 选择用户界面主题
接下来，系统会提示你选择 UI 主题，你可以在 **Default** 和 **Darcula** 主题之间进行选择：

![]({{ site.baseurl }}{% link assets/images/customize-idea.png %})

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——`Darcula` 主题更舒服一些，保护眼睛，拒绝亮色系。
</span>

### 禁用不必要的插件
IntelliJ IDEA 装载了各种插件，可与不同的版本控制系统和应用程序服务器进行集成，增加对各种框架和开发技术的支持等。

下一步，为增加 IntelliJ IDEA 的性能，您可以禁用不需要的插件。如有必要，你可以稍后在 **Settings** 对话框中重新启用它们（`Ctrl+Alt+S` 下的 **Plugins**）。

![]({{ site.baseurl }}{% link assets/images/default-plugins.png %})

你可以点击每个插件组的 **Disable All** 链接来禁用所有插件，或者点击 **Customize** 禁用单个插件。

### 下载并安装其他插件
下一步，系统会提示你从 [IntelliJ IDEA plugins repository] 下载未捆绑在 IDE 中的其他插件：

![]({{ site.baseurl }}{% link assets/images/ij_set_featured_plugins.png %})

### 启动一个项目
完成初始化 IntelliJ IDEA 的配置后，有一个 **Welcome** 屏幕将显示出来，它允许你：

\- [create a new project]

\- 或 [check out an existing project from a version control system (clone from a remote repository)]

<span class="d-inline-block p-3 bg-grey-lt-000">
提示：也可以将现有项目目录或单独的文件拖到 `Welcome` 屏幕，就可以在 IntelliJ IDEA 中将其打开。
</span>

![]({{ site.baseurl }}{% link assets/images/ij_welcomeScreen.png %})

你可以观看关于如何首次运行 IntelliJ IDEA 的快速视频教程。

<iframe width="600" height="400" src="https://www.youtube.com/embed/c0efB_CKOYo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——视频需要科学上网才能观看。
</span>

如果您想快速了解 IntelliJ IDEA 的主要功能以及如何使用它们，请参考 [探索][13] 部分。

---

## 注册
想要尝试和评估 IntelliJ IDEA，你可以免费下载并安装试用版。试用版可以使用 30 天，因此您需要获得并注册许可证。

<span class="d-inline-block p-3 bg-yellow-000">
注意：IntelliJ IDEA 构建可以作为 [Early Access Program] 的部分进行下载，不需要注册，并且附带 30 天的许可认证。
</span>

<span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
——这里描述的是 `Ultimate` 版本
</span>

1. 执行以下操作之一：

    \- 在 **Welcome** 屏幕上，点击 **Configure丨Manage License**
    
    \- 从主菜单中选择 **Help丨Register**

    ![]({{ site.baseurl }}{% link assets/images/ij_register.png %})
    
    <span class="d-inline-block p-3 text-green-200 bg-grey-lt-200">
    ——图片中的地址不确定是否可用，需要永久使用的同学，百度 `IDEA lanyu` 即可。
    </span>

2. 选择你想要注册 IntelliJ IDEA 的方式：

    | 选项 | 描述 |
    |:-----|:-----|
    |**JetBrains Account**|使用 [JetBrains Account] 注册。<br>参阅 [What is JetBrains Account?] 了解更多信息。|
    |**Activation code**|使用激活码注册。|
    |**License server**|使用 [License Server] 注册。<br>要在初始 IntelliJ IDEA 启动期间覆盖系统代理的 URL，请使用 `-Djba.http.proxy` 属性，该属性可以添加为 [JVM option]。<br>在多台计算机上执行静默安装或管理 IntelliJ IDEA 安装时，可以设置 **JETBRAINS_LICENSE_SERVER** 环境变量以将安装指向许可证服务器 URL。|

如果您的插件需要许可证，则可以从主菜单上点击 **Help丨Licenses** 打开 **Licenses** 对话框，而不是 **License Activation** 对话框。

![]({{ site.baseurl }}{% link assets/images/Licenses_Dialog.png %})

**Licenses** 对话框包含许可证列表并显示其状态：

\- *Expired*：续订许可证以继续。

\- *Grace period*：距离许可证到期还有几天。

\- *Evaluation period*：使用过期许可证。

\- *Active license*：使用直到失效日期。

要配置许可证，请单击 **Edit** 按钮，这将打开 **License Activation** 对话框。

---

## 更新
开箱即用，独立的 IntelliJ IDEA 会被配置为自动检查更新。当有一个新版本可用时，它会自动通知你：

![]({{ site.baseurl }}{% link assets/images/ij_update_restart.png %})

<span class="d-inline-block p-3 bg-grey-lt-100">
提示：如果您更喜欢集中管理所有开发人员工具（包括更新它们），请使用 [工具箱管理](#六、工具箱管理) 。
</span>

IntelliJ IDEA 更新通常是 *patch-based*（基于补丁的）：它们被应用于现有安装，并只需要你重启 IDE。

<span class="d-inline-block p-3 bg-yellow-000">
注意：主要版本之间不提供补丁更新。更新到新的主要版本（例如，从 2018.1 到 2018.2）时，必须按照 [安装和设置][11] 中的说明单独下载和安装。
</span>

如果修补程序的下载需要很长时间，则可以将其发送到后台并继续工作。下载完成后，系统会提示您重新启动，以完成更新。

出于某种原因，你不想安装建议的更新，你可以在更新对话框中，点击 **Ignore This Update** 按钮来忽略它。被忽略的版本号将被添加到 **被忽略的更新** 列表中，并且不会提示你安装这个特定版本，除非您 [remove it from the list]。

---

## 管理工具箱
**Toolbox App** 是一个控制面板，允许你从单一访问点管理所有 JetBrains 开发人员工具，包括 IntelliJ IDEA 以及你的项目。它允许你维护同一工具的不同版本，安装更新并在需要时将其回滚。它还会记住你的 JetBrains 帐户，并使用它在你安装和注册新工具时自动登录。

1. [下载 Toolbox App]。
2. 启动安装文件。
3. 安装完成后，接受 JetBrains 隐私政策并登录 JetBrains 帐户。

现在你可以管理现有工具、安装新工具和下载更新：

![]({{ site.baseurl }}{% link assets/images/toolbox_app.png %})

---

## 在 Windows 上进行静默安装
静默安装，即在没有任何用户界面的情况下执行。网络管理员可以使用它来将 IntelliJ IDEA 安装在多台计算机上，并避免中断其他用户。

要执行静默安装，请使用以下开关运行安装程序：

\- **/S**： 启用静默安装

\- **/D**： 指定安装目录的路径

\- **/CONFIG**： 指定 [silent configuration file] 的路径

比如：

```bash
ideaIU.exe /S /CONFIG=d:\temp\silent.config /D=d:\IDE\IntelliJ IDEA Ultimate
```

<span class="d-inline-block p-3 bg-yellow-000">
注意：要在安装过程中检查问题，请添加带有日志文件路径和名称的 **/LOG** 开关。安装程序将生成指定的日志文件。例如：**/LOG=d:\JetBrains\IDEA\install.log**。
</span>

### 静默配置文件
你可以在 [https://download.jetbrains.com/idea/silent.config] 下载 IntelliJ IDEA 的静默配置文件。

静默配置文件定义了用于安装 IntelliJ IDEA 的选项。对于默认选项，静默安装只针对当前用户 **(mode=user)** 执行。如果要为所有用户安装 IntelliJ IDEA，请使用文本编辑器打开静默配置文件，更改安装模式选项 **(mode=admin)** 的值，并作为管理员运行安装程序。

<span class="d-inline-block p-3 bg-yellow-000">
默认的静默配置文件对于每个 JetBrains 产品都是唯一的。您可以根据需要对其进行修改以启用或禁用各种安装选项。
</span>

### 静默卸载
要以静默方式卸载 IntelliJ IDEA，请以管理员身份使用 **/S** 开关运行卸载程序。卸载程序位于 `bin` 下的安装目录中。

以管理员身份运行 **cmd**（Windows命令提示符），切换到 IntelliJ IDEA 安装目录，然后运行以下命令：

```bash
bin\uninstall.exe /S
```

---

## 在 Linux 上作为 snap 包安装
您可以将 Linux 上的 IntelliJ IDEA 作为自包含的 [snap] 软件包进行安装 ，由于快照会自动更新，你的 IntelliJ IDEA 安装将始终是最新的版本。

<span class="d-inline-block p-3 bg-yellow-000">
注意：要使用快照，请按照 [installation guide] 中的描述，在您的机器上安装和运行 __snapd__ 服务。在 Ubuntu 16.04 LTS 及更高版本中，这个服务已预先安装。
</span>

IntelliJ IDEA 通过两种渠道分发：

\- *stable* 渠道只包括稳定版本。要安装 IntelliJ IDEA 的最新稳定版本，请运行以下命令：

- **Ultimate Edition**：
```bash
$ sudo snap install intellij-idea-ultimate --classic
```

- **Community Edition**：
```bash
$ sudo snap install intellij-idea-community --classic
```

\- *edge* 渠道包括 EAP 发行版。要安装 IntelliJ IDEA 最新的 EAP 版本，请运行以下命令：

- **Ultimate Edition**：
```bash
$ sudo snap install intellij-idea-ultimate --classic --edge
```

- **Community Edition**：
```bash
$ sudo snap install intellij-idea-community --classic --edge
```

安装快照时，可以通过运行 **intellij-idea-community** 或 **intellij-idea-ultimate** 命令来启动它。

要列出所有已安装的快照，请运行 **sudo snap list** 。有关更多信息，请参见 [Snapcraft documentation]。

<span class="d-inline-block p-3 bg-yellow-000">
注意：`--classic` 选项是必需的，因为 IntelliJ IDEA 快照需要对系统进行完全访问，就像传统的打包应用程序一样。
</span>



[Install and set up IntelliJ IDEA]:https://www.jetbrains.com/help/idea/install-and-set-up-product.html

[editions comparison matrix]:https://www.jetbrains.com/idea/features/editions_comparison_matrix.html
[下载 IntelliJ IDEA]:https://www.jetbrains.com/idea/download/index.html
[import and export settings]:https://www.jetbrains.com/help/idea/exporting-and-importing-settings.html
[IntelliJ IDEA plugins repository]:https://plugins.jetbrains.com/idea
[create a new project]:https://www.jetbrains.com/help/idea/configuring-projects.html#working-with-projects
[check out an existing project from a version control system (clone from a remote repository)]:https://www.jetbrains.com/help/idea/version-control-with-intellij-idea.html
[Early Access Program]:https://www.jetbrains.com/community/eap/
[JetBrains Account]:https://account.jetbrains.com/login
[What is JetBrains Account?]:https://sales.jetbrains.com/hc/en-gb/articles/208459005-What-is-JetBrains-Account-
[License Server]:https://www.jetbrains.com/help/license_server/getting_started.html
[JVM option]:https://www.jetbrains.com/help/idea/tuning-the-ide.html#configure-jvm-options
[remove it from the list]:https://www.jetbrains.com/help/idea/keep-intellij-idea-up-to-date.html#manage_ignored_updates
[下载 Toolbox App]:https://www.jetbrains.com/toolbox/app/
[silent configuration file]:https://www.jetbrains.com/help/idea/install-and-set-up-intellij-idea.html#silent-config
[https://download.jetbrains.com/idea/silent.config]:https://download.jetbrains.com/idea/silent.config
[snap]:https://snapcraft.io/
[installation guide]:https://docs.snapcraft.io/core/install
[Snapcraft documentation]:https://docs.snapcraft.io/

[11]:{{ site.baseurl }}{% link docs/meet/install-and-set-up.md %}
[13]:{{ site.baseurl }}{% link docs/meet/discover.md %}