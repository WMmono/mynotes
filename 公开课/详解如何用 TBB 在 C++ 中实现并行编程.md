









标准库版本的线程对应的是操作系统意义上的线程。
但tbb的任务不一定对应一个线程


tbb会预先分配，比如一个四核电脑，就会预先分配4个线程
如果你分配8个任务，那么就会将8个任务通过分时的方式在4个线程上轮流去运行
TBB中任务和线程的关系就像操作系统严重线程和物理核心的关系。
TBB负责调度


parallel_invoke
能够接受任意个lambda函数然后同时执行它们
并且在函数返回之前自动的等待它们执行完毕。

在四核电脑中，它会先执行前面4个，然后再执行后面四个.
它作为一个结构体被线程读取然后执行。比系统提供的更加轻量级一些。



更好的例子是在字符串中查找字符d
可以拆成两半，然后利用tbb来并行查找

时间复杂度决定了快慢，工作复杂度决定了耗电量。

并行映射


parallel_for免得一个个去run
指定一个输入的区间
将这个区间变成lambda表达式的参数喂之。


parallel_for_each

tbb::parallel_for_each(a.begin(),a.end(),[&](float &f){
	f=32.f;
});


...折叠表达式


reduce（缩并）



parallel_reduce
存在一个问题，就是


保证每次运行结果一致：parallel_deterministic_reduce


C++模板使用inl文件的原因

inl文件是内联函数的源文件。





















































