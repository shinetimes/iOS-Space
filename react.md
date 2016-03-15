#React-Native 技术资源

##homebrew
[homebrew](https://github.com/Homebrew/homebrew) OS X 包管理器

[watchman](https://github.com/facebook/watchman) 监视文件变动

[flow](https://github.com/facebook/flow) 类型检查 for JavaScript

```
// 安装
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

// 搜索
brew search ？？

// 安装 git
brew install git

// 安装 watchman
brew install watchman

// 安装 flow
brew install flow

// 更新
brew update && brew upgrade
```

##node
[node.js](https://nodejs.org) 服务器
 
```
node -p process.versions.v8
node -v
```

##npm
[npm.js](https://www.npmjs.com) 包管理

```
sudo npm install npm@latest -g
npm -v
```

##react-native
[react-native](https://github.com/facebook/react-native) APP 开发框架

```
npm install react-native-cli -g
```

##创建项目

```
react-native init my-project
cd my-project
```

解决下载速度问题： 用国内的下载源替换 npmjs.org, 修改以下文件

/usr/local/lib/node_modules/react-native-cli/index.js 将其中的

run('npm install --save react-native', function(e){
   ...
}

npm 更换为 cnpm, 将从淘宝的镜像提取相关的资源



##iOS 出发
用 Xcode 打开 my-project.xcodeproj

编辑代码

command+R 在模拟器内运行

##Android 出发

```
react-native run-android
```

编辑代码

F2 启动，Reload JS 运行
