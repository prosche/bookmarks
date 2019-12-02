#JAVA多线程

 ·实现方式: Thread类，Runable接口， Callable接口
 
      Thread类: 调用start()开启线程
      
      Runable接口: 重写Run()方法
      
      Runnable接口比继承Thread类所具有的优势:
      
      1） 适合多个相同的程序代码的线程去处理同一个资源
      2） 可以避免JAVA中的单继承的限制
      3） 增加程序的健壮性，代码可以被多个线程共享，代码和数据独立
      4） 线程池只能放入实现Runnable或Callable类线程，不能直接放入继
      
 ·线程状态: New, Runnable, Blocked, Waiting, Time_Waiting，Terminated, Dead?
 
 ·线程安全: 
 
 reference
 
 http://www.codeceo.com/article/java-coding-performance.html
 

#IO，NIO，AIO，Netty

#JVM

#GC

#反射

#泛型

#设计模式

#事务

#序列化 反序列化

#springboot

#springcloud

#activeMQ, rabbitMQ, Kafka

#mangodb, cassandra, radis, Hbase, mysql

#数据结构及算法

#http2.0协议及安全

#tcp协议

#saas, paas, soa

#微服务，分布式架构

#jenkins

#docker

#dubbo

#nginx

#nodejs

# bookmarks
# JAVA
https://yq.aliyun.com/articles/727799?spm=a2c4e.11155472.0.0.2d837103tqG9jT

# translate  
https://translate.google.com/  
https://www.collinsdictionary.com/translator  

# web  
# # RxJS  
https://xgrommx.github.io/rx-book/content/guidelines/contract/index.html  
https://webcache.googleusercontent.com/search?q=cache:KTCx13GptxAJ:https://yuyang041060120.github.io/2016/05/16/observable-vs-promise/+&cd=2&hl=zh-CN&ct=clnk&gl=cn  
https://github.com/Reactive-Extensions/RxJS#the-need-to-go-reactive  
https://mcxiaoke.gitbooks.io/rxdocs/content/Observables.html   
http://reactivex.io/rxjs/manual/overview.html#pull-versus-push  
# # ReactiveX
https://webcache.googleusercontent.com/search?q=cache:cEHlSeGHr-QJ:https://mcxiaoke.gitbooks.io/rxdocs/content/Intro.html+&cd=2&hl=zh-CN&ct=clnk&gl=cn  
