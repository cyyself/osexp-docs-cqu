## 实验任务

### 异常中断

（1）结合LoongArch32的文档，列出LoongArch32有哪些例外？以及这些例外有哪两个例外向量入口？

（2）请编程完善`kern/driver/clock.c`中的时钟中断处理函数`clock_int_handler`，在对时钟中断进行处理的部分填写trap函数中处理时钟中断的部分，使操作系统每遇到100次时钟中断后，调用kprintf，向屏幕上打印一行文字”100 ticks”。

（3）请编程完善`kern/driver/console.c`中的串口中断处理函数`serial_int_handler`，在接收到一个字符后读取该字符，并调用kprintf输出该字符。

要求完成问题（2）、（3）提出的相关函数实现，提交改进后的源代码包（可以编译执行），并在实验报告中简要说明实现过程，并写出对问题（1）的回答。完成这问题（2）和（3）要求的部分代码后，运行整个系统，可以看到大约每1秒会输出一次”100 ticks”，而按下的键也会在屏幕上显示。