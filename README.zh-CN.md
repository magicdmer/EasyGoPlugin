# EasyGo 快捷启动

[![Join the chat at https://gitter.im/magicdmer/EasyGo](https://badges.gitter.im/magicdmer/EasyGo.svg)](https://gitter.im/magicdmer/EasyGo?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Watch video at https://www.bilibili.com/video/BV16P4y1Z7jQ/?](https://img.shields.io/badge/watch-on%20bilibili-brightgreen)](https://www.bilibili.com/video/BV16P4y1Z7jQ/?)

## 简介
这是一款快捷启动软件，基本功能是快速查找所要打开的软件，并对其进行打开等操作。增强功能为软件所支持的各种插件，比如书签搜索，有道翻译 ，天气查询 等。插件支持python，c++和易语言三种语言，下面是动态图演示：
![0f4ccd48ff9f30cb78cf52955454c57c_503ae0a70888d398](https://user-images.githubusercontent.com/5556368/183931138-45027153-f389-4069-9ec0-e997925c5a18.gif)




## 来历

一开始用的是开源的wox快捷启动，感觉很好用，于是就写了一些插件，修改了些bug。 但是用了一段时间发现问题多多，一些功能和操作也感觉满足不了我的要求，作者长时间不维护，而我对c#又不是很熟悉，所以就打算自己用c++写一个类似的软件，然后就动手了。主要参考wox的功能界面和使用习惯，插件架构也参考了wox的逻辑，然后对wox中我感觉不太好的体验做了修正，对一些感觉薄弱的功能进行了加强，希望大家使用愉快

Wox官网：http://www.wox.one/




## 优点

主要的特性如下：

1. 使用everything的原理进行检索，减少建立程序索引的时间
2. 插件支持 **c++** ， **python** 和 **易语言**，其中python插件可以很方便的从wox移植过来，因为大体使用了wox的插件架构方式
3. 插件支持 **回车模式** 和 **实时模式** ，默认是 **实时模式** 。实时模式就是和wox一样，实时的查询输入的关键字，回车模式则是需要按回车后进行查询操作。对于一些网络插件，采用实时模式，很容易出现访问频率过于频繁的问题，比如之前用到的wox的有道词典插件，所以就加了回车模式
4. 插件支持文件类型操作结构，根据用户拖入的文件类型来调用注册了此文件类型的插件，并显示操作列表
5. 安装python插件的时候，可以自行根据插件里面的配置文件来自动安装相关依赖库



## 工程结构

**depends**:  EasyGo一些插件以来的第三方软件，比如解码器啥的，支持音乐播放

**plugin**:  插件目录，格式为 `.plugin`  ，其实就是 zip 格式改了后缀，具体可以看压缩包自带的文档

**plugin-sources**:  这个里面是插件源码，主要是c++和易语言的，因为python本身就是源码，可以解压看



## 注意事项
你可以fork或者参考该工程结构，弄一个自己的插件仓库，供自己使用



## 帮助文档
1. 可以直接查看 github 上的 wiki 分类
2. 查看压缩包类的 mht 文档



## 交流
1. QQ群: 707119847
2. 小众软件论坛
3. Discussions
