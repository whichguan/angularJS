# AngularJS

## Controller 使用过程正的注意点

- 不要试图去复用Controller，一个控制器一般只负责一小块视图
  不用继承，通用使用service。

  ![](https://ws4.sinaimg.cn/large/006tNc79gy1fowl2z23spj30gl084aag.jpg)

- 不用再Controller中操作DOM，这不是控制器的职责
  操作dom会触发重绘，封装成Angular的指令

- 不用在Controller里面做数据格式化，ng有很好用的表单控件

- 不要在Controller里面做数据过滤操作，ng有$filter服务

- 一般来说，Controller是不会互相调用的，控制器之间的交互会通过事件进行。



## 如何复用Model

scope是有作用域在对应的Controller里面，rootScope是定义根作用，所有的Controller可用。