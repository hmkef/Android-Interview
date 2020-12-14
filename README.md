# Android-Interview
Android面试笔记




2020Android面经，历时一个半月，斩获3个大厂offer
================================


历时一个半月，斩获3个大厂offer（京东、新浪、滴滴），这里进行下简单的总结，希望能帮助到大家。

总体来说，面试一般都是基于你的`简历`来进行的，一般先考察你的基础，然后考察你知识体系的完备程度，接着会考察你的极限，最后还会考察一些软技能，比如你的学习能力、协作能力、沟通能力、分析解决未知问题的能力、抗压能力等。

个人心得
----

凡事预则立，不预则废。

#### 准备周期

面试之前，最好先系统的复习一下基础知识，然后再复盘下自己的项目经历，把亮点都发掘出来。复习周期个人建议是`三个月到半年`，时间不宜太久，久了就容易懈怠或者闭门造车，三个月的时候最好出去开始试水，检验一下自己的学习效果。

复习计划的制定和进度的把控也很重要，可以参考别人的学习计划去学习，再根据自己的实际情况去做适当的调整。

#### 复习技巧

我一直认为`学习没有捷径可言`。我信奉"好记性不如烂笔头"，也信奉"书读百遍其义自见"。

一定要去`实践`。对于程序员而言，不单单是死记硬背，我们有更好的方式去学习，比如写demo去验证，比如学习源码的过程中，一定要自己去翻看源码，多翻几遍看熟了再说。

`学习笔记`我认为很重要，不仅要记笔记，还要写心得体会，文字笔记、画图、总结等，方式很多，但是一定要自己认真去做，不要太相信自己的记忆，只有反复记忆，加深理解才行。

学习知识点的过程中，可以遵循`What、How、Why`这个三板斧。即这个东西是什么？它是怎么做的？它为什么这么做，原理是什么，有没有更好的方式？

在复习的过程中，都是从一个个小的知识点开始学的，复习到一定阶段，可以尝试着去把这些东西串联起来，由点及面。

另外在复习的过程中，一定要及时跟你做过的项目结合起来，这样也可以反哺你的项目，你在面试时就知道怎么聊了，就会有项目讲到知识点，由一个知识点串联到另一个知识点，这样你的知识体系就建立起来了。

#### 准备简历

简历是你的敲门砖，具体简历模板我就不提供了，网上有很多优秀的模板大家可以参考。我觉得最重要的是你要把你的简历上的东西吃透，要深挖，多问几个为什么，比如我为什么要选择这个方案，它有什么优势和劣势，有没有更好的方式。

面试官一般会基于你的简历来考察你的综合能力，所以写简历千万不能偷懒，要拿出去写论文的态度来，认真修改反复揣摩，多请几个大佬帮你修改，提建议。

#### 答题技巧

面试总体上是一个你跟面试官相会了解、相互交流的过程，大厂的面试官一般都很奈斯，如果你遇到不会的问题了，可以及时请教对方，不会了就问，不要怕丢面子，面试本就是一个学习和相互交流的过程，offer不是目的，只是个过程。

另外，有些时候某些技术或者知识点你不了解细节，但是大体的设计思路你是知道的，你就尽可能的答出你的理解，可以用横向的类似的技术去阐述这个技能点。

有些时候如果某个知识点一时半会想不起来了，可以迂回一下，跟递推公式一样，根据你擅长的知识点，一步一步去推导，先大胆假设，再小心求证，推导的过程也能说明一些问题。

还有需要注意的一点，对于不会的东西，可以尝试从原理角度去回答，但是尽量不要说错，回答的不全和方向错了是两个概念。

常考知识点
-----

### 1、Java

*   讲下equals和hashcode，他们为何必须一起重写？hashcode方法重写规则。
    
*   HashMap相关。
    

```
①HashMap添加元素的过程，hash方法细节；扩容的触发条件、扩容过程中是数据是整体复制么？链表转红黑树的阈值为何是8，红黑树转链表的阈值为何是6，为何不上同一个阈值？链表为何要转红黑树？红黑树有何特性？hashmap为何如此设计？

②对应的并发容器。HashTable以及ConcurrentHashMap实现细节，优劣势； 如何使现有的HashMap线程安全？（Collections#synchronizedMap）
```


