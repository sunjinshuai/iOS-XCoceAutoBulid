# iOS-XCoceAutoBulid
iOS自动打包

## 前言
这是用Python+xcodebuild写的脚本打包工具，支持上传fir，打包完成后多邮件发送。

### 环境

* Xcode8.3+
* ruby 2.4.1
* rvm 1.29.3+
* 项目使用CocoaPods生成

### AutoBuild.py用法

* 在使用前先把ruby -v 在终端看到下ruby的版本，如果大于2.0.0，需要在终端中运行命令rvm use system（如果没有安装rvm点[这里](https://ruby-china.org/wiki/rvm-guide)）

* 如果要用到fir上传，要先安装[fir-cli](https://github.com/FIRHQ/fir-cli),并且使用fir login + token命令登录（具体用法可以在下载地址查看）

注意：
因为Xcode8.3以后打包的ruby版本要为mac系统的默认版本，而fir-cli插件最低支持的版本为2.3.0，所以在脚本里用了rvm来做版本的切换，需要安装rvm（可以使用在终端命令rvm -v查看是不是安装了rvm），如果安装了，最好下通过下面命令：

```
ruby -v命令查看下ruby的版本
rvm use system 切换到系统版本
```

* 打开conf.ini，设置里面的证书名、描述文件、项目路径等。

* 打开终端，运行命令

```
python 路径+AutoBuild.py
```


