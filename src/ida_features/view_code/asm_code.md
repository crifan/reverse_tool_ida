# 汇编代码

TODO：

* 【已解决】IDA使用心得：IDA汇编代码如何快速找到匹配的Xcode汇编代码
* 【已解决】IDA中查看ARM汇编的伪代码
* 【未解决】IDA中开启宏指令比如ADRP和ADD变成ADRL
* 【整理】IDA使用心得：auto comments
* 【整理】IDA使用心得：OpCode区

---

IDA中的`汇编代码`，是从原始二进制的字节码，反汇编得到的汇编代码

![ida_asm_code_example](../../assets/img/ida_asm_code_example.jpg)

一般来说，在逆向尝试搞懂代码逻辑时，不太需要直接查看汇编代码，因为的确很难直接看懂逻辑。

不过有些情况下，会用到汇编代码：

* iOS逆向
  * 静态分析
    * 有些汇编代码中，IDA已帮忙分析和插入了相关的解释信息，值得研究逻辑时去参考
      * 比如，YouTube逆向期间，IDA已帮忙给相关汇编加上了描述，指明了有些代码是vtable的部分
        * 便于分析和对照，寻找对应虚函数的具体实现
  * 动态调试
    * 想要找到调试期间的，Xcode中汇编代码，对应的代码逻辑
      * 往往就需要找到IDA中对应的伪代码是什么
        * 往往就需要先去找到IDA中汇编代码的位置
          * 再去F5（或Tab键）跳转到对应的伪代码的位置
