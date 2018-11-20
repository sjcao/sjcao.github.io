---
title: Hexo博客NexT主题配置记录
date: 2018-10-18 11:53:59
tags: Hexo
categories: 博客教程
---
记录一些NexT 主题配置
<!--more-->

NexT6.0主题github地址：[https://github.com/theme-next/hexo-theme-next](https://github.com/theme-next/hexo-theme-next)

### 安装NexT主题

------

使用的是Mac环境，打开终端cd到hexo项目的目录,例如我的是`~/develop/hexo`

```
cd ~/develop/hexo
```

使用git把NexT主题克隆到hexo项目的`themes/next`目录下

```
git clone https://github.com/theme-next/hexo-theme-next themes/next
```

修改hexo项目`根目录下的_config.yml`，theme标签改成next

```
theme: next
```

编辑language标签将站点的语言改成中文

```
//从 v6.0.3版本起，`zh-Hans`改名为`zh-CN`
language: zh-CN
```

Ok修改好保存，终端cd 到hexo根目录，重新生成网站并访问 [http://localhost:4000/](http://localhost:4000/) 预览效果

```
cd ~/develop/hexo
hexo clean && hexo g && hexo s
```

### 站点部分配置：

#### 基本配置信息

修改hexo项目`根目录下的_config.yml`，找到Site模块

```
title: 标题
subtitle: 副标题
description: 描述
author: 作者
language: 语言（简体中文是zh-Hans）
timezone: 网站时区（Hexo 默认使用您电脑的时区，不用写）
```

#### 菜单配置

首页、归档、分类、标签、关于等等,需要把前面的#号删掉才能启用该菜单

```
menu:   home: / || home                   //首页
archives: /archives/ || archive          //归档   
categories: /categories/ || th           //分类   
tags: /tags/ || tags                     //标签   
about: /about/ || user                   //关于   
```

更多配置请参考[官方网站](http://theme-next.iissnan.com/getting-started.html#menu-settings)

#### 添加分类模块

新建一个分类页面

```
hexo new page categories
```

你会发现你的`source`文件夹下有了`categorcies/index.md`

打开`index.md`文件，添加字段`type`

```
type: "categories"
```

把文章归入分类只需在创建文章的顶部标题下方添加`categories`字段，即可自动创建分类名并加入对应的分类中。

```
title: 分类测试文章标题
categories: 分类名
```

#### 同理添加标签模块

新建一个标签页面

```
hexo new page tags
```

你会发现你的`source`文件夹下有了`tags/index.md`

打开`index.md`，添加字段`type`

```
type: "tags"
```

添加标签只需要在文字的顶部，添加字段tags，就可以自动把文章通过关键字分类。

```
tags: Hexo
```

#### 同理添加关于界面

新建一个关于页面

```
hexo new page about
```

你会发现你的`source`文件夹下有了`about/index.md`，打开`index.md`文件即可编辑关于你的信息，可以随便编辑。

#### 添加搜索功能

安装==hexo-generator-searchdb==插件

```
npm install hexo-generator-searchdb --save
```

打开`站点配置文件`找到 ==Extensions== 节点，添加搜索插件

```
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

打开`主题配置`文件，找到Local search ，将 enable 设置为 true

其他的更多配置可以[参考官网](http://theme-next.iissnan.com/getting-started.html#menu-settings)