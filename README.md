```
    _       _
  ┏┛ ┻━━━━━┛ ┻┓     
  ┃　　　　　　 ┃            
  ┃　　　━　　　┃               
  ┃　┳┛　  ┗┳　┃           
  ┃　　　　　　 ┃            
  ┃　　　┻　　　┃             
  ┃　　　　　　 ┃         
  ┗━┓　　　┏━━━┛              
    ┃　　　┃         
    ┃　　　┃               
    ┃　　　┗━━━━━━━━━┓          
    ┃　　            ┣┓       
    ┃　              ┏┛       
    ┗━┓ ┓ ┏━━━┳ ┓ ┏━┛           
      ┃-┫-┫   ┃-┫-┫         
      ┗-┻-┛   ┗-┻-┛   
```

# React Native 环境搭建

## xcode
> xcode-select --install

## homebrew
> /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
>> 查看版本 :
>>> brew -v

## 常用工具插件
```
  $ brew install watchman
      watchman : 监视并记录文件的改动
  $ brew install flow
      flow : 检查文件js文件错误
  $ brew install git
      git : 代码管理工具
  $ brew install gcc
      gcc : c程序的编译器
  $ brew install pkg-config
      pkg-config : 向用户向程序提供相应库的路径、版本号等信息的程序
  $ brew install cairo
      cairo : 2D图形库
  $ brew install libpng
      libpng : 多种应用程序使用的解析PNG图象格式的库
  $ brew install jpeg
      jpeg : 对图片处理
  $ brew install gitlib
      gitlib : 搭建本地的git服务器
  $ brew install mongodb
      mongodb : 非关系型数据库
```

## nvm 安装（node版本管理）
> curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash
>> 安装node版本 :
>>> nvm install v4.2.3
>>>> 设置 node 默认版本 :
>>>>>  nvm alias default v4.2.3
```
  问题 ： nvm is not found 相关
  解决方案 ：
    source ~/.nvm/nvm.sh
    source ~/.profile
    source ~/.bashrc
```

## cnpm 安装
> npm install cnpm -g
>> -or-
>>> sudo npm install -g cnpm --registry=https://registry.npm.taobao.org

## 安装RN
> npm install -g create-react-native-app


## 脚手架工具 react-native-cli
> cnpm install -g react-native-cli@0.1.10
>> react-native-cli 版本:
>>> react-native -v  

## react-native-cli 初始化项目
> react-native init 项目名

## 运行IOS
> cd 项目名
  >> react-native run-ios
```
  -or-
  Open ios/项目名.xcodeproj in Xcode
  Hit the Run button

  报错：
    xcrun: error: unable to find utility "instruments", not a developer tool or in PATH
  解决方法：
    sudo xcode-select -s /Applications/Xcode.app/Contents/Developer/

  调整simulator界面大小：
    command+1、command+2、command+3、command+4

```

## 运行Android
> cd 项目名
>> react-native run-android
```
  Have an Android emulator running (quickest way to get started), or a device connected
```

## 项目目录说明
```
|- _tests_
  |- App.js
|- android
  |- app
  |- gradle
  |- keystores
  ...
|- ios
  |- build
  |- lenjeeReactNative
  |- lenjeeReactNative-tvOS
  |- lenjeeReactNative-tvOSTests
  |- lenjeeReactNative.xcodeproj
  |- lenjeeReactNativeTests
|- node_modules
|- .babelrc
|- .buckconfig
|- .flowconfig
|- .gitattributes
|- .gitignore
|- .watchmanconfig
|- App.js
|- app.json
|- index.js 入口文件
|- package-lock.json
|- package.json 配置文件
|- README.md
```

## 修改项目默认端口号
> react-native start --port 9999

# Flexbox布局
```
  React Native中的Flexbox的工作原理和web上的CSS基本一致，当然也存在少许差异。
    flexDirection的默认值是column而不是row
    flex只能指定一个数字值

  flexDirection
    可以决定布局的主轴(子元素是应该沿着水平轴(row)方向排列，还是沿着竖直轴(column)方向排列)

  justifyContent
    决定其子元素沿着主轴的排列方式

  alignItems
    决定其子元素沿着次轴（与主轴垂直的轴，比如若主轴方向为row，则次轴方向为column）的排列方式
```

# React Native控件