*   运行时数据区域分区，哪些线程私有，哪些线程共享。栈帧的数据结构。方法区存放哪些数据。
    
*   简单描述一下 Person person = new Person() 对象实例化过程。最好有类加载过程。
    
*   GCRoot的类型，举例说明。
    


```
Activity中的匿名Handler导致的内存泄漏，最终的引用链root要分析到Thread#threadLocals上
```


*   LRU的实现。让你自己实现一个，你会怎么做。
    
*   线程的几种状态。
    
*   线程池。
    

```
    ①7个参数。
    ②线程池中的任务可以实现按照优先级执行么，如何实现？（优先级队列）
    ③线程池的设计用到了那种设计思想？（生产者消费者模型）
    ④何为阻塞队列？
    ⑤你是如何配置线程池的？核心线程数你一般是怎么配置的？
    
```


*   T1、T2、T3三个线程，如何保证它们顺序执行？也就是异步转同步的方式。

  
```
  ①Thread#join
  ②等待多线程完成的CountDownLatch
  ③FutureTask
  ④Executors#newSingleThreadExecutor
  ⑤wait/notify
```

*   Java中 wait和sleep方法的不同？（wait释放锁，sleep不会释放锁）
*   线程安全相关。
*   锁。synchronized、volatile、Lock。锁的几种状态。CAS原理。


```
    ①为什么会有线程安全？
    ②Java中如何保证线程安全？
    ③synchronized和Lock的使用、区别及底层实现；volatile的作用和使用方式；常见的原子类。
    ④synchronized中的类锁和对象锁互斥么？
    
```


*   讲下Java的双亲委派。
    
*   泛型。
    

```
    ①泛型擦除的原因和效果，擦除的时机。
    ②为何会有协变和逆变
    ③通配符。
    ④PECS
```
    

*   反射。
    
*   注解。

 
```
   ①Source和Class、Runtime注解的区别
    ②注解如何使用
    
```

*   方法内部的匿名内部类使用方法的局部变量时，为何要使用final修饰？

### 2、Android

*   启动模式，以及常见用法。

```
    ①举例说明
    ②taskAffinity，allowTaskReparting的用法。
    ③有没有遇到哪些诡异的现象？如何解决的？
    
```

*   Activity生命周期。


```
    ①常见生命周期方法
    ②A启动B的，然后按back键，执行了哪些方法？如果是A启动B的，然后按home键呢？
    ③onSaveInstance方法调用时机。   
```


*   Bitmap内存优化。


```
    ①Bitmap内存如何计算？如何在不改变图片质量的情况下优化？Bitmap内存复用（Options.inBitmap）
    ②超大图加载（BitmapRegionDecoder）
    ③跨进程传递大图（Bundle#putBinder）
    
```


*   xhdpi的图片分别显示到hdpi和xxhdpi的手机上，显示的大小和内存是怎样的？
    
*   资源文件加载规则。比如说图片存放在drawable-hdpi和drawable-xxhdpi下，xhdpi的手机会加载哪张？如果删除掉drawable-xxhdpi下的图片呢？
    
*   Android的进程间通信方式。
    

```
    ①Android为何要自己搞一个binder，使用linux原有的通信方式不行么？（安全、性能好，方便易用）
    ②binder通信的内存大小限制。（1M和128k）
    ③binder的架构（Application、ServiceManager、系统Service、binder驱动），以获取系统服务的过程举例分析。
    ④Application#onCreate里面可以使用binder服务么(可以)？Application的binder机制是何时启动的（zygote在fork好应用进程后，会给应用启动binder机制）？binder机制启动的几个关键步骤。
    ⑤binder线程池默认最大数量（15）？
    ⑥binder和AIDL。
    ⑦oneway。
```
   

*   谈谈你对Android中Context的理解？四大组件里面的Context都来源于哪里。
    
*   Application启动流程。
    

```
    ①AMS是如何确认Application启动完成的？关键条件是什么（zygote返给AMS的pid；应用的ActivityThread#main方法中会向AMS上报Application的binder对象）？
    ②Application#constructor、Application#onCreate、Application#attach他们的执行顺序（132）。Activity和Service呢？
```  

