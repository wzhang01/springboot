#### Java异常分类和结构图
>由下面类图可以看出,Throwable作为基类,派生Error类和Exception类。\
>注意：异常能被程序本身可以处理，错误是无法处理。\
>根据编译器是否检查,又可以分为\
>不可查异常（unchecked exceptions）：运行时异常（RuntimeException与其子类）和错误（Error）。\
>可查异常（checked exceptions）：除了RuntimeException及其子类以外，其他的Exception类及其子类都属于可查异常。。



![](./ex_diagram.jpg '')

#### 中心思想
>1、框架捕获checked exception，转化为unchecked exception。\
>2、定义业务异常（RuntimeException子类），业务代码只抛异常，不捕获异常。\
>3、框架统一处理异常。并将异常转化为用户能理解的信息传达给用户。
