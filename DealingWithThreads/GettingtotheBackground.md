###来到后台

因此，你需要把耗时的工作移到后台线程中去，但是这些线程需要做一些事情才能安排使用主应用线程做
更新UI的操作。

Android中有许多帮助做这件事的工具。

一些是为解决主功能区问题的高层次框架。其中一个例子就是从数据库获取信息的Loader框架，并且我们会
在[稍后一章](/TheLoaderFramework/README.md)中来分析这个框架。

有时候，存在内置进其它Android操作的异步选项。例如，我们[稍后一章](/UsingPreferences/README.md)
会讨论的`SharedPreferences`，我们会看到我们能够以异步或同步的方式进行持久化。

也有一把为解决这个问题的底层解决方案，你可以在其上面实现你自定义的业务逻辑。
