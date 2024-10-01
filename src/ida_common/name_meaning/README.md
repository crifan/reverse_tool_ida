# 命名和含义

TODO：

* 
* 【已解决】iOS逆向心得：如何从对x8的adrp和ldr计算出对应的qword字符串值

---

此处整理IDA中，各处看到的，各种名称的命令规则的含义。

## 背景知识

* `动态链接库`文件类型=后缀
  *  `Windows`：`.dll`
  *  `Linux`：`.so`
  *  `Mac`：`.dylib`

## 大的类型

* `F`=`Function`=**函数**
  * regular function, which is not a library function.
* `L`=`Library`=**库**
  * library function that can be recognized with different signatures that are part of IDA. If the matching signature is not found, the name is labeled as a regular function.
* `I`=`Imported`=**导入**（符号=函数）
  * imported name from the shared library. The code from this function/name is not present in the executable and is provided at run time, whereas the library function is embedded into the executable.
* `C`=`Code`=**代码**
  * named code that represent program locations that are not part of any function, which can happen if the name is a part of the symbol table, but the executable never calls this function.
* `D`=`Data`=**数据**
  * named data locations that are usually global variables.
* `A`=`Ascii`=（ASCII）**字符串**
  *  ASCII string data that represents a string terminated with a null byte in the executable.

## 命名规则

IDA中，对于未命令的内容，会采用默认从缩写命名。其命名规则是：

* IDA常见命名
  * `sub`=`subroutine`=`子程序`：函数
  * `locret`：返回指令
  * `loc`：location=（代码的）位置
  * `off`=`offset`：某个偏移量，存放某个数据
  * `seg`=`segment`：数据，包含段地址值
  * `asc`=`ascii`：数据，ASCII字符串
  * `byte`：数据，字节（或字节数组）
  * `word`：数据，16位数据（或字数组）
  * `dword`：数据，32位数据（或双字数组）
  * `qword`：数据，64位数据（或4字数组）
  * `flt`：浮点数据，32位（或浮点数组）
  * `dbl`：浮点数，64位（或双精度数组）
  * `tbyte`：浮点数，80位（或扩展精度浮点数）
  * `stru`=`structure`：结构体(或结构体数组)
  * `algn`=`align`：对齐指示
  * `unk`=`unknown`：未处理字节
  * 字节相关
    * `db`=1个字节
      * b=byte
    * `dw`=2个字节
      * w=word
    * `dd`=4个字节
      * d=double