*   startActivity的具体过程。
    
*   Activity#setContentView的具体过程。
    

```
    ①PhoneWindow是何时创建的，它的作用是什么？
    ②setContentView中传递的资源文件是如何变成View对象的？
    ③布局文件对应的View对象是添加到哪里的？
    ④Activity的布局是何时显示出来的？
    ⑤ViewRootImpl是何时初始化的？它的作用是什么？
    ⑥Choreography了解么？作用是什么？
   
```

*   Surface的作用是什么？它是何时初始化的？View绘制的数据是如何显示到屏幕上的？
*   Handler机制：

```
    ①应用层，消息的发送、接收、获取和处理；消息是如何存储的？延时消息一定准时么？是如何保证延时时间的？Handler#dispatchMessage细节，如何使用？
    ②Handler的Framework层。Looper#loop方法为何不会导致ANR？nativePollOnce细节。eventfd和epoll机制了解么？
    ③IdleHandler了解么？合适调用？如何使用？靠谱么？
    ④handler里面消息有几种？普通消息、同步消息、消息屏障。如何使用？如何区分普通消息和异步消息？
    ⑤如何实现给Handler发送一个Runnable，又不通过Handler#post(Runnable run)这个API？（Message#obj属性，或者通过反射设置Message#callback属性）
    ⑥Message#obtain实现细节了解么？为何要池化？最大限制容量是多少？
    
```

*   ThreadLocalMap的实现。
*   View绘制流程


```
    ①onMeasure、onLayout、onDraw
    ②MeasureSpec为何如此设计？
    ③子View的LayoutParams来源。ViewGroup#addView(view)这种添加view的方式，没有给子View设置LayoutParams，那么LayoutParams是谁设置的？
    ④onMeasure和onLayout为何会执行两次或多次？
    ⑤View#draw方法细节。
    ⑥View绘制这一块遇到过什么问题么？如何解决的。  
```


*   自定义View有哪几种方式？注意事项。你对自定义属性如何理解？
    
*   事件分发。滑动冲突如何解决，具体在哪个方法里面解决？如何判断滑动方向？
    
*   动画
    
*   Apk打包流程。R文件最终会生成什么文件？aapt的作用是什么？
    
*   LocalBroadcastReceiver，为何比BroadCastReceiver速度快，LocalBroadcastReceiver的实现。
    
*   RecyclerView的缓存。RecyclerView的优势是哪些？都用它做过什么功能?
    
*   讲下leakCanary原理。为什么不用虚引用？引用队列里面存的是什么？内存数据是如何dump出来的？
    
*   讲下OkHttp的实现。拦截器的顺序，网络拦截器和普通拦截器有什么区别？它的线程池是怎样的？如何管理的？
    
*   glide的三级缓存如何做的？
    
*   rxjava的原理。rxjava的线程切换如何实现的？map和flatmap操作符区别；zip和merge操作符区别。
    
*   ArrayMap和SparseArray的作用和实现细节。
    
*   组件化和模块化的区别。
    
*   mvp、mvvm。
    
*   jetpack组件。
    
*   gradle中task的生命周期。
    
*   插件化原理。
    
*   热修复原理。
    

### 3、Android性能优化

*   启动速度优化。冷启动、温启动、热启动了解么。
    
*   内存优化
    
*   卡顿优化
    
*   网络优化
    
*   数据库优化
    
*   内存泄漏优化
    
*   包体积优化
    

### 4、http相关

*   描述一个完整的网络请求流程。
    
*   TCP和UDP区别，三次握手与四次挥手的细节；为何建立链接需要三次，断开链接却需要四次。
    
*   http和https区别。https的链接过程？
    
*   断线续传如何实现。大图分段上传如何实现。关键步骤
    
*   分段下载如何实现。
    
*   请求重试机制如何实现。
    

### 5、设计模式

*   你熟悉哪些设计模式？请举例说明。为何选用这个设计模式。
    
*   策略模式和桥接模式的区别
    

### 6、kotlin

*   说一下kotlin的优缺点。let和with的区别
    
*   扩展函数
    
*   kotlin的lateinit和by lazy的区别
    
*   构造函数有哪几种
    
*   协程
    

### 7、flutter

*   flutter的isolate
    
*   flutter的优势和劣势
    
*   flutter的channel通信方式有哪几种？
    
*   flutter的包体积优化
    
*   flutter中State的生命周期，didUpdateWidget方法何时调用
    

### 8、项目相关

*   选一个你最熟悉的项目讲解下。
    
*   讲一下你的技术栈
    
*   你最自豪的项目或者片段
    
*   你最擅长哪些部分
    
*   你的上份工作经历中，最大的收获是什么？
    
*   你的职业规划
    

面试真题
----

### 1、滴滴

#### 一面

1、View绘制流程。onMeasure、onLayout、onDraw。

2、竖向的TextView如何实现。TextView文字描边效果如何实现。

3、事件分发。冲突解决。

4、动画

5、RecyclerView的特点和缓存

6、SparseArray和ArrayMap。具体实现原理和特性

7、说一下kotlin的优缺点。let和with的区别

8、接口和抽象类的区别，接口中可以有属性么？

9、用过哪些设计模式？策略模式和桥接模式的区别

10、多线程如何实现？有哪些方式？

11、线程池的参数

12、你如何自己实现一个LRUCache？Android里面的LRUCache是如何实现的？

13、synchronized和volatile的区别？为何不用volatile替代synchronized？类锁和对象锁互斥么？

14、gcroot的类型

15、jvm的运行时数据结构。栈帧中会有什么异常？方法区里面存放的是什么数据？

16、动态代理的实现。

17、Gradle的实现，gradle中task的生命周期。

18、Aop、AspectJ、ASM了解么

19、组件化和模块化的区别。ARouter的缺点。

20、MVP、MVVM的优缺点，jetpack中的组件

21、okhttp源码。

22、glide缓存

23、你对flutter的理解

#### 二面

1、react的单向数据流

2、redux的状态管理，如何实现的？关键角色有哪些？

3、flutter的channel通信有哪几种？你用的哪种？插件你如何实现的？

4、flutter的包体积优化

5、自定义View的关键步骤，注意事项，你的理解

6、MeasureSpec讲一下

7、包体积优化

8、混淆的步骤和原理

9、module间的资源文件merge后，生成过多的R文件，处理过么？如何处理？

10、Bitmap内存大小，注意事项，如何优化

11、启动速度优化

12、glide中对Bitmap做了哪些操作？三级缓存？为何在有了内存缓存后，还要持有ActivityRef这个呢？

13、gradle声明周期，task，插件

14、注解：Source和Class、Runtime注解的区别

15、卡顿优化

16、内存泄漏检测及优化

17、RecyclerView的缓存，局部刷新用过么？

18、List的滑动卡顿如何优化

19、Activity中的Window的初始化和显示过程

20、Application中可以显示Dialog么？为什么？

21、泛型擦除，为何会有擦除？擦除的时机。通配符。

下面这段代码有问题么？有什么问题？为何会有这个问题？


```
    List<? extends Object> list = new ArrayList<>();
    list.add(123);
    Object obj = list.get(0);
    
```


22、synchronized的同步原语

23、锁的几种状态

24、Android热修复原理，tinker的patch文件如何生成，patch文件是全部加载dex文件首部么？

25、插件化原理

26、两个用单链表表示的大数相加，求他们的和。单链表元素的值为0~9。

#### 三面

1、选一个你的项目讲一下

2、技术选型是如何做的

3、优化内存

4、上传的重试机制

5、OOM和内存泄漏

6、包体积优化

7、你最擅长的点

8、你的职业规划

### 2、新浪

#### 一面

1、封装的Adapter讲解。

2、自定义View：支持换行的尾部标签的实现。

3、IdleHandler调用时机

4、Bitmap内存计算规则

5、glide默认Bitmap的Config配置是ARGB\_8888么？

6、下面这段代码有什么异常？如何解决？


```
    private final ArrayMap<String, Boolean> mBlackFirstFrame = new ArrayMap<>();
    
    public boolean getFlag(String key) {
    		return mBlackFirstFrame.get(key);
    }
```

    

