# Flutter安装

## Fluter

将下面的命令加入到`.zshrc`中

```shell
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

找到下载链接，比如`https://storage.googleapis.com/flutter_infra/releases/stable/macos/flutter_macos_v1.12.13+hotfix.5-stable.zip`，将其中的`storage.googleapis.com`替换为`storage.flutter-io.cn`，得到`https://storage.flutter-io.cn/flutter_infra/releases/stable/macos/flutter_macos_v1.12.13+hotfix.5-stable.zip`，使用这个链接下载即可。

在`~`目录下创建一个目录`.flutter`，进入这个目录，解压flutter。`unzip ~/Downloads/flutter_macos_v1.12.13+hotfix.5-stable.zip`

__大坑！！！，不能使用`.flutter`目录，[issue](https://github.com/flutter/flutter/issues/25089)__

后面改为在家目录下直接解压。记得删除`.flutter`目录

将`export PATH="$PATH:/Users/blue/flutter/bin"`添加到`.zshrc`中。

运行`flutter doctor`检查一下是否安装成功。

## iOS

### 安装Xcode

在App Store上直接下载最新版的`Xcode`。
运行下面的命令

```shell
 sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
 sudo xcodebuild -runFirstLaunch
```

### 安装iOS模拟器

`open -a Simulator`

### 创建和运行一个简单的Flutter app

`flutter create my_app`

`cd my_app`

`flutter run`

### 发布到真机

`sudo gem install cocoapods`
`pod setup`

- 在项目目录中`open ios/Runner.xcworkspace`
- 连上手机，选择目标手机
- 点击Runner
- Signing & Capabilities > Team，登录iOS账号，选择信任。General > Identity > Bundle Identifier 要唯一
- `flutter run`
