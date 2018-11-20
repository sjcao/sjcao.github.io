---
title: AndroidJetpack
date: 2018-11-20 09:12:08
tags:
- Android
- Android JetPack
categories:
- Android JetPack总结
---
关于Android JetPack的一些总结。
<!--more-->
Jetpack是一个Android软件组件的集合，JetPack可以让开发出高质量的Android apps更加的容易。这些组件能帮助你遵循最佳的实践，释放你的双手去写一些模块化的代码，或者一些复杂的任务，你就可以把精力放在创建你自己的代码身上。
Jetpack包括 `androidx.*` 依赖包，从Android的平台APIs分离出来，这就意味着能提供向下的兼容性，并且会比Android平台更新得更加频繁，请确保你总是能获取到最新的或者最好的 Jetpack 组件。



JetPack包含四大部分

#### 1.Foundation 基础组件：

AppCompat： 兼容旧的Android版本的组件 

Android KTX： 基础Kotlin语言的一些方便快捷的工具

Multdex：提供支持multiple DEX files

Test: 单元测试或者UI测试等

#### 2.Architecture 构建组件：

Data Binding： 绑定可观察的数据到UI元素上

Lifecycles： 管理你的Activity和Fragment的生命周期

#### LiveData： 当数据改变时，可自动通知视图更新

Navigation： 处理Activity、Fragment等的跳转导航

Paging： 逐步从加载源加载数据

Room： 流畅通过SQLite数据库获取数据

ViewModel： 以生命周期的意识管理UI相关的数据

WorkManager： 管理你的后台运行的工作

#### 3.Behavior 行为组件可以与标准的Android服务集成、如通知、权限、分享、助手

#### Download manager： 处理大文件的下载

Media & playback：向后兼容的媒体播放组件

Notifications： 提供向后兼容的通知API，支持Wear 和 Anto

Permissions： 向后兼容的检查和请求权限

Sharing： 提供适合应用操作栏的分享操作

Slices： 创建可在应用程序外部显示应用程序的灵活UI元素

Preferences： 创建可交互的屏幕设置

#### 4.UI UI组件提供小部件帮助程序，使你的应用程序不仅简单而且使用起来很愉快

Animation & transitions： 移动组件和切换屏幕的动画

Auto：开发自动的App、用于汽车类的自动操作

Emoji：在比较旧的平台上启用最新的表情符号字体

Fragment：可组合的UI基本单元

Layout：使用不同的类型布置组件

Palette：调色板

TV：TV应用开发

Wear OS by Google：开发Wear组件

##### 

这里先做一个官网的简单翻译，官网详情：[https://developer.android.google.cn/jetpack/](https://developer.android.google.cn/jetpack/)