7、下面这段代码会有什么问题？如何解决？

    
```
public static class Person implements Serializable {
    		private One one;
    		private Two two;
    }
    
    public static class One implements Serializable {
    
    }
    
    public static class Two {
    
    }
```

    

8、Java为何会有线程安全问题？如何解决？

#### 二面

1、vue的binding原理

2、flutter中isolate的原理。

3、promise的原理

4、讲一下你的技术栈

5、讲下OOM原理

6、讲下ANR

7、linux中进程间通信的方式，Android为何会自己搞一个？

8、Java中进程间共享的数据是放在JVM那个分区的？Java中主进程和子进程间的通信，通过哪块内存区域？

9、Facebook的litho了解过么？flexbox用过么？

10、热修复用的什么方案？

11、代码质量如何控制？

12、app质量如何控制？

13、你做过的最烂的一件事是什么？最好、最自豪的一件呢？

### 3、京东物流

#### 一面

1、模块化，组件化，开发中要点有哪些。组件间如何去除强依赖。

2、Android11有没有适配

3、flutter中State的生命周期，didUpdateWidget方法何时调用

4、包体积如何优化

#### 二面

1、上家公司期间你的技术亮点，期间遇到什么问题，如何解决的，原理深挖。

2、View的绘制流程。MeasureSpec，关键方法，

3、LRU如何实现的？LinkedHashMap如何实现的？LinkedHashMap是否线程安全？如何实现线程安全？有序还是无序？

4、ThreadLocal干嘛的？用法和原理。

5、HashMap讲一下，数据结构、hash过程、扩容、加载因子为何是0.75等。

6、Handler讲一下。Message#what的不同值，会影响Message在MessageQueue中的顺序么？

7、讲下Java的双亲委派

8、插件化和热更新原理

9、讲一下锁，synchronized和Lock。CAS原理

10、事件分发

#### 三面

1、对vue的掌握程度

2、现有项目情况

3、包体积优化细节

4、画现有项目的架构图

5、后端交互过程中有遇到什么难以解决的问题么？如何解决的。

6、讲下你觉得最好或者最自豪的项目

#### 四面

1、讲下hashmap；链表转红黑树的限制为何是8；红黑树的时间复杂度；红黑树转链表的限制为何是6；current hashmap在所有情况下都是线程安全的吗？hashtable呢？

2、synchronized实现。非静态方法A和B在同一个类中，方法A用synchronized修饰，当A方法因为多线程请求有线程阻塞在对象锁上的时候，B方法的访问受不受影响？

3、既然泛型有编译期类型擦除，那么运行时无法获取到具体类型；而反射能在运行时获取到Class的类型；它们一个获取不到，一个可以获取到，这不就是矛盾么？请解释下细节。

4、在同一个手机上，如果把drawable-xxhdpi下的图片移动到drawable-xhdpi下，图片内存是如何变的，解释原理。如果在drawable-hdpi、drawable-xxhdpi下放置了图片，但是手机是xhdpi的，会优先加载哪个，加载优先级是怎样的？如果是400\*800，1080\*1920这种呢，会如何查找？xhdpi和400\*800同时存在时，会如何查找？布局文件呢？

5、图片内存优化；

6、Handler机制。MessageQueue中的Message是如何排列的？Msg的runnable对象可以外部设置么，比如说不用Handler#post系列方法（反射可以实现）；

7、application中持有静态的用户信息，有何缺点？如何改进？

8、mvp和mvvm，jetpack

### 4、小米

#### 一面

1、组件化

2、mvp优缺点，mvvm

3、kotlin

4、单例的几种实现方式：DCL、enum，静态内部类。还有饿汉式。懒汉式的使用场景：占用内存大、延迟初始化

5、jvm：运行时数据分区；类加载过程；GCRoot，垃圾回收算法。

6、hashmap。hash冲突时给链表插入数据，1.7头插法，1.8尾插法。

7、ArrayMap和SparseArray的区别，实现。

8、泛型：为何会有协变和逆变，PECS规则。

9、kotlin泛型：out和in.

