# Install and set up IntelliJ IDEA
安装和设置IDEA，这将是你的第一步。

## 安装要求

#### 硬件要求
- 最小1GB内存，推荐2GB内存
- 1.5GB的硬盘空间+至少1GB用于缓存
- 1024 x768最低屏幕分辨率

#### 软件要求
- JRE 1.8与IntelliJ IDEA发行版捆绑在一起。您不需要在计算机上安装Java来运行IntelliJ IDEA
- Java开发需要独立的JDK

**请注意：通常IDEA捆绑的jre（例如..\IntelliJ IDEA 2017.3.2\jre64）会导致输入法无法正常工作，最明显的一个表现是，输入的内容将无法跟随光标。**

###### Windows
Microsoft Windows 10/8/7/Vista/2003/XP (32 or 64 bit)

###### macOS
macOS 10.8 or later (only 64-bit systems are supported)

###### Linux
OS Linux (note that a 32-bit JDK is not bundled, so a 64-bit system is recommended)KDE, Gnome or Unity DE desktop


## 下载和安装
IntelliJ IDEA有两个版本:``Ultimate``和``Community``。

- ``Community``版是一个开源项目，它是免费的，但它的功能更少
- ``Ultimate``版是商业性的，并提供了一套出色的工具和功能

有关详细信息，请参阅[版本比较](https://www.jetbrains.com/idea/features/editions_comparison_matrix.html)。


#### 安装
1. 根据您的操作系统，[下载IDEA](https://www.jetbrains.com/idea/download/index.html)。
2. 在您的操作系统中，执行以下操作：
    - Windows：
        - 运行下载的安装文件，比如：``ideaIC-2017.3.2.exe``或者``ideaIU-2017.3.2.exe``
        - 按照安装向导中的说明操作
    - macOS：
        - 双击``ideaIC.dmg``或者 ``ideaIU.dmg``文件，您已经下载了安装macOS磁盘映像——这句翻译可能不准确
        - 将IDEA复制到``Applications``文件夹
    - Linux：
        - 解压``ideaIC.gz``或``ideaIU.gz``，如果你当前下载文件夹不支持文件执行，你可以下载到一个不同的文件夹：

        ```
        tar xfz ideaIC.tar.gz or ideaIU.tar.gz. <new_archive_folder>
        ```

        推荐的安装位置根据文件系统层次标准(FHS)是``/opt``。例如，可以输入以下命令：
        ```
        sudo tar xf -*.tar.gz -C /opt/
        ```

        - 切换到``bin``目录，比如：

        ```
        cd /opt/-*/bin
        ```

        - 从bin的子目录运行``idea.sh``


## 首次运行

#### 导入设置
当您第一次启动IntelliJ IDEA，或者您从以前的版本升级它之后，``完成安装``的对话框将打开，您可以选择是否要导入IDE设置:
