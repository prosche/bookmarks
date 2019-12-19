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
        Blocked：等待阻塞 wait() (释放持有的锁，其他等待的线程得到该资源)，Notify()/NotifyAll() 唤醒
                         同步阻塞 Synchronized
                         其他阻塞 sleep() (不释放持有的锁，释放cpu， 其他等待的线程不能该资源)， join()唤醒
        
        yield()线程回到可执行状态，之后又会被执行
        
        setPriority() 设置优先级 MIN_PRIORITY=1, NORM_PRIORITY=5, MAX_PRIORITY=10
    
 ·线程同步 synchronized
 
 ·线程数据传递
 
 ·锁 Lock java.util.concurrent.locks
 
 ·线程池
        
        java.util.concurrent.Executors;
        java.util.concurrent.ExecutorService;
        
      1)newCachedThreadPool()
      缓存型池子，如果以前有线程，就reuse；如果没有，就建一个新的线程
      执行一些生存周期很短的异步任务
      能reuse的线程，必须是timeout IDLE内的池中线程，缺省timeout是60s，超出这个IDLE时长，线程实例将被终止及移出池
      cache池线程数支持 0-Integer.MAX_VALUE（考虑主机的资源承受能力），60s IDLE
      
      Executors.newCachedThreadPool();
      
      2)newFixedThreadPool(int)
      能reuse，不能新建
      任意时间点，最多只能有固定数目的活动线程存在，此时如果有新的线程要建立，只能放在另外的队列中等待，直到当前的线程中某个线程终止直接被移出池子
      没有IDLE机制
      cache池和fixed池调用的是同一个底层池。 fixed池线程数固定，无IDLE。
      
      Executors.newFixedThreadPool(5);
      
      3)newScheduledThreadPool(int)
      调度型线程池
      池子中线程可以按schedule依次delay执行，或周期执行
      
      Executors.newScheduledThreadPool(10)
      
      4)SingleThreadExecutor()
      单例线程
      和cache池和fixed池同一个底层池，但数目是1-1，无IDLE
      
      Executors.newSingleThreadExecutor();
      
    Executor执行Callable任务
      通过ExecutorService的submit(Callable task)方法来执行，并且返回一个Future
      
    自定义线程池
      ThreadPoolExecutor(int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, BlockingQueue<Runnable> workQueue)
      corePoolSize: 线程池中所保持的核心线程数，包括空闲线程
      maximumPoolSize：池中允许的最大线程数
      keepAliveTime：线程池中的空闲线程所能持续的最长时间
      unit：持续时间点单位
      workQueue：任务执行前保持任务的队列，仅保存有executor方法提交的Runnable任务
 
 ·线程安全: 
 
 reference
 
 http://www.codeceo.com/article/java-coding-performance.html
 http://blog.csdn.net/Evankaka/article/details/44153709
 https://juejin.im/post/5a73cbbff265da4e807783f5
 https://juejin.im/post/5cb4551ef265da03b858443d#heading-36
 https://tech.meituan.com/2018/11/15/java-lock.html
 https://aijishu.com/a/1060000000071010
 

#IO，NIO，AIO，Netty

#JVM

#GC

#反射

#泛型

#设计模式

#事务

#序列化 反序列化

#微服务

reference

https://zhihu.com/question/65502802
http://dockone.io/article/3687
https://www.cnblogs.com/stulzq/p/8573828.html

#springboot

·AOP， IOC

·注解

·Spring WebFlux 
      异步非阻塞的Web框架
      

     https://juejin.im/post/5cb5d71d51882545dd09b634
     https://zhuanlan.zhihu.com/p/35305648
     https://github.com/JeffLi1993/springboot-learning-example

·过滤器，拦截器，切片

     过滤器(filter)
     
     拦截器(HandlerInterceptor)
     
     切片(Aspect)
     
     https://juejin.im/post/5c6901206fb9a049af6dcdcf

·异常捕获处理

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