10、Handler。Looper.loop( )为何不会阻塞进程。

11、自定义View的几种方式。onMeasure、onLayout、onDraw方法都何时需要重写。自定义属性的作用。

12、事件分发，多点触碰处理，是在onTouchEvent方法里面。

13、网络优化，网络监控。

14、网络分层架构，https的连接过程，tcp和udp的区别。

15、blog相关。

16、滑动窗口的最大值。

#### 二面

1、滑动冲突如何解决？有几种方式？具体从哪个事件开始拦截？在哪里拦截？比如双层ViewPager嵌套的滑动冲突如何解决。

2、事件分发的具体流程。

3、Activity#setContentView中的xml文件是如何转化成View并显示到Activity中的。


```
①PhoneWindow是在哪里初始化的？

②LayoutInflater是如何把xml布局文件转换成View对象的（反射）？View树如何生成的？怎么优化？

③为什么会有R文件这个映射表？直接使用资源的路径不好么？

④Android项目中都包含哪些资源？apk打包流程。apk解压后都包含哪些资源？R文件打包后生成的文件是哪种？

⑤dex文件结构了解过么？为何会有65535的限制？mutildex技术了解么？这项技术的目的是什么？

⑥Window和Activity的对应关系。除了Activity还有别的方式显示Window出来么？

```

4、绘制相关：


```
①requestLayout调用后，都会调用哪些方法？

②onMeasure、onLayout、onDraw这三个方法中，哪个最耗时？onMeasure和onLayout呢？

③Choreography的作用。它的上游和下游各自是哪个。Choreography发布了订阅消息，同类型的Callback还有哪些？这些Callback之间的优先级如何？vsync机制。

④Surface对象了解么？作用，何时初始化，怎么使用的。

⑤一个Button的点击事件中，调用requestLayout，接下来哪些方法会被调用？

⑥Surface和Window的关系

⑦SurfaceView的实现

⑧View#draw()方法细节

⑨绘制的数据是如何提交到远端的SurfaceFlinger

⑩GPU和surfaceFlinger之间的设计思想是什么？surfaceFlinger具体作用是什么？它对数据做了哪些操作？

⑪硬件加速了解么？GPU如何高效绘制？

```

5、ContentProvider具体实现。

6、binderService方法中的回调具体运行在哪个线程？binder线程池最大线程数是多少？自定义的Callback远程调用，运行在哪个线程？为何不是主线程，如果运行在主线程会有哪些问题？

7、hdpi和xxhdpi的手机，分别加载xhdpi下的图片，会缩放图片么？如果会缩放，是如何缩放的，像素点是如何补全或者减少的？图片在内存中的大小会如何变化？

8、操作系统：


```
①讲一下用户态和内核态

②为何会有用户态和内核态划分

```

9、数据结构：


```
①二叉树用的多么？哪里用过？

②二叉搜索树、AVL树，红黑树

③二叉树的使用举例。

④链表和二叉树的区别，优劣势

```

10、jetpack组件库使用过么？讲下具体组件

11、函数式编程如何理解？

12、t1、t2、t3三个线程，如何让三个线程按照顺序依次打印1-100。手写。

#### 三面

1、悬浮窗如何实现

2、通知的类别

3、为何需要进程保活？如何做？

4、进程优先级

5、Android为何会使用binder来进行进程间通信。

6、oneway和非oneway了解么？举例说明

7、binder线程池的最大线程个数；binder线程池中如果满了，对待新来的任务，会如何处理？此时client端会是什么效果？

8、ANR的log中关键字是什么？

9、你认为优秀的工作流程是怎样的？

10、讲下你项目的技术栈。

11、你认为好的app质量标准，产品标准。

### 5、百度

#### 一面

1、js调用原生有几种方式？

2、大图加载优化，原理。

3、http消息体讲一下。消息首行的方法有哪几种？

4、http post请求上传大文件，如何实现？分块上传呢？用到的关键Header有哪些？

5、Activity的onSaveInstance方法何时调用？它跟onPause、onStop的调用顺序如何？

6、Activity A启动Activity B，调用顺序。最后Activity A的onStop一定会调用么？

7、RecyclerView的缓存。

