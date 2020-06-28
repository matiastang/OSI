# socket

[socket技术详解](https://www.jianshu.com/p/066d99da7cbd)
[(重要)socket原理详解](https://blog.csdn.net/pashanhu6402/article/details/96428887)
[IBM-Swift/BlueSocket 一个为Swift而生的Socket框架](https://blog.csdn.net/zhang5690800/article/details/79286678)
[BlueSocket-gitHub](https://github.com/IBM-Swift/BlueSocket)
[SwiftSocket-gitHub](https://github.com/swiftsocket/SwiftSocket)

什么是Socket？
上面我们已经知道网络中的进程是通过socket来通信的，那什么是socket呢？socket起源于Unix，而Unix/Linux基本哲学之一就是“一切皆文件”，都可以用“打开open –> 读写write/read –> 关闭close”模式来操作。我的理解就是Socket就是该模式的一个实现，socket即是一种特殊的文件，一些socket函数就是对其进行的操作（读/写IO、打开、关闭），这些函数我们在后面进行介绍。

socket一词的起源
在组网领域的首次使用是在1970年2月12日发布的文献IETF RFC33中发现的，撰写者为Stephen Carr、Steve Crocker和Vint Cerf。根据美国计算机历史博物馆的记载，Croker写道：“命名空间的元素都可称为套接字接口。一个套接字接口构成一个连接的一端，而一个连接可完全由一对套接字接口规定。”计算机历史博物馆补充道：“这比BSD的套接字接口定义早了大约12年。”

socket的基本操作
既然socket是“open—write/read—close”模式的一种实现，那么socket就提供了这些操作对应的函数接口。下面以TCP为例，介绍几个基本的socket接口函数。

[@_silgen_name](https://stackoverflow.com/questions/35030998/what-is-silgen-name-in-swift-language)
[深度探究HandyJSON(二) Mirror 的原理](https://www.jianshu.com/p/da0ccff0b531)