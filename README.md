# Linux Mint 17 Setup

1. 安装Chrome浏览器
2. 安装Skype

  ```
  sudo apt-get install skype
  ```
3. 添加所需要使用的工具的第三方PPA源

  ```
  sudo add-apt-repository ppa:git-core/ppa
  sudo add-apt-repository ppa:webupd8team/atom
  sudo add-apt-repository ppa:webupd8team/java
  sudo add-apt-repository ppa:jerzy-kozera/zeal-ppa
  ```
4. 更新软件包数据并安装所需要使用的工具

  ```
  sudo apt-get update
  sudo apt-get install git atom zeal oracle-java8-installer
  sudo apt-get remove default-jre openjdk-7-jre
  ```
5. 配置Git全局设置参数

  ```
  git config --global user.name '<用户名>'
  git config --global user.email '<电子邮件地址>'
  git config --global color.ui true
  ```
6. 生成SSH密钥并将其注册到GitHub账号
7. 安装Atom编辑器的扩展包

  ```
  apm install linter linter-jshint editorconfig atom-beautify
  ```
8. 安装 IntelliJ IDEA 编辑器
9. 安装 IntelliJ IDEA 编辑器插件
  - .gitignore support
  - EditorConfig
  - NodeJS
  - AngularJS
  - Karma
10. 安装搜狗输入法依赖包

  ```
  sudo apt-get install fcitx fcitx-bin fcitx-config-common fcitx-config-gtk fcitx-data fcitx-frontend-all fcitx-frontend-gtk2:amd64 fcitx-frontend-gtk3:amd64 fcitx-frontend-qt4:amd64 fcitx-libs:amd64 fcitx-libs-gclient:amd64 fcitx-libs-qt:amd64 fcitx-module-dbus fcitx-module-kimpanel fcitx-module-lua fcitx-module-x11 fcitx-modules fcitx-ui-classic
  ```
11. 安装搜狗输入法
12. 安装NVM

  https://github.com/creationix/nvm
13. 在home目录下创建 ```.bashrc``` 文件并添加如下内容

  ```
  source ~/.nvm/nvm.sh
  ```
14. 使用NVM安装NodeJS并设置默认版本
15. 安装文泉驿微米黑和文泉驿正黑字体解决界面中文缺失问题

  ```
  sudo apt-get install fonts-wqy-microhei fonts-wqy-zenhei
  ```

