---
title: create-react-app
date: 2019-10-24 10:49:05
tags:
  - React
  - 脚手架
  - 前端
---

这个的是React官网推荐的一个脚手架，文档地址：https://create-react-app.dev/。
足够简单，你根本都不用了解webpack、babel是个啥，非常适合初学者，但也有一个很大的弊端，就是可配置性。

这个脚手架本身的使用方式非常简单，看官网文档就行了，下面主要说说如何进行个性化配置：

首先，你需要用到eject命令将封装在react-scripts里的配置文件、相关依赖弹射出来，它会将内置的配置全部以文件的形式重新存放于你的项目中，你可能比较在意的就是webpack的配置和Babel的配置。配置的时候只需要改变config/webpack.config.js相应的属性即可，这样基本上和裸了一个webpack没啥区别，不过是帮你把一些需要的loader，plugin配置好，其中有些配置在你的项目中甚至根本用不到。

至此，可配置性问题也算是勉强解决了，可eject出来的配置真的是有点复杂，至少看起来非常复杂，它是根据不同的环境，启动不同的脚本(scripts)，然后设置不同的执行环境变量，动态设置不同的webpack配置，不像固定的webpack文件那样简洁明了。

总结一下就是，官网推荐简单易上手，可配置性基本为0，但也有勉强能用的解决方案(eject)。

反正我个人是非常不喜欢create-react-app的，社区也提供了其他类似脚手架：如rodhog。

这里有篇文章还不错：https://github.com/sorrycc/blog/issues/15
不过rodhog这个项目好像好久没更新了。

近期也有尝试过umi，umi的设计思想像是模仿next.js，整体用下来感觉还是很不错的，足够简单，就是有一套自己的开发模式(框架固有模式)，可能稍微需要你去适应一下。

yeoman社区 (https://yeoman.io) 也有提供一些个人开发者提供的不错的脚手架，有空可以去探索一下，说不定突然就灵感大发，写一个御用的脚手架。

官网还提到两个工具neutrinojs和nwb，看着牛逼哄哄的，还没仔细看。