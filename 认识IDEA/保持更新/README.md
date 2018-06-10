[Toolbox]:https://www.jetbrains.com/help/idea/install-and-set-up-product.html#toolbox-app
[apply updates one by one]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#apply_patch
[安装设置]:https://github.com/mrzhqiang/idea-helper/tree/master/认识IDEA/安装设置/
[remove it from the list]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#manage_ignored_updates
[Settings / Preferences Dialog]:https://www.jetbrains.com/help/idea/settings-preferences-dialog.html
[Check for updates manually]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#check_updates
[automatic updates]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#enable_auto_update
[update channel]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#choose_update_channel
[ignored updates]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#manage_ignored_updates
[can receive patch-based updates]:https://www.jetbrains.com/help/idea/keep-product-up-to-date.html#apply_patch
[http://eap.jetbrains.com/]:http://eap.jetbrains.com/

[idea-helper]:https://github.com/mrzhqiang/idea-helper/
[获取帮助]:https://github.com/mrzhqiang/idea-helper/tree/master/认识IDEA/获取帮助/


# 保持更新

## 基本
开箱即用，独立的 IntelliJ IDEA 安装配置为自动检测更新。当有新版本时，将出现通知：

![](https://github.com/mrzhqiang/idea-helper/blob/master/认识IDEA/保持更新/image/ij_update_restart.png)

*小提示：如果你更喜欢集中管理所有的开发人员根据（包括更新它们），请使用 [Toolbox] 应用程序。*

IntelliJ IDEA 通常是基于补丁更新：补丁被应用于现有安装，并且只要求重启 IDE。注意，这些补丁只能按顺序依次应用。如果更新被忽略或跳过，则后续更新无法应用。遇到这种情况，你想要更新到最新的 IntelliJ IDEA，将要重新下载安装，或使用 **Ignored updates** 列表来 [apply updates one by one]。

*小提示：当在 IntelliJ IDEA 中引入重大改变时，你将需要下载安装新的版本，就像在 [安装设置] 中描述的那样。*

如果补丁下载耗时很长，你可以让它进入后台工作。一旦下载完毕，你会收到重启提示，这将完成更新。

如果你出于某种原因不想安装建议的更新，可以通过点击更新对话框中的 **Ignore This Update** 按钮来忽略它。忽略的构建编号将被添加到 **Ignored updates** 列表，并且你将不再被提示安装这个特定构建，直到你 [remove it from the list]。


## 手动管理更新
你可以使用 [Settings / Preferences Dialog] 的 **Updates** 页面来管理 IntelliJ IDEA 更新。

为管理更新，需要执行以下步骤：

1. 通过按下 `Ctrl+Alt+S` 或者选择 Windows 和 Linux 系统下的 **File | Settings** 以及 macOS 系统下的 **IntelliJ IDEA | Preferences** 来打开 [Settings / Preferences Dialog]。展开 **Appearance and Behavior** 节点，并且点击 **Updates** 下面的 **System Settings**。

2. 根据你的需要：
  - [Check for updates manually]。
  - 启用或禁用 [automatic updates]。
  - 选择 [update channel] 你想要接收的更新源。
  - 管理 [ignored updates] 列表。
  - 确保 IntelliJ IDEA [can receive patch-based updates]。

### 检查更新
要检查更新，执行下面的任意一项：
- 点击 **Check Now** 按钮。
- 在主菜单中选择 **Help | Check for Updates**（对于 Windows 或 Linux）或者 **IntelliJ IDEA | Check for Updates**（对于 macOS）。

### 应用自动更新
下面的设置允许你启用自动更新：
- 选择 **Automatically check for updates for** 复选框来启用自动更新，然后从列表中选择所需要的 [update channel]。
- 使用 **Use secure connection** 复选框（默认已选中）在安全连接协议（HTTPS）和 HTTP 协议之间选择下载更新的方式。注意，出于安全因素，HTTP 协议可能被阻塞。

### 选择更新通道
通道列表允许你指定更新哪一个 IntelliJ IDEA 的发布版本。注意，此列表中的 *stable versions* 总是可用的。对于 EAPs，它是强制执行的 *Early Access Program*。

*小提示：有关 __Early Access Program__（ __EAP__）的更多细节，请参阅 [http://eap.jetbrains.com/] 。*

- *Early Access Program*：该通道接收更新，允许您尝试预览 IntelliJ IDEA 版本，并评估将在下一个版本中添加的特性。

  注意事项：
  - IntelliJ IDEA 可以只更新到一个小的而不是主要的 EAP 版本。例如，可以将 IntelliJ IDEA **2017.2.3** 更新为 **2017.2.4 EAP**，但不能更新为 **2017.3 EAP**。本例中的 **2017.3 EAP** 将与已存在的稳定版本并行安装。
  - EAP 版本可以更新为新的 EAP 版本和稳定的 IntelliJ IDEA 版本。如果某个 EAP 版本被更新到一个稳定的版本，那么原始安装目录，即 **%product*-EAP-x** 的名称不会改变。

  *小提示：不建议在产品开发中使用 EAP 版本。*

- *Beta Releases or Public Previews*：这个通道包括候选版本(RC)。
- *Stable Releases*：这个通道包括所有的 IntelliJ IDEA 版本，例如 IntelliJ IDEA X.Y.Z。

### 查看和管理忽略的更新
你可以查看当前已忽略更新的列表，也选择让它们重新下载。

1. 点击 **View/edit ignored updates** 链接。此 **Ignored Updates** 对话框将列出当前被忽略的版本构建编号。
2. 为使某个构建可用，可以从已忽略的列表中删除它。注意，如果你删除了好几个更新，那么最新的更新将提供下载。

### 应用基于补丁的更新
IntelliJ IDEA 补丁是按顺序应用的。例如，如果你正在使用 IntelliJ IDEA **2017.1.1**，可以为它打补丁到 **2017.1.2**，而不能直接到 **2017.1.3**。如果你跳过或忽略更新，将丢失当前 IntelliJ IDEA 安装补丁的能力。因此，当新版本发布时，将提示你下载并安装它。*——它应该指是前面忽略的更新。*

要恢复当前 IntelliJ IDEA 安装基于补丁的更新这个功能，你需要按照以下步骤逐一应用跳过更新:

1. 在更新对话框中，点击 **Ignore This Update** 按钮忽略所推荐的更新。此忽略的构建编号将被添加到 **Ignored updates** 列表。
2. 通过以下任意一项手动地检查可用的更新：
  - 在主菜单上选择 **Help | CHeck for Updates**（对于 Windows 或 Linux）或者 **IntelliJ IDEA | Check for Updates** （对于 macOS）
  - 执行以下步骤：
    - 通过按下 `Ctrl+Alt+S` 或通过选择 **File | Settings**（对于 Windows 和 Linux）或者 **IntelliJ IDEA | Preferences**（对于 macOS）打开 [Settings / Preferences Dialog]。
    - 点击 **Check Now** 按钮。
3. 如果你已跳过单个更新，此更新对话框将立即提示你去更新和重启 IntelliJ IDEA。否则，重复步骤 1 - 2，直到基于补丁的更新能够弹出。
4. 更新和重启 IntelliJ IDEA。
5. 就像 [查看和管理忽略的更新](#查看和管理忽略的更新) 中描述的那样，从 **Ignored updates** 列表中删除忽略构建编号。
6. 再次检查可用的更新。没有忽略的更新现在也可以作为补丁应用。注意，如果你忽略了好几个更新，你需要从最老的更新开始，逐个去移除和应用它们。

# ——
**返回** [idea-helper]

**下一步** [获取帮助]
