###六要素

在新闻界，所有新闻故事都由六个基本要素构成，五个W一个H。这里，我们会应用这六个要素来帮助构架我们所讨论的关于碎片内容。

####为何

碎片不是activity，尽管它们可以被activity使用。

碎片不是容器(就是ViewGroup的子类)，尽管通常它们会创建一个ViewGroup。

相反的，你应该把碎片当做可重用的UI单元。你可以以定义activity的方式定义一个碎片，碎片中
有着布局和生命周期方法等。但是，如果需要的话，你能把碎片挂到一个或多个activity上。

Android没有明确实现像MVC,MVP,MVVM等UI架构。就把Android推到MVC架构而言，碎片和activity结合成了
控制层。碎片承担了局部控制者的职责，聚焦于它们的控件集，从模型数据填充进控件，并处理它们的事件。Activity
更像是承担了一个业务流程层的角色，处理跨碎片的通讯(例如，一个碎片A中的点击导致了碎片B所展示内容的改变)。


####何地

因为碎片是Java类，你的碎片会存在在你应用的Java包中。最简单的方式是把它放到你用来放activity的地方，尽管
如果需要的话，你可以修改你的UI逻辑到其他包上。

####谁

通常来说，你可以自己创建fragment实现，然后告诉Android什么时候去使用它们。一些第三方Android类库项目可能装载了
你可以重用的碎片实现，如果你这么选的话。

####何时

一些开发者在应用开发最初的时候添加了碎片-这是这个教程中我们会采用的方法。并且，如果你想从零开始弄一个新的应用，先定义碎片可能是一个好主意。话虽如此，完全有可能使用碎片来翻新一个已经存在的Android应用，尽管它可能需要很大的工作量。并且，不使用碎片创建也是完全有可能的。

碎片是在Android 3.0的时候被引进的（API等级11，又名蜂巢）。


####为何

这是一个大问题。如果我们没有碎片就可以了，并且我们没有必需要使用碎片来创建Android应用，要点是什么？为什么我们
要这么麻烦呢？

使用碎片的主要根本原因是，碎片使支持多个屏幕尺寸变得更容易了。

Android开始的时候是支持手机设备的。手机的大小可能是多变的，小到比三寸还小的小可爱(例如，Sony Ericsson X10 mini),大到五寸多的怪物（例如，Samsung Galaxy Note）。但是这些屏幕尺寸的变动跟手机和平板，或手机和电视之间的区别就显得苍白无力了。

一些应用仅仅会进行扩展从而填满较大的屏幕。许多游戏会采取这个方法，仅仅提供给用户较大的交互元素，较大的游戏布告栏等。

每个有玩过愤怒的小鸟这个游戏系列的人都知道，当在平板上玩的时候，给予了你较大的鸟和较大的猪，而不是被广告栏包围的手机大小的游戏区域。

但是，另一种设计方案是把平板屏幕当成一个并排排列的手机屏幕的数据集。

用户可以一次性就可以在平板上使用所有的功能，而不用在手机的多个独立的屏幕之间跳来跳去。


对于适配这个设计模式的应用来说，碎片允许你从一份代码同时支持手机和平板。碎片可以被手机上多个独立的activity使用，或者它们可以在平板上的单个activity上一起使用。

更多关于使用碎片来支持大屏的话题会在本书稍后一章中。这章是关注于设置和使用碎片的基本技术的。


####过程如何

回答这个问题就要看这章的剩余部分内容和这本书中其他地方的关于碎片的高级使用了。










