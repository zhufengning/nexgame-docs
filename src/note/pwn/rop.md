# Pwn ROP技术

ROP技术是pwn的入门技术，也是很多入门题的出题方向。因此你能够看到海量的资料。想要学习到这个技术，你甚至不需要google搜索。

大部分的资料会告诉你如何做题，但是涉及具体的原理，你需要结合之前的章节来理解。

推荐资料：

https://hello-ctf.com/HC_PWN/Stack_Overflow

https://pwn.college/software-exploitation/return-oriented-programming

关于这部分，你可以使用各种搜索引擎搜索[pwn ROP]，并尝试理解以下要点：
1. 什么是gadget
2. gadget会在哪里出现
3. 如何使用gadget
4. 什么是ROP链
5. 结合调用约定思考他们是如何调用system('/bin/sh')的