# 一个前端的MAC
经常遇到配MAC后不知道如何配环境，或者是要到处在网上找需要安装什么，所以此处列出一个清单。

## 通用
### 1.修改MAC主机名
用惯了terminal, 不想看到XXX@localhost， 可以修改一下主机名

修改为主机名为Superman:

```
sudo scutil --set HostName Superman
```

### 2.修改MAC共享机器名:
不想别人AirDrop时看到的XXX’MAC, 可以设置一下共享机器名 

system -> preference -> sharing

系统 -> 偏好设置 -> 共享

### 3.触摸板
MAC的触摸半绝对是pc中最好用的, 用好了可以不用鼠标了(前端，其它就不清楚了)

- 开启单击轻触
- 双指滚动
- 三指选取移动
- 四指换屏
- 五指显示桌面

### 4.软件

常用

- vmware
- evernote
- qq
- wechat
- xcode
- NeteaseMusic
- thunder
- vlc
- office for mac

偏向开发

- opera
- chrome
  - 插件:switchyomega,可在网上下crx离线文件
  - google账号一个，同步方便
- firefox
  - 插件:autoproxy, ublock,firebug
- mou
- charles
- lanscan pro
- alfred 2
- iterm 2
- spectacle
- photoshop
- dash
- cheatsheet


## 开发
安装前请先弄清楚每个是做什么的，然后有选择性的安装

### 1.MAC上的软件管理器
如ubuntu的apt-get一样，mac上的包管理器Homebrew

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```



### 2.MAC数据库
```
brew install mysql   // mysql
brew install mongodb // mongo
brew install redis   // redis
```

### 3.Web服务器
mac自带的是apache web服务器，但个人还是喜欢nginx的代理设置
nginx: brew install nginx

在terminal运行git
command developer tool

### 4.Terminal设置，不用的话就不用设置了

__推荐使用命令行终端__:iterm2各种分屏等特色功能,然后找个好看的主题

__好用的shell__:oh my zsh

```
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

### 4.使用最新的vim
由于很多插件如css color标识等都需要最新的vim, 所以还是用最新的vim
brew install vim

__替换系统的vim__

1. mv /usr/bin/vim /usr/bin/vim/73
2. 增加 alias vim=‘/usr/local/bin/vim’ 到bash配置文件如 ~/.bash_profile


__vim插件管理器Vundle__

```
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```


## python环境配置
python包管理器pip:

```
sudo easy_install pip
```

python环境配置在特定目录，而不用安装在系统中virtualenv:

```
sudo pip install virtualenv
```

// pip安装python依赖
pip install -r requirements.txt


## 前端

### node相关
```
sudo npm install -g grunt-cli
sudo npm install -g bower
sudo npm install -g jshint
sudo npm install -g yo

npm install -g node-inspector // 调试node代码
sudo npm install -g weinre    // 调试webview的样式及请求很好的一个工具
```

### hybird框架(传说中的全栈全平台前端)

```
sudo npm install -g cordova ionic
sudo npm install -g ios-sim

sudo npm install -g cordova
sudo npm install -g phonegap
```

### css预编译框架

```
sass:sudo gem install sass

compass:sudo gem install compass
```

__安装compass不成功时可修改安装源__:

```
gem sources --remove https://rubygems.org/
gem sources -a https://ruby.taobao.org/
gem sources -l // 如果修改为taobao的安装源则可以重新安装了
```