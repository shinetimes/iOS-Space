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

react-native 会按照你指定的项目名称，创建相应的项目目录

```
react-native init my-project
cd my-project
```

解决下载速度问题，请使用国内的下载源替换 npmjs.org, 修改以下文件：

/usr/local/lib/node_modules/react-native-cli/index.js 将其中的

run('npm install --save react-native', function(e){  
    ...  
}

npm 更换为 cnpm, 将从淘宝的镜像提取相关的资源


##文件注释
.flowconfig 是 Flow 的配置文件  
.gitignore  是 Git 的配置文件  
.watchmanconfig 是 WatchMan 的配置文件  


##iOS 出发
用 Xcode 打开 my-project.xcodeproj

编辑代码：  
index.ios.js 是 iOS 版本的入口文件  
虽然模板生产的结果是 ES5 的代码，你仍然要考虑用 ES6 来开发新的代码

command + R 在模拟器内运行

ios/../AppDelegate.m 是 APP 的代理入口


##Android 出发

```
react-native run-android
```

编辑代码：  
index.android.js 是 Android 版本的入口文件  
虽然模板生产的结果是 ES5 的代码，你仍然要考虑用 ES6 来开发新的代码  

F2 启动，Reload JS 运行


##iOS 版开发
在项目目录下，创建 App 目录作为代码的主要工作目录   
./App/Components 作为项目组件的代码目录  

代码模板通常如下：  
```
import React, {Text, View} from 'react-native'

export default class YourComponent extends React.Component {  
	render() {  
		...  
	}  
}
```

##props
props 是系统的属性清单

this.props.x  x 通常是预设的属性

y = {this.props.x} 通常用于建立绑定

{this.props.x} 通常是从属性清单内取值


##propTypes
propTypes 用于检查输入的值是否类型匹配（防御性编程）


##Navigator
react-nativator 重新实现了 UINavigationController, 这就是 Navigator，它主要用于屏幕自己的导航

initialRoute 定义了初始屏幕  
renderScene 指定函数执行屏幕的切转

navigator.push() 用于屏幕却换

NavigationBar 用户表现导航条

##StyleSheet
界面风格定义组件

```
var styles = StyleSheet.create({


});
```

##AsyncStorage
异步存储

```
async funName() {
try {
await AsyncStorage.setItem(key, value)
} catch(error) {
console.log(',,,,,,')
}
}
```

##用户界面
[react-native-material-design](https://github.com/react-native-material-design/react-native-material-design) Material 风格组件

[react-native-vector-icons](https://github.com/oblador/react-native-vector-icons) 矢量图标

[tcomb-form](https://github.com/gcanti/tcomb-form-native) 表单

[immutable](https://github.com/thewei/react-native-immutable) 集成 immutable.js

##集成
[webpack-starter](https://github.com/jhabdas/react-native-webpack-starter-kit) 使用 webpack

```
git clone https://github.com/jhabdas/react-native-webpack-starter-kit.git native-starter && cd $_

npm install
```

[greenkeeper](https://github.com/greenkeeperio/greenkeeper) 保持 node.js 开发的程序，持续更新到最新版本


##应用
[snowflake](https://github.com/bartonhammond/snowflake)

##运行
在项目的根目录下运行 npm start, 这样，测试时不会引发连接不到服务器的错误

##资源
[react-native](https://js.coach/react-native) 资源清单页


