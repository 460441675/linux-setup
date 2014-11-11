# Ubuntu 14.04 Setup

## 安装

### 下载地址

- [Ubuntu 14.04.1 LTS](http://www.ubuntu.com/download/desktop/thank-you?country=CN&version=14.04.1&architecture=amd64)

### 语言选择

- 为了学习质量和便于适应英文工作环境，请在安装时务必选择英文（美国）版本。

### 制作USB启动盘

- 准备一个容量大于4GB的U盘（请提前将U盘中内容备份，然后使用FAT32格式格式化该U盘）；
- 在Windows操作系统下使用 [Universal USB Installer](http://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) 选择下载的安装镜像（ISO）文件并选择U盘所在盘符制作USB启动盘。

### 安装

**（安装时不要连接互联网，可以大幅度提高安装速度）**

#### 干净安装

直接使用制作好的USB启动盘引导计算机，擦除并使用全部硬盘进行安装（该方法仅适合新电脑或者不准备继续使用Windows且做好备份的情况）。

#### 双系统安装

1. 在Windows操作系统下，使用磁盘工具（推荐使用[EaseUS Partition Master Free](http://www.partition-tool.com/personal.htm)，安装时请仔细看清不要安装任何其捆绑的垃圾软件），在现有硬盘上划分出一个主分区（建议不要小于20GB，推荐60GB）和一个逻辑分区（与电脑内存大小一致）;
2. 使用 [EasyBCD](http://neosmart.net/EasyBCD/) 新建一个名为```Ubuntu```的GRUB2引导项目，并将其位置指定在刚刚新划分出的主分区上；
3. 使用制作好的USB启动盘引导计算机，在安装向导中选择手动硬盘划分，选择新划分出的主分区，选择格式化为Ext4格式，并将```/```根目录指定到该分区上；
4. 选择新划分出的逻辑分区，并制定该分区为Swap分区；
5. 将引导分区盘符指定为新划分出的主分区（**这一步非常重要，切记！**）；
6. 按照安装向导完成后续安装步骤。

## 配置

**（安装有独立安装包的软件时，请优选择64位版本）**

1. 在 Software & Updates 的 Ubuntu Software 选项卡中，将软件源切换至国内服务器（推荐中国科技大学服务器USTC）
2. 在 Software & Updates 的 Other Software 选项卡中勾选 Canonical Partners 源
2. 使用 Software Updater 更新系统（选择并应用全部更新）
3. 在 Mouse & Touchpad 中，将鼠标和触摸板设置为最适合自己使用习惯的选项
4. 在 Language Support 中，根据系统提示安装缺失的语言文件。
6. 安装中文输入法

  ```
  sudo apt-get install ibus-libpinyin
  ```
  注销当前用户并重新登录，在 Text Entry 中添加 Intelligent Pinyin 输入法，并且在输入法设置中关闭 Correct pinyin 功能。
7. 安装[Chrome浏览器](https://www.google.com/intl/en/chrome/browser/?platform=linux)
8. 安装 Flash 插件

  ```
  sudo apt-get install flashplugin-installer
  ```
8. 安装Skype

  ```
  sudo apt-get install skype sni-qt:i386
  ```
9. 安装[uGet](http://ugetdm.com)
  
  ```
  sudo apt-get install aria2 uget
  ```
  安装完成以后请在设置选项中的Plugin面板开启```aria2```支持，这样能够在以后下载时使用多点下载功能。
9. 添加所需要使用的工具的第三方PPA源

  ```
  sudo add-apt-repository ppa:git-core/ppa
  sudo add-apt-repository ppa:webupd8team/atom
  sudo add-apt-repository ppa:webupd8team/java
  sudo add-apt-repository ppa:jerzy-kozera/zeal-ppa
  ```
10. 更新软件包数据并安装所需要使用的工具（cURL、Git、Atom、[Zeal](http://zealdocs.org)、Oracle JDK 8）

  ```
  sudo apt-get update
  sudo apt-get install curl git atom zeal oracle-java8-installer
  ```
11. 安装Atom编辑器的扩展包

  ```
  apm install linter linter-jshint editorconfig atom-beautify
  ```
12. 安装 [IntelliJ IDEA Ultimate Edition](https://www.jetbrains.com/idea/download/) 编辑器
13. 安装 IntelliJ IDEA Ultimate Edition 编辑器插件
  - .gitignore support
  - NodeJS
  - AngularJS
  - Karma
14. 安装[Node Version Manager (NVM)](https://github.com/creationix/nvm#install-script)
15. 在home目录下创建 ```.bashrc``` 文件并添加如下内容

  ```
  source ~/.nvm/nvm.sh
  ```
16. 使用NVM安装NodeJS并设置默认版本
17. 配置Git全局设置参数

  ```
  git config --global user.name '<用户名>'
  git config --global user.email '<电子邮件地址>'
  git config --global color.ui true
  ```
18. 生成SSH密钥并将其注册到GitHub账号
