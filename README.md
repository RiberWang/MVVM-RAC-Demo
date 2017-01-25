# MVVM-RAC-DEMO
使用MVVM+RAC结合的方式，搞定一个添加上拉加载及下拉刷新的列表，更多的诠释MVVM思想，而不是RAC的逻辑链式操作（这一点用登录界面来写更能体现Y^o^Y ），RAC在此扮演的更大一部分的角色是更好的解耦，减少代码复杂度，使代码层次分明、逻辑清晰更便于维护升级!

本Demo的讲解可查看这里[《iOS MVVM+RAC 从框架到实战》](http://www.jianshu.com/p/3beb21d5def2)

欢迎评论提意见！谢谢！๑乛◡乛๑ 磨人的小妖精！

## MVC模式：
MVC即Model-VIew-Controller。MVC模式致力于关注点的切分，这意味着model和controller的逻辑是不与用户界面（View）挂钩的。因此，维护和测试程序变得更加简单容易。
MVC设计模式将应用程序分离为3个主要的方面：Model，View和Controller
01.Model
Model代表了描述业务路逻辑，业务模型、数据操作、数据模型的一系列类的集合。这层也定义了数据修改和操作的业务规则。
02.View
View代表了UI组件，像CSS，jQuery，html等。他只负责展示从controller接收到的数据。也就是把model转化成UI。
03.Controller
Controll负责处理流入的请求。它通过View来接受用户的输入，之后利用Model来处理用户的数据，最后把结果返回给View。Controll就是View和Model之间的一个协调者。

## MVP模式：
这个模式把Presenter换成Controller就非常和MVC相像了。这个设计模式把应用程序分成了3个主要方面：Model、View和Presenter。
01.Model
Model层代表了描述业务逻辑和数据的一系列类的集合。它也定义了数据修改和操作的业务规则。
02.View
View代表了UI组件，像CSS，JQuery，html等。他只负责展示从Presenter接收到的数据。也就是把模型（译者注：非Modle层模型）转化成UI。
03.Presenter
Presenter负责处理View背后所有的UI事件。它通过View接收用户输入，之后利用Model来处理用户的数据，最后把结果返回给View。与View和Controller不同，View和Presenter之间是完全解耦的，他们通过接口来交互。另外，presenter不像controller处理进入的请求。

## MVVM模式：
MVVM即Model-View-View Model。这个模式提供对View和View Model的双向数据绑定。这使得View Model的状态改变可以自动传递给View。典型的情况是，View Model通过使用obsever模式（观察者模式）来将View Model的变化通知给model。
01.Model
Model层代表了描述业务逻辑和数据的一系列类的集合。它也定义了数据修改和操作的业务规则。
02.View
View代表了UI组件，像CSS，JQuery，html等。他只负责展示从Presenter接收到的数据。也就是把模型转化成UI。
03.View Model
View Model负责暴漏方法，命令，其他属性来操作VIew的状态，组装model作为View动作的结果，并且触发view自己的事件。