8、kotlin的协程，构造函数。

9、进程间有哪几种通信方式、binder安全原理、讲下aidl内容。

10、binder是cs架构，Server端的binder都是运行在同一个线程里面么？

11、讲下GC root的类型。

12、讲下Handler。

13、讲下你做过的首页优化。

14、讲下leakCanary原理，为什么不用虚引用？引用队列里面存的是什么？

15、求单链表的倒数第n个结点，时间复杂度为O(1)的解法。bad case是哪种？

16、遍历目录及其子目录，使用非递归的方式。

#### 二面

1、讲下flutter的项目

2、kotlin的扩展，属性是否可以扩展，是否可以扩展跟现有方法签名相同的方法

3、讲一下Activity的TaskRecord，也就是四种启动模式。

4、方法内部的匿名内部类，比如说给View设置的OnClickListener，它里面相关调用外部方法的形参，必须使用final修饰这个形参，为何？

5、Android里面进程间通信方式，ContentProvider可以用file实现么？

6、linux下常见的进程间通信方式，Android为何自己搞一个Binder，有何优势？

7、本地广播为何效率高？

8、讲下synchronized和volatile；读写锁和ReentrantLock，synchronized和读写锁的区别。

9、布局优化

### 6、vipkid

#### 一面

1、项目中有哪些亮点？自定义View


```
①获取TextView的行数时，StaticLayout原理

②MotionEvent#offsetLocation事件转发。

```

2、讲下onMeasure方法：

①如何测量

②测量模式

③入参为什么是int类型？

④为什么会多次调用onMeasure和onLayout方法？

3、讲下事件传递：

①总体流程

②DOWN事件拦截后，后续事件如何处理？

③dispatchTouchEvent方法返回true后事件如何处理？

4、ActivityA启动了ActivityB后，两个Activity的生命周期是怎样的？

5、线程、进程的区别

6、多线程为何不安全

7、synchronized和volatile区别

8、Lock的实现，以及与synchronized的区别

9、GCRoot，举例说明。比如说Activity和它的匿名内部类Handler，分析下引用链，对应的gcroot是哪个？

10、图片内存的计算。

①在不影响图片质量的前提下，如何减少内存？

②图片显示不全、变形怎么处理？

11、http和https：

①它们的区别：https多了tls层。对称加密和非对称加密。

②具体验证的过程是怎样的？

12、你擅长的领域：

①Handler

②Activity启动流程：AMS、zygote、ApplicationThread之间交互；oneway特性（server端不阻塞和client端串行化），非oneway的情况有哪些？

③postDelay(1s)是如何保证1s时间执行的？

④Application启动流程

⑤ContentProvider启动流程

13、使用Application#onTrimMemory优化

14、使用ActivityLifecycleCallbacks做了哪些事情？

15、zxing优化

16、如何提高线上代码质量？

17、你的不足？

18、你的期望

#### 二面

1、直播弹幕如何实现？

2、离职原因，问的很细。

3、以前的app的技术深度，知识沉淀，如何成长等

4、之前的不足，如何避免；最自豪的项目或者片段。

5、职业规划

### 7、少年得到

#### 一面

1、讲一下项目

2、成员变量和局部变量的区别。为何成员变量需要jvm在对象初始话过程中赋默认值？

3、讲下equals和hashcode，他们为何必须一起重写？

4、字符串的 “+” 和 append操作的区别。避免创建多个String对象。

5、泛型和泛型擦除。kotlin真泛型的实现；泛型中T和？的区别，List<?>和List有什么区别；泛型里的super和extends区别；泛型为何会有擦除；擦除的时机；泛型的编译器类型检查。

6、HashMap：数据结构（数组加链表（或者红黑树）），为何这么设计；数组和链表的特性；元素添加的过程；扩容过程中为何不整体复制；链表为什么要转红黑树？

7、HashMap的替代方案，ArrayMap和SparseArray。

8、Parcelable和Serializable本质区别，不要说用法，说原理。

9、Activity和Fragment的生命周期；Fragment#onHiddenChanged是生命周期方法么？如何触发？

10、Activity和Fragment的通信方式；系统为何会设计Fragment#setArgument方法。

