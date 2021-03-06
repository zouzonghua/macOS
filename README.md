# MacOS 工作环境配置

> 尽量使用开源软件 尽量少装不必要软件 尽量使用自带软件

## 系统设置

- 触摸板轻触和右键: 系统偏好设置 - 触控板 - 光标与点按 - 勾选 `轻点来点按` 和 `辅助点按`（双指点按或轻点）
- 三指拖移: 系统偏好设置 - 辅助功能 - 指针控制 - 触控板选项 - 启用拖移 - 三指拖移
- 取消自动重新排列空间: 系统偏好设置 - 调度中心 - 取消勾选 `根据最近使用情况自动重新排列空间`
- Tab 键移动焦点: 系统偏好设置 - 键盘 - 快捷键 - 全键盘控制 `所有控制`
- 控制音频切换: 系统偏好设置 - 声音 - 在菜单中显示音量
- 修改密码: 系统偏好设置 - 用户与群组 - 更改密码
- 修改用户名: 系统偏好设置 - 用户与群组 - 点击左下角解锁 - 用户名上双指轻点 - 高级选项
- 修改电脑名称: 系统偏好设置 - 共享 - 电脑名称

## 常见问题

- “文件已损坏”?: 终端输入 `sudo spctl --master-disable` ，系统偏好设置 - 安全性与隐私 - 通用 - 允许“任何来源”

## 工具安装

