- https://baike.baidu.com/item/servlet/477555?fr=aladdin
- Servlet（Server Applet）是[Java](https://baike.baidu.com/item/Java/85979)Servlet的简称，称为小服务程序或服务连接器，用Java编写的[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8/100571)端程序，具有独立于平台和[协议](https://baike.baidu.com/item/%E5%8D%8F%E8%AE%AE/13020269)的特性，主要功能在于交互式地浏览和生成数据，生成动态[Web](https://baike.baidu.com/item/Web/150564)内容。
- 狭义的Servlet是指Java语言实现的一个接口，广义的Servlet是指任何实现了这个Servlet接口的类，一般情况下，人们将Servlet理解为后者。Servlet运行于支持Java的应用服务器中。从原理上讲，Servlet可以响应任何类型的请求，但绝大多数情况下Servlet只用来扩展基于[HTTP协议](https://baike.baidu.com/item/HTTP%E5%8D%8F%E8%AE%AE/1276942)的Web服务器。
- 最早支持Servlet标准的是JavaSoft的Java[Web Server](https://baike.baidu.com/item/Web%20Server/9306055)，此后，一些其它的基于Java的Web服务器开始支持标准的Servlet。
- 中文名
  : 小服务程序或服务连接器
  外文名
  : Servlet
  别    名
  : Servlet Applet
  - 类    别
  : 程序
  环    境
  : Java[applet](https://baike.baidu.com/item/applet)
  平    台
  : Java Web Server
- Servlet 是在[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)上运行的小程序。这个词是在 Java[applet](https://baike.baidu.com/item/applet)的环境中创造的，Java applet 是一种当作单独文件跟网页一起发送的小程序，它通常用于在客户端运行，结果得到为用户进行运算或者根据用户互作用定位图形等服务。
  
  服务器上需要一些程序，常常是根据用户输入访问数据库的程序。这些通常是使用[公共网关接口](https://baike.baidu.com/item/%E5%85%AC%E5%85%B1%E7%BD%91%E5%85%B3%E6%8E%A5%E5%8F%A3)（**C**ommon**G**ateway**I**nterface，CGI）应用程序完成的。然而，在服务器上运行 Java，这种程序可使用 Java 编程语言实现。在通信量大的服务器上，JavaServlet 的优点在于它们的执行速度更快于 CGI 程序。各个用户请求被激活成单个程序中的一个线程，而**无需**创建单独的进程，这意味着[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)端处理请求的[系统开销](https://baike.baidu.com/item/%E7%B3%BB%E7%BB%9F%E5%BC%80%E9%94%80)将明显降低。
  
  **实现过程**
  
  最早支持 Servlet 技术的是 JavaSoft 的 Java Web Server。此后，一些其它的基于 Java 的 Web Server 开始支持标准的 Servlet API。Servlet 的主要功能在于交互式地浏览和修改数据，生成动态 Web 内容。这个过程为：
- 客户端发送请求至服务器端；
- 服务器将请求信息发送至 Servlet；
- Servlet 生成响应内容并将其传给[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)。响应内容动态生成，通常取决于客户端的请求；
- 服务器将响应返回给客户端。
  
  
  
  Servlet 看起来像是通常的 Java 程序。Servlet 导入特定的属于 Java Servlet API 的包。因为是对象[字节码](https://baike.baidu.com/item/%E5%AD%97%E8%8A%82%E7%A0%81)，可动态地从网络加载，可以说 Servlet 对 Server 就如同 Applet对 Client 一样，但是，由于 Servlet 运行于 Server 中，它们并不需要一个[图形用户界面](https://baike.baidu.com/item/%E5%9B%BE%E5%BD%A2%E7%94%A8%E6%88%B7%E7%95%8C%E9%9D%A2)。从这个角度讲，Servlet 也被称为 FacelessObject。
  
  一个 Servlet 就是 Java 编程语言中的一个类，它被用来扩展[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)的性能，服务器上驻留着可以通过“请求-响应”编程模型来访问的应用程序。虽然 Servlet 可以对任何类型的请求产生响应，但通常只用来扩展 Web 服务器的应用程序。
## 命名
[编辑](javascript:;)[播报](javascript:;)

Servlet 的命名可以看出 sun 命名的特点，如 Applet 表示[小应用程序](https://baike.baidu.com/item/%E5%B0%8F%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F/3350978)；Scriptlet = Script + Applet，表示小脚本程序；同样 Servlet = Service + Applet，表示小服务程序。
## 生命周期
[编辑](javascript:;)[播报](javascript:;)
- 客户端请求该 Servlet；
- 加载 Servlet 类到内存；
- 实例化并调用init()方法初始化该 Servlet；
- service()（根据请求方法不同调用doGet() 或者 doPost()，此外还有doHead()、doPut()、doTrace()、doDelete()、doOptions()、destroy())。
- 加载和实例化 Servlet。这项操作一般是动态执行的。然而，Server 通常会提供一个管理的选项，用于在 Server 启动时强制装载和初始化特定的 Servlet。
  
  
  
  Server 创建一个 Servlet的实例
  
  第一个客户端的请求到达 Server
  
  Server 调用 Servlet 的 init() 方法（可配置为 Server 创建 Servlet 实例时调用，在 web.xml 中 标签下配置 标签，配置的值为整型，值越小 Servlet 的启动优先级越高）
  
  一个客户端的请求到达 Server
  
  Server 创建一个请求对象，处理客户端请求
  
  Server 创建一个响应对象，响应客户端请求
  
  Server 激活 Servlet 的 service() 方法，传递请求和响应对象作为参数
  
  service() 方法获得关于请求对象的信息，处理请求，访问其他资源，获得需要的信息
  
  service() 方法使用响应对象的方法，将响应传回Server，最终到达客户端。service()方法可能激活其它方法以处理请求，如 doGet() 或 doPost() 或程序员自己开发的新的方法。
  
  对于更多的客户端请求，Server 创建新的请求和响应对象，仍然激活此 Servlet 的 service() 方法，将这两个对象作为[参数传递](https://baike.baidu.com/item/%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92)给它。如此重复以上的循环，但无需再次调用 init() 方法。一般 Servlet 只初始化一次(**只有一个对象**)，当 Server 不再需要 Servlet 时（一般当 Server 关闭时），Server 调用 Servlet 的 destroy() 方法。
  
  如图1所示显示了一个典型的 Servlet 生命周期方案:
  
  
  #+BEGIN_EXPORT hiccup
  [:a {:class "image-link", :nslog-type "9317", :href "https://baike.baidu.com/pic/servlet/477555/0/2cf5e0fe9925bc31930cf45c55df8db1ca1370a5?fr=lemma&ct=single", :target "_blank", :title "图1：典型的 Servlet 生命周期"} [:img {:class "", :src "https://bkimg.cdn.bcebos.com/pic/2cf5e0fe9925bc31930cf45c55df8db1ca1370a5?x-bce-process=image/resize,m_lfit,w_842,limit_1/format,f_auto", :alt "图1：典型的 Servlet 生命周期"}]]
  #+END_EXPORT图1：典型的 Servlet 生命周期
  
  
  1.第一个到达服务器的 HTTP 请求被委派到 Servlet 容器。
  
  2.Servlet 容器在调用 service() 方法之前加载 Servlet。
  
  3.然后 Servlet 容器处理由多个线程产生的多个请求，每个线程执行一个单一的 Servlet 实例的 service() 方法。
## 工作模式
[编辑](javascript:;)[播报](javascript:;)

客户端发送请求至[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)；

服务器启动并调用 Servlet，Servlet 根据客户端请求生成响应内容并将其传给服务器；

服务器将响应返回客户端。
## 对比
[编辑](javascript:;)[播报](javascript:;)

与 Applet 的比较

**相似之处：**

* 它们不是独立的应用程序，没有[main](https://baike.baidu.com/item/main)() 方法。

* 它们不是由用户或程序员调用，而是由另外一个应用程序(容器)调用。

* 它们都有一个生存周期，包含 init() 和 destroy() 方法。

**不同之处：**

*[Applet](https://baike.baidu.com/item/Applet)具有很好的图形界面([AWT](https://baike.baidu.com/item/AWT))，与浏览器一起，在客户端运行。

* Servlet 则没有图形界面，运行在[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)端。

与 CGI 比较

与传统的 CGI 和许多其他类似 CGI 的技术相比，Java Servlet 具有更高的效率，更容易使用，功能更强大，具有更好的可移植性，更节省投资。在未来的技术发展过程中，Servlet 有可能彻底取代 CGI。

在传统的 CGI中，每个请求都要启动一个新的进程，如果 CGI 程序本身的执行时间较短，启动进程所需要的开销很可能反而超过实际执行时间。而在 Servlet 中，每个请求由一个轻量级的 Java 线程处理（而不是重量级的操作系统进程）。

在传统 CGI 中，如果有 N 个并发的对同一 CGI程序的请求，则该CGI程序的代码在内存中重复装载了 N 次；而对于 Servlet，处理请求的是 N 个线程，只需要一份 Servlet 类代码。在性能优化方面，Servlet 也比 CGI 有着更多的选择。

*** 方便**

Servlet 提供了大量的实用工具例程，例如自动地解析和解码 HTML 表单数据、读取和设置[HTTP](https://baike.baidu.com/item/HTTP)头、处理[Cookie](https://baike.baidu.com/item/Cookie)、跟踪会话状态等。

*** 功能强大**

在Servlet中，许多使用传统 CGI 程序很难完成的任务都可以轻松地完成。例如，Servlet 能够直接和 Web[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)交互，而普通的 CGI 程序不能。Servlet 还能够在各个程序之间共享数据，使得数据库[连接池](https://baike.baidu.com/item/%E8%BF%9E%E6%8E%A5%E6%B1%A0)之类的功能很容易实现。

*** 可移植性好**

Servlet 用 Java 编写，Servlet[API](https://baike.baidu.com/item/API)具有完善的标准。因此，为 IPlanet Enterprise Server 写的 Servlet 无需任何实质上的改动即可移植到[Apache](https://baike.baidu.com/item/Apache)、[Microsoft](https://baike.baidu.com/item/Microsoft)IIS 或者 WebStar。几乎所有的主流[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)都直接或通过[插件](https://baike.baidu.com/item/%E6%8F%92%E4%BB%B6)支持 Servlet。

*** 节省投资**

不仅有许多廉价甚至免费的 Web 服务器可供个人或小规模网站使用，而且对于现有的服务器，如果它不支持 Servlet 的话，要加上这部分功能也往往是免费的（或只需要极少的投资）。

与 JSP 比较

JSP 和 Servlet 的区别到底在应用上有哪些体现，很多人搞不清楚。简单的说，SUN 首先发展出 Servlet，其功能比较强劲，体系设计也很先进，只是，它输出 HTML 语句还是采用了老的 CGI 方式，是一句一句输出，所以，编写和修改 HTML 非常不方便。

Java Server Pages(JSP)是一种实现普通静态HTML 和动态 HTML 混合编码的技术，JSP 并没有增加任何本质上不能用 Servlet 实现的功能。但是，在 JSP 中编写静态HTML 更加方便，不必再用 println语 句来输出每一行 HTML 代码。更重要的是，借助内容和外观的分离，页面制作中不同性质的任务可以方便地分开：比如，由页面设计者进行[HTML](https://baike.baidu.com/item/HTML)设计，同时留出供 Servlet 程序员插入动态内容的空间。

后来 SUN 推出了类似于 ASP 的镶嵌型的 JSP，把 JSP TAG 镶嵌到 HTML 语句中，这样，就大大简化和方便了网页的设计和修改。新型的网络语言如 ASP，PHP，JSP 都是镶嵌型的语言。 这是 JSP 和 Servlet 区别的运作原理层面。

从网络三层结构的角度看 JSP 和 Servlet 的区别，一个网络项目最少分三层：data layer(数据层)，business layer(业务层)，presentation layer(表现层)。当然也可以更复杂。Servlet 用来写 business layer 是很强大的，但是对于写 presentation layer 就很不方便。JSP 则主要是为了方便写 presentation layer 而设计的。当然也可以写 business layer。写惯了[ASP](https://baike.baidu.com/item/ASP)，[PHP](https://baike.baidu.com/item/PHP)，CGI的朋友，经常会不自觉的把 presentation layer 和 business layer 混在一起。

根据 SUN 自己的推荐，JSP中应该仅仅存放与 presentation layer 有关的东西，也就是说，只放输出 HTML 网页的部分。而所有的数据计算，数据分析，数据库联结处理，统统是属于 business layer，应该放在 Java BEANS 中。通过 JSP 调用 Java BEANS，实现两层的整合。

微软前不久推出的 DNA 技术，是 ASP+COM/DCOM 技术。与J SP+BEANS 完全类似，所有的 presentation layer 由 ASP 完成，所有的 business layer 由 COM/DCOM 完成。通过调用，实现整合。

采用这些组件技术单纯的因为 ASP/JSP 语言是非常低效率执行的，如果出现大量用户点击，纯 SCRIPT 语言很快就到达了他的功能上限，而组件技术就能大幅度提高功能上限，加快执行速度。

另外一方面，纯 SCRIPT 语言将 presentation layer 和 business layer 混在一起，造成修改不方便，并且代码不能重复利用。如果想修改一个地方，经常会牵涉到十几页 code，采用组件技术就只改组件就可以了。

综上所述，Servlet 是一个早期的不完善的产品，写 business layer 很好，写 presentation layer 就很臭，并且两层混杂。

所以，推出JSP+BEAN，用 JSP 写 presentation layer，用 BEAN 写 business layer。SUN 自己的意思也是将来用 JSP 替代 Servlet。这是技术更新方面 JSP 和 Servlet 的区别。

可是，这不是说，学了 Servlet 没用，实际上，你还是应该从 Servlet 入门，再上 JSP，再上 JSP+BEAN。

强调的是：学了JSP，不会用 Java BEAN 并进行整合，等于没学。大家多花点力气在 JSP+BEAN 上。

我们可以看到，当 ASP+COM 和 JSP+BEAN 都采用组件技术后，所有的组件都是先进行编译，并驻留内存，然后快速执行。所以，大家经常吹的 Servlet/JSP 先编译驻内存后执行的速度优势就没有了。

反之，ASP+COM+IIS+NT 紧密整合，应该会有较大的速度优势呈现。而且，ASP+COM+IIS+NT 开发效率非常高，虽然bug 很多。

那么，为什么还用 JSP+BEAN？因为 Java 实在前途远大。操作系统群雄并起，应用软件的开发商必定要找一个通用开发语言进行开发，Java 一统天下的时机就到了。

简单分析了一下 JSP 和 Servlet 的区别和 Java Web 开发方面的发展。随着机器速度越来越快，Java 的速度劣势很快就可以被克服。
## 版本介绍
[编辑](javascript:;)[播报](javascript:;)

| 

版本

 | 

日期

 | 

JAVA EE/JDK版本

 | 

特性

 |
| 

Servlet 4.0

 | 

2017年10月

 | 

JavaEE 8

 | 

HTTP2[1]

 |
| 

Servlet 3.1

 | 

2013年5月

 | 

JavaEE 7

 | 

Non-blocking I/O, HTTP protocol upgrade mechanism

 |
| 

Servlet 3.0

 | 

2009年12月

 | 

JavaEE 6, JavaSE 6

 | 

Pluggability, Ease of development, Async Servlet, Security, File Uploading

 |
| 

Servlet 2.5

 | 

2005年10月

 | 

JavaEE 5, JavaSE 5

 | 

Requires JavaSE 5, supports annotation

 |
| 

Servlet 2.4

 | 

2003年11月

 | 

J2EE 1.4, J2SE 1.3

 | 

web.xml uses XML Schema

 |
| 

Servlet 2.3

 | 

2001年8月

 | 

J2EE 1.3, J2SE 1.2

 | 

Addition of Filter

 |
| 

Servlet 2.2

 | 

1999年8月

 | 

J2EE 1.2, J2SE 1.2

 | 

Becomes part of J2EE, introduced independent web applications in .war files

 |
| 

Servlet 2.1

 | 

1998年11月

 | 

未指定

 | 

First official specification, added RequestDispatcher, ServletContext

 |
| 

Servlet 2.0

 |  | 

JDK 1.1

 | 

Part of Java Servlet Development Kit 2.0

 |
| 

Servlet 1.0

 | 

1997年6月

 |  |  |
## 新增功能
[编辑](javascript:;)[播报](javascript:;)

Servlet 2.2：

引入了 self-contained Web applications 的概念。

servlet 2.3：

:2000年10月份出来

Servlet API 2.3中最重大的改变是增加了 filters

Servlet 2.3 增加了 filters 和 filter chains 的功能。引入了 context 和 session listeners 的概念，当 context 或 session 被初始化或者被将要被释放的时候，和当向 context 或 session 中绑定属性或解除绑定的时候，可以对类进行监测。

servlet 2.4：

2003年11月份推出

Servlet 2.4 加入了几个引起关注的特性，没有特别突出的新内容，而是花费了更多的功夫在推敲和阐明以前存在的一些特性上，对一些不严谨的地方进行了校验。

Servlet 2.4 增加了新的最低需求，新的监测 request 的方法，新的处理 response 的方法，新的国际化支持，RequestDispatcher 的几个处理，新的 request listener 类，session 的描述，和一个新的基于 Schema 的并拥有 J2EE 元素的发布描述符。这份文档规范全面而严格的进行了修订，除去了一些可能会影响到跨平台发布的模糊不清的因素。总而言之，这份规范增加了四个新类，七个新方法，一个新常量，不再推荐使用一个类。

注意：改为 Schema 后主要加强了两项功能：

(1) 元素不依照顺序设定；

(2) 更强大的验证机制。

主要体现：

a.检查元素的值是否为合法的值

b.检查元素的值是否为合法的文字字符或者数字字符

c.检查 Servlet, Filter, EJB-ref 等等元素的名称是否单一的

2.新增 Filter 四种设定：REQUEST、FORWARD、INCLUDE 和 ERROR。

3.新增 Request Listener、Event和Request Attribute Listener、Event。

4.取消 SingleThreadModel 接口。当 Servlet 实现 SingleThreadModel 接口时，它能确保同时间内，只能有一个 thread 执行此 Servlet。

5.可以为Servlet。

6.ServletRequest接口新增一些方法。

public String getLocalName()；

public String getLocalAddr()；

public int getLocalPort()；

public int getRemotePort()

Servlet 2.5：

2005 年 9 月发布 Servlet 2.5

Servlet 2.5 一些变化的介绍：

1） 基于最新的 J2SE 5.0 开发的。

2） 支持 annotations 。

3） web.xml 中的几处配置更加方便。

4） 去除了少数的限制。

5） 优化了一些实例

Servlet 的各个版本对监听器的变化有：

(1) Servlet 2.2 和 jsp1.1

新增Listener:HttpSessionBindingListener

新增Event: HttpSessionBindingEvent

(2) Servlet 2.3 和 jsp1.2

新增Listener:ServletContextListener,ServletContextAttributeListener

,HttpSessionListener,HttpSessionActivationListener,HttpSessionAttributeListener

新增Event: ServletContextEvent,ServletContextAttributeEvent,HttpSessionEvent

(3) Servlet 2.4 和 jsp2.0

新增Listener:ServletRequestListener,ServletRequestAttribureListener

新增Event: ServletRequestEvent,ServletRequestAttributeEvent

Servlet 3.0

Servlet 3.0 作为 Java EE 6 规范体系中一员[2]，随着 Java EE 6 规范一起发布。该版本在前一版本（Servlet 2.5）的基础上提供了若干新特性用于简化 Web 应用的开发和部署。其中有几项特性的引入让开发者感到非常兴奋，同时也获得了 Java 社区的一片赞誉之声：[3]
- 异步处理支持：有了该特性，Servlet 线程不再需要一直阻塞，直到业务处理完毕才能再输出响应，最后才结束该 Servlet 线程。在接收到请求之后，Servlet 线程可以将耗时的操作委派给另一个线程来完成，自己在不生成响应的情况下返回至容器。针对业务处理较耗时的情况，这将大大减少服务器资源的占用，并且提高并发处理速度。[3]
- 新增的注解支持：该版本新增了若干注解，用于简化 Servlet、过滤器（Filter）和监听器（Listener）的声明，这使得 web.xml 部署描述文件从该版本开始不再是必选的了。[3]
- 可插性支持：熟悉 Struts2 的开发者一定会对其通过插件的方式与包括 Spring 在内的各种常用框架的整合特性记忆犹新。将相应的插件封装成 JAR 包并放在类路径下，Struts2 运行时便能自动加载这些插件。Servlet 3.0 提供了类似的特性，开发者可以通过插件的方式很方便的扩充已有 Web 应用的功能，而不需要修改原有的应用。[3]
  
  
  
  Servlet 4.0
  
  从3.1到4.0将是对Servlet 协议的一次大改动，而改动的关键之处在于对HTTP/2的支持。HTTP2将是是继上世纪末HTTP1.1协议规范化以来首个[HTTP协议](https://baike.baidu.com/item/HTTP%E5%8D%8F%E8%AE%AE/1276942)新版本，相对于HTTP1.1，HTTP2将带来许多的增强。在草案提议中，Shing Wai列举出了一些HTTP2的新特性，而这些特性也正是他希望在Servlet 4.0 API中实现并暴露给用户的新功能，这些新特性如下：[4]
  
  1.请求/响应复用(Request/Response multiplexing)
  
  2.流的优先级(Stream Prioritization)
  
  3.服务器推送(Server Push)
  
  4.HTTP1.1升级(Upgrade from HTTP 1.1)[4]
## 规范
[编辑](javascript:;)[播报](javascript:;)

1.简化开发

2.便于部署

3.支持 Web2.0 原则

为了简化开发流程，Servlet 3.0 引入了注解（annotation），这使得 web 部署描述符 web.xml 不再是必须的选择。

**Pluggability可插入性**

当使用任何第三方的框架，如 Struts，JSF 或 Spring，我们都需要在 web.xml 中添加对应的 Servlet 的入口。这使得 web 描述符笨重而难以维护。Servlet3.0 的新的可插入特性使得 web 应用程序模块化而易于维护。通过 web fragment 实现的可插入性减轻了开发人员的负担，不需要再在 web.xml 中配置很多的 Servlet 入口。

**Asynchronous Processing 异步处理**

另外一个显著的改变就是 Servlet 3.0 支持异步处理，这对 AJAX 应用程序非常有用。当一个 Servlet 创建一个线程来处理某些请求的时候，如查询数据库或消息连接，这个线程要等待直到获得所需要的资源才能够执行其他的操作。异步处理通过运行线程执行其他的操作来避免了这种阻塞。

Apart from the features mentioned here, several other enhancements have been made to the existing API. The sections towards the end of the article will explore these features one by one in detail.

除了这些新特性之外， Servlet 3.0对已有的 API 也做了一些改进，在本文的最后我们会做介绍。

**Annotations in Servlet Servlet中使用注解**

Servlet 3.0 的一个主要的改变就是支持注解。使用注解来定义 Servlet 和 filter 使得我们不用在 web.xml 中定义相应的入口。

**@WebServlet**

@WebServlet 用来定义 web 应用程序中的一个 Servlet。这个注解可以应用于继承了 HttpServlet。这个注解有多个属性，例如 name，urlPattern, initParams，我们可以使用者的属性来定义 Servlet 的行为。urlPattern 属性是必须指定的。
## 编程接口
[编辑](javascript:;)[播报](javascript:;)

[HTTPServlet](https://baike.baidu.com/item/HTTPServlet)使用一个 HTML 表单来发送和接收数据。要创建一个 HTTPServlet，请扩展[HttpServlet](https://baike.baidu.com/item/HttpServlet)类， 该类是用专门的方法来处理 HTML[表单](https://baike.baidu.com/item/%E8%A1%A8%E5%8D%95)的 GenericServlet 的一个子类。 HTML 表单是由 和 标记定义的。表单中典型地包含输入字段（如文本输入字段、[复选框](https://baike.baidu.com/item/%E5%A4%8D%E9%80%89%E6%A1%86)、[单选按钮](https://baike.baidu.com/item/%E5%8D%95%E9%80%89%E6%8C%89%E9%92%AE)和选择列表）和用于提交数据的按钮。当提交信息时，它们还指定[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)应执行哪一个Servlet（或其它的程序）。 HttpServlet 类包含 init()、destroy()、service() 等方法。其中 init() 和 destroy() 方法是[继承](https://baike.baidu.com/item/%E7%BB%A7%E6%89%BF)的。

**(1) init() 方法**

在 Servlet 的生命期中，仅执行一次 init() 方法。它是在服务器装入 Servlet 时执行的。 可以[配置服务器](https://baike.baidu.com/item/%E9%85%8D%E7%BD%AE%E6%9C%8D%E5%8A%A1%E5%99%A8)，以在启动服务器或客户机首次访问 Servlet 时装入 Servlet。 无论有多少客户机访问 Servlet，都不会重复执行 init() 。

缺省的 init() 方法通常是符合要求的，但也可以用定制 init() 方法来覆盖它，典型的是管理[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)端资源。 例如，可能编写一个定制 init() 来只用于一次装入 GIF 图像，改进 Servlet 返回 GIF 图像和含有多个客户机请求的性能。另一个示例是初始化数据库连接。缺省的 init() 方法设置了 Servlet 的初始化参数，并用它的 ServletConfig 对象参数来启动配置， 因此所有覆盖 init() 方法的 Servlet 应调用 super.init() 以确保仍然执行这些任务。在调用 service() 方法之前，应确保已完成了 init() 方法。

**(2) service() 方法**

service() 方法是 Servlet 的核心。每当一个客户请求一个HttpServlet 对象，该对象的service() 方法就要被调用，而且传递给这个方法一个"请求"(ServletRequest)对象和一个"响应"(ServletResponse)对象作为参数。 在 HttpServlet 中已存在 service() 方法。缺省的服务功能是调用与 HTTP 请求的方法相应的 do 功能。例如， 如果 HTTP 请求方法为 GET，则缺省情况下就调用 doGet() 。Servlet 应该为 Servlet 支持的 HTTP 方法覆盖 do 功能。因为 HttpServlet.service() 方法会检查请求方法是否调用了适当的处理方法，不必要覆盖 service() 方法。只需覆盖相应的 do 方法就可以了。

Servlet 的响应可以是下列几种类型：

一个输出流，浏览器根据它的内容类型（如 text/html）进行解释。

一个 HTTP 错误响应，重定向到另一个 URL、servlet、JSP。

**(3) doGet() 方法**

当一个客户通过 HTML[表单](https://baike.baidu.com/item/%E8%A1%A8%E5%8D%95)发出一个 HTTP GET 请求或直接请求一个 URL 时，doGet() 方法被调用。与 GET 请求相关的参数添加到 URL 的后面，并与这个请求一起发送。当不会修改[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)端的数据时，应该使用 doGet() 方法。

**(4) doPost() 方法**

当一个客户通过 HTML 表单发出一个 HTTP POST 请求时，doPost() 方法被调用。与 POST 请求相关的参数作为一个单独的 HTTP 请求从浏览器发送到服务器。当需要修改服务器端的数据时，应该使用 doPost() 方法。

**(5) destroy() 方法**

destroy() 方法仅执行一次，即在服务器停止且卸装 Servlet 时执行该方法。典型的，将 Servlet 作为服务器进程的一部分来关闭。缺省的 destroy() 方法通常是符合要求的，但也可以覆盖它，典型的是管理服务器端资源。例如，如果 Servlet 在运行时会累计统计数据，则可以编写一个 destroy() 方法，该方法用于在未装入 Servlet 时将统计数字保存在文件中。另一个示例是关闭数据库连接。

当[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)卸装 Servlet 时，将在所有 service() 方法调用完成后，或在指定的时间间隔过后调用 destroy() 方法。一个 Servlet 在运行 service() 方法时可能会产生其它的线程，因此请确认在调用 destroy() 方法时，这些线程已终止或完成。

**(6) getServletConfig() 方法**

getServletConfig() 方法返回一个 ServletConfig 对象，该对象用来返回初始化参数和 ServletContext。ServletContext 接口提供有关 servlet 的环境信息。

**(7) getServletInfo() 方法**

getServletInfo() 方法是一个可选的方法，它提供有关 servlet 的信息，如作者、版本、版权。

当[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)调用 sevlet 的 service()、doGet() 和 doPost() 这三个方法时，均需要 “请求”和“响应”对象作为参数。“请求”对象提供有关请求的信息，而“响应”对象提供了一个将响应信息返回给浏览器的一个通信途径。

javax.servlet 软件包中的相关类为 ServletResponse 和 ServletRequest，而 javax.servlet.[http](https://baike.baidu.com/item/http)软件包中的相关类为 HttpServletRequest 和 HttpServletResponse。Servlet 通过这些对象与[服务器](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8)通信并最终与客户端通信。Servlet 能通过调用"请求"对象的方法获知客户端环境，服务器环境的信息和所有由客户机提供的信息。Servlet 可以调用“响应”对象的方法发送响应，该响应是准备发回客户端的。
## 常见容器
[编辑](javascript:;)[播报](javascript:;)

Tomcat, Jetty, resin, Oracle Application server, WebLogic Server, Glassfish, Websphere, JBoss 等等。（提供了 Servlet 功能的服务器，叫做 Servlet 容器。对 web 程序来说，Servlet 容器的作用就相当于桌面程序里操作系统的作用，都是提供一些编程基础设施）
## 建议
[编辑](javascript:;)[播报](javascript:;)

在 Web 应用程序中，一个 Servlet 在一个时刻可能被多个用户同时访问。这时 Web 容器将为每个用户创建一个线程来执行 Servlet。如果 Servlet 不涉及共享资源的问题，不必关心多线程问题。但如果 Servlet 需要共享资源，需要保证 Servlet 是[线程安全](https://baike.baidu.com/item/%E7%BA%BF%E7%A8%8B%E5%AE%89%E5%85%A8)的。

下面是编写线程安全的 Servlet 的一些建议：

（1）用方法的局部变量保存请求中的专有数据。对方法中定义的局部变量，进入方法的每个线程都有自己的一份方法变量拷贝。任何线程都不会修改其他线程的局部变量。如果要在不同的请求之间共享数据，应该使用会话来共享这类数据。

（2）只用 Servlet的成员变量来存放那些不会改变的数据。有些数据在 Servlet 生命周期中不发生任何变化，通常是在初始时确定的，这些数据可以使用成员变量保存，如数据库连接名称、其他资源的路径等。

（3）对可能被请求修改的成员变量同步。有时数据成员变量或者环境属性可能被请求修改。当访问这些数据时应该对它们同步，以避免多个线程同时修改这些数据。

（4）如果 Servlet 访问外部资源，那么需要同步访问这些资源。例如，假设 Servlet 要从文件中读写数据。当一个线程读写一个文件时，其他线程也可能正在读写这个文件。文件访问本身不是线程安全的，所以必须编写同步访问这些资源的代码。在编写线程安全的 Servlet 时，下面两种方法是不应该使用的：

（1）在 Servlet API 中提供了一个 SingleThreadModel 接口，实现这个接口的 Servlet 在被多个客户请求时一个时刻只有一个线程运行。这个接口已被标记不推荐使用。

（2）对 doGet() 或doPost() 方法同步。如果必须在 Servlet 中使用同步代码，应尽量在最小的代码块范围上进行同步。同步代码越小，Servlet 执行得才越好。[5]