11、View绘制流程；requestLayout和invalidate区别；invalidate每次都会触发onDraw么？View#onLayout每次会触发么？

12、SharedPreference的apply和commit区别；apply会不会导致ANR；SharedPreference的替代方案

13、讲下你的自定义View，为何如此设计？

14、屏幕适配方案；头条适配方案核心原理。

15、启动速度优化。

16、绘制优化。

17、JsBridge原理，它是如何解决安全性问题的？

18、mvp和mvvm（面试官说要从订阅、观察者角度讲）

19、项目架构

20、kotlin的lateinit和by lazy的区别

21、flutter的三棵树；flutter为何性能比rn好

#### 二面

1、Android与js交互方式；JsBridge原理，它是如何解决安全性问题的？

2、View绘制优化

3、图片加载优化，不要讲公式，就讲你怎么做的。glide源码

4、Activity实现了一个Lifecycle接口，有了解么？

5、如何上传数据？请求头关键字段和请求体格式

6、音视频了解么？MediaPlayer能同时播放多个音频么？如果需要播放多个提示音，如何实现？

7、Rxjava的map和flatmap区别，flatmap为何要生成多个Observable？Rxjava的线程种类，线程切换如何实现的？

8、drawable下所以的格式都能转成webp么？哪些不能转？

### 8、水滴

#### 一面

1、从0到1搭建一个项目框架，你会怎么做？

2、flutter的生命周期管理？讲讲做过的flutter项目。flutter的路由管理方式。除了默认的两种路由方式，有没有考虑过记录路由状态？

3、讲下arraylist、hashmap、linkedlist、linkedhashmap的实现。linkedhashmap为何会有这样的特性(lru)?它有个参数，表示命中率和使用次数。

4、lru是通过linkedhashmap实现的么？

5、线程的使用。讲下线程池的类型，线程池对象的参数，线程池最大线程数和核心线程数的关系，task的优先级如何实现？（优先级队列）

6、activity启动模式：standard、singleTop、singleTask、singleInstance。taskAffinity，allowTaskReparting，常见应用场景。

7、startActivity方法是异步的么？同步的。

8、activity生命周期。A启动B，生命周期；B回到A，生命周期

9、rxjava源码。用过哪些操作符？map和flatmap区别。

10、讲下View绘制流程。canvas可以画Bitmap么？画布要做旋转、缩放、平移等操作该如何实现？

11、讲下事件分发。如果onInterceptTouchEvent返回true，但是onTouchEvent返回了false，是什么效果？如果还想让其他View接收事件，该怎么做？

12、flutter中，有没有遇到过路由断掉的情况，比如说原生打开flutter，flutter再打开原生这种？

#### 二面

没聊技术，就聊些职业发展之类的。

### 9、滴滴-IM部门

#### 一面

1、项目经历，

2、最有成就感的项目

3、性能优化：UI优化、内存泄漏

4、大图加载；xhdpi的图片放到xxhdp的手机上，内存会如何变化；Bitmap内存复用

5、网络优化，数据库优化

6、Handler

7、ThreadLocal，LocalBroadcastReceiver实现

8、binder的mmap

9、Java的线程同步方式；synchronized和Lock的实现及区别

10、线程池如何配置，核心线程数你一般给多少

11、Java内存模型

12、TCP和UDP区别，TCP为何是三次握手，为何是四次挥手

13、设计模式（问了一个什么模式，我没听清）

14、自定义View，测量模式的匹配

15、事件分发，如何处理滑动冲突

16、启动速度优化，IdleHandler用法

17、冷启动热启动优化

18、组件化架构设计，ARouter具体实现

19、Activity生命周期，按Home按键后的生命周期

20、启动模式及其用法。A应用的A1页面启动B应用的B1页面，A1和B2都是standard模式，B1启动后B1在那个任务栈，按下back键后显示那个页面，再按一次back键呢？

21、MVC、MVP、MVVM

22、IM你知道多少？

### 结束语

面试的最终目的是找到一个自己满意的offer，也是一个实现自我价值的过程。

欢迎各位同学随时交流。

最后，祝各位同学都有一个美好的前程。

