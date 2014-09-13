Linux Mint 17 Setup
===============

```
Chrome

sudo apt-get install skype

sudo add-apt-repository ppa:git-core/ppa
sudo add-apt-repository ppa:webupd8team/atom
sudo add-apt-repository ppa:webupd8team/java
sudo add-apt-repository ppa:jerzy-kozera/zeal-ppa

sudo apt-get update

sudo apt-get install git atom zeal oracle-java8-installer
sudo apt-get remove default-jre openjdk-7-jre

< set up git (git config xxx)>
git config --global user.name '< your username >'
git config --global user.email '< your email >'
git config --global color.ui true

< set up your github accounts and ssh key >

Atom Packages:
apm install linter linter-jshint editorconfig atom-beautify

IntillJ IDEA

Plugins:
.gitignore support
EditorConfig
NodeJS
AngularJS
Karma

sudo apt-get install fcitx fcitx-bin fcitx-config-common fcitx-config-gtk fcitx-data fcitx-frontend-all fcitx-frontend-gtk2:amd64 fcitx-frontend-gtk3:amd64 fcitx-frontend-qt4:amd64 fcitx-libs:amd64 fcitx-libs-gclient:amd64 fcitx-libs-qt:amd64 fcitx-module-dbus fcitx-module-kimpanel fcitx-module-lua fcitx-module-x11 fcitx-modules fcitx-ui-classic

Sogou Pinyin

NVM:
https://github.com/creationix/nvm

add this code to ~/.bashrc:
source ~/.nvm/nvm.sh

sudo apt-get install fonts-wqy-microhei fonts-wqy-zenhei
```
