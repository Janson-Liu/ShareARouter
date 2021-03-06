## ShareARouter
# 阿里路由框架ARouter使用与简单封装

借用阿里云栖社区的一段话：我们所使用的原生路由方案一般是通过显式intent和隐式intent两种方式实现的（这里主要是指跳转Activity or Fragment）。在显式intent的情况下，因为会存在直接的类依赖的问题，导致耦合非常严重；而在隐式intent情况下，则会出现规则集中式管理，导致协作变得非常困难。一般而言配置规则都是在Manifest中的，这就导致了扩展性较差。除此之外，使用原生的路由方案会出现跳转过程无法控制的问题，因为一旦使用了StartActivity()就无法插手其中任何环节了，只能交给系统管理，这就导致了在跳转失败的情况下无法降级，而是会直接抛出运营级的异常。这时候如果考虑使用自定义的路由组件就可以解决以上问题，比如通过URL索引就可以解决类依赖的问题；通过分布式管理页面配置可以解决隐式intent中集中式管理Path的问题；自己实现整个路由过程也可以拥有良好的扩展性，还可以通过AOP的方式解决跳转过程无法控制的问题，与此同时也能够提供非常灵活的降级方式。<br>

[探索Android路由框架-ARouter之基本使用](https://www.jianshu.com/p/6021f3f61fa6)  
[探索Android路由框架-ARouter之深挖源码](https://www.jianshu.com/p/5b35309e9bb2) 
