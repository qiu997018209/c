Bss段存放没有初始化或者初始化为0的全局变量
他在程序运行周期内都是存在的，所以不要申明大的全局变量

objdump -h a.out | grep bss


Data段存放的是初始化为非0的全局变量

静态变量在第一次进入作用愈时被初始化，以后不必初始化，静态变量在类之间共享数据
也是放在全局静态区域中。并且只有一份拷贝。

静态变量和全局数据都在一个区域,注意静态变量和全局变量是在main函数结束后才释放


rodata:存放常量数据，字符串常量，编译器会去掉重复的，保证只有一个副本，并且不可修改

拷贝构造:1.通过一个对象创造宁一个对象(a=b),2.作为函数入参赋值的时候 3.理论上，函数返回一个对象时也会，但是会被编译器优化掉

编译器提供的默认拷贝构造函数的行为:
将每一个非static成员，依次复制到正在创建的对象。

浅拷贝:只拷贝指针，指针所对应的堆资源没有被复制





