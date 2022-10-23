# IDA快手上手

* iOS逆向
  * 常用：（Mac中）用IDA分析代码
    * 下载和安装IDA
    * 找到要分析的iOS的app的二进制文件
    * 拖动二进制到IDA中
    * 等待分析完毕
    * 利用各种功能，研究代码逻辑
      * 常用功能
        * 字符串
          * 搜索感兴趣的关键字
            * 比如：越狱对应的单词：`jailbreak`、`jail`、`jb`等
        * 函数
          * 搜索已找到的iOS的ObjC的类和函数
            * 用于打开查看代码逻辑
        * 伪代码
          * 当打开函数后，默认是汇编代码，按`F5`即可打开`伪代码`
            * 近似于自己写的源码，人类可读的那种，就可以分析代码，搞懂函数的基本（甚至全部的）逻辑了
  * 偶尔用：用IDA调试二进制

## 下载

IDA官网有试用版可供下载：

[Download center (hex-rays.com)](https://hex-rays.com/download-center/)

->

* [IDA Free](https://hex-rays.com/ida-free/#download)
* [IDA Evaluation](https://out7.hex-rays.com/demo/request)
