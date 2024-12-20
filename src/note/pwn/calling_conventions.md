# Pwn 调用约定

我们往往需要做一些约定，来确保团队开发中各类接口统一，使得不同的功能模块能够被正确地调用。

举个例子来说，小明开发了一个功能，并将其包装成了一个函数。而小李需要正确地使用这个功能。于是他们商量并确定了这个函数的名字，如何传参，函数返回什么。

我们能够看到有各种各样的"**约定**"：API接口规范，各种网络协议，总线协议……

在这里，我们讨论在汇编语言层面的一类重要的约定：**调用约定**

调用约定规定了一个函数应该如何传参，如何调用与被调用，如何返回，调用者和被调用者应该如何维护栈以及寄存器的数据。

> 调用者依据调用约定设置寄存器以及栈，确保传入参数正确，被调用者依据调用约定取出参数，设置返回数据。

一般来说，CTF中(x86/x64 linux)常用的是syscall, fastcall, cdecl调用约定，syscall用于使用x64系统调用，fastcall用于x64函数调用，cdecl是x86下默认的C语言调用约定。

> 需要注意的是，windows下的fastcall和linux下的fastcall不太一样。具体需要查手册。

更多的调用约定详见：google [调用约定]

linux调用约定：https://www.cnblogs.com/liert/p/17353566.html

windows调用约定：https://learn.microsoft.com/zh-cn/cpp/build/x64-calling-convention

在比赛中，我们需要控制程序设置好不同的参数，以正确调用不同的函数。在此之前，你还需要学习栈帧。

### 下一章节： [Pwn —— 栈帧](./stackframe.md)