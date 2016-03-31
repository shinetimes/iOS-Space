##Cocoapods for XCode

[官网](https://github.com/CocoaPods/CocoaPods)

[资源](https://cocoapods.org/)

###Cocoapods 安装
安装 Ruby  

```
sudo gem update --system

// 添加淘宝数据源
gem sources --add https://ruby.taobao.org/

// 安装 Rails 框架
gem install rails
```

安装 Cocoapods

```
sudo gem install -n /usr/local/bin cocoapods

sudo xcode-select --switch /Applications/Xcode.app

pod setup
```

重新安装 Cocoapods

```
pod repo remove master  
pod setup
```

###Cocoapods 使用
进入项目目录

* 使用 search

```
pod search AFNetworking
```

* 设置 podfile

```
touch Podfile

vi Podfile
```

* 添加依赖性

```
platform :ios, '7.0'
pod "AFNetworking", "2.5.0"
```

* 安装依赖项

```
pod install 
```

* 更新依赖性

```
pod update
```