```shell
# 【必装】安装 Homebrew - MacOS包管理器(命令行轻松装软件)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

# 【必装】brew-cask-upgrade - is a command-line tool for upgrading every outdated app installed by Homebrew Cask.
brew tap buo/cask-upgrade

# 【必装】oh-my-zsh - 更强大的终端Shell
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 【必装】z - jump around
git clone https://github.com/rupa/z.git $ZSH_CUSTOM/plugins/z
. $ZSH_CUSTOM/plugins/z/z.sh

# 【必装】zsh-autosuggestions - Fish-like autosuggestions for zsh.
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

# 【必装】zsh-syntax-highlighting - Fish shell like syntax highlighting for Zsh.
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

# 【必装】tmux - is a terminal multiplexer: it enables a number of terminals to be created, accessed, and controlled from a single screen. tmux may be detached from a screen and continue running in the background, then later reattached.
brew install tmux

# 【必装】nnn - nnn (n³) is a full-featured terminal file manager. It's tiny, nearly 0-config and incredibly fast.
brew intasll nnn

# 【必装】unrar - 解压RAR工具
brew install carlocab/personal/unrar

# 【必装】AdoptOpenJDK - 是一个由OpenJDK构建，并以免费软件的形式提供社区版的 OpenJDK 二进制包。 它至少提供 4 年的免费长期支持(LTS)。 CentOS7.5和EulerOS2.8操作系统在鲲鹏生态中可以完整运行AdoptOpenJDK的全部功能。
brew tap AdoptOpenJDK/openjdk
brew install adoptopenjdk8

# 【必装】docker - Docker 是一个开放源代码软件，是一个开放平台，用于开发应用、交付应用、运行应用。 Docker允许用户将基础设施中的应用单独分割出来，形成更小的颗粒，从而提高交付软件的速度。 Docker容器与虚拟机类似，但二者在原理上不同。
brew install --cask docker

# 【必装】nvm - 管理多个Node版本的工具。
brew install nvm

# 【必装】Node.js® - 是一个基于Chrome V8 引擎 的JavaScript 运行时。
nvm install --lts

# 【必装】 yarn - 快速、可靠、安全的依赖管理工具。
npm i -g yarn

# 【必装】MongoDB - 是一种面向文档的数据库管理系统，用C++等语言撰写而成，以解决应用程序开发社区中的大量现实问题。
brew tap mongodb/brew
brew install mongodb-community
brew services start mongodb-community

# 【必装】MySQL - MySQL 是最流行的关系型数据库管理系统，在 WEB 应用方面 MySQL 是最好的 RDBMS(Relational Database Management System：关系数据库管理系统)应用软件之一。。
brew install mysql@5.7

# 【必装】Robo 3T - Native cross-platform MongoDB management tool.
brew install --cask robo-3t

# 【必装】Sequel Pro - is a fast, easy-to-use Mac database management application for working with MySQL databases.
brew install --cask homebrew/cask-versions/sequel-pro-nightly

# 【必装】VMware Fusion - VMware Fusion是VMware为苹果电脑开发的虚拟机程序，它允许用户在中央处理器为英特尔的苹果电脑的MacOS操作系统上运行其他操作系统，例如Microsoft Windows、Linux、NetWare、Solaris等。VMware Fusion 1.0于2007年8月6日发布。
 brew install vmware-fusion

# 【必装】Google Chrome - 是由Google开发的免费网页浏览器。
brew install --cask google-chrome

# 【必装】Visual Studio Code - is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux. It comes with built-in support for JavaScript, TypeScript and Node.js and has a rich ecosystem of extensions for other languages (such as C++, C#, Java, Python, PHP, Go) and runtimes (such as .NET and Unity).
brew install --cask visual-studio-code

# 【必装】IntelliJ IDEA - 是一种商业化销售的Java集成开发环境工具软件，由JetBrains软件公司开发，提供Apache 2.0开放式授权的社区版本以及专有软件的商业版本，开发者可选择其所需来下载使用。
brew install --cask intellij-idea-ce

# 【必装】Android Studio是一个为Android平台开发程序的集成开发环境。2013年5月16日在Google I/O上发布，可供开发者免费使用。 2013年5月发布早期预览版本，版本号为0.1。2014年6月发布0.8版本，至此进入beta阶段。第一个稳定版本1.0于2014年12月8日发布。
brew install --cask android-studio

# 【必装】Typora - 是一款支持实时预览的Markdown 文本编辑器。
brew install --cask typora

# 【必装】react-native-debugger - The standalone app based on official debugger of React Native, and includes React Inspector / Redux DevTools
brew install --cask react-native-debugger

# 【必装】wechatwebdevtools - 微信开发者工具，集成了公众号网页调试和小程序调试两种开发模式。
brew install --cask wechatwebdevtools

# 【必装】wechat - 一款跨平台的通讯工具。支持单人、多人参与。通过手机网络发送语音、图片、视频和文字。
brew install --cask wechat

# 【必装】qq - I'm QQ - 每一天，乐在沟通。
brew install --cask qq

# 【必装】tencent-lemon - 全新Mac清理工具，实时了解Mac系统状况。
brew install --cask tencent-lemon

# 【必装】neteasemusic - 网易云音乐是一款专注于发现与分享的音乐产品，依托专业音乐人、DJ、好友推荐及社交功能，为用户打造全新的音乐生活。
brew install --cask neteasemusic

# 【必装】wpsoffice - Free Editor for all-in-one Office Suite: Word, PDF, Excel, PowerPoint with wonderful editing experience.
brew install --cask wpsoffice

# 【必装】dingtalk - Ding Talk, Make Work and Study Easy
brew install --cask dingtalk

# 【必装】IINA - is born to be a modern macOS application, from its framework to the user interface. It adopts the post-Yosemite design language of macOS and keeps up the pace of new technologies like Force Touch, Touch Bar, and Picture-in-Picture.
brew install --cask iina

# 【必装】Rectangle - Move and resize windows in macOS using keyboard shortcuts or snap areas.
brew install --cask rectangle

# 【必装】V2rayU - 基于v2ray核心的mac版客户端,用于科学上网,使用swift编写,支持vmess,shadowsocks,socks5等服务协议,支持订阅, 支持二维码,剪贴板导入,手动配置,二维码分享等
brew install --cask v2rayu

# 【必装】Tunnelblick - Tunnelblick是OS X和macOS上用于OpenVPN（虚拟专用网络）的免费开源图形用户界面。它提供对OpenVPN客户端和/或服务器连接的轻松控制。
brew install --cask tunnelblick

# 【必装】bob - Bob 是一款 Mac 端翻译软件，翻译方式支持划词翻译和截图翻译，翻译引擎支持有道翻译、百度翻译和谷歌翻译。
brew install --cask bob

# 【必装】istat-menus - istat-menus  An advanced Mac system monitor for your menubar
brew install --cask istat-menus

# 【必装】hiddenbar - An ultra-light MacOS utility that helps hide menu bar icons
brew install --cask hiddenbar

# 【必装】Mos - A lightweight tool used to smooth scrolling and set scroll direction independently for your mouse on macOS
brew install --cask mos

# 【必装】HandShaker - Manage Your Android Phones at Ease 
brew install --cask handshaker

```

## 开发相关

```shell
# 脚本安装 vim 配置
sh <(curl -L https://github.com/zouzonghua/vim/raw/main/utils/install.sh)

# 更新所有软件和开发包并删除过期包
brew update && brew upgrade && brew cu -a -y && brew cleanup && brew cleanup --prune 0
alias brewUpdate='brew update && brew upgrade && brew cu -a -y && brew cleanup && brew cleanup --prune 0'

# 生成 ssh key 并加入 git 账户
ssh-keygen # 一路回车即可

# 粘贴到自己 git 账号设置里的 ssh-key
cat ~/.ssh/id_rsa.pub | clipcopy

# 配置用户信息
git config --global user.name "zouzonghua"
git config --global user.email "zouzonghua.cn@gmail.com"

# 粘贴到终端配置 ssh 免密登陆服务器
ssh-copy-id -i ~/.ssh/id_rsa.pub -p 22 root@www.zouzonghua.cn
```
## 配置文件

- [zsh](https://github.com/zouzonghua/.config/blob/main/.zshrc)
- [tmux](https://github.com/zouzonghua/.config/blob/main/.tmux.conf)
- [vim](https://github.com/zouzonghua/vim)
