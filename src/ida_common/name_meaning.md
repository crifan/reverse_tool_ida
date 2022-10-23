# 命名和含义

TODO：

* 【整理】IDA使用心得：常见名称及含义
* 【未解决】搞懂IDA中_D_objc_selrefs qword_38AF870 % 8的含义

---

此处整理IDA中，各处看到的，各种名称的命令规则的含义。

## 命名规则

IDA经常会自动生成假名字。他们用于表示子函数，程序地址和数据。根据不同的类型和值假名字有不同前缀

* IDA常见命名意义
  * sub 指令和子函数起点
  * locret 返回指令
  * loc 指令
  * off 数据，包含偏移量
  * seg 数据，包含段地址值
  * asc 数据，ASCII字符串
  * byte 数据，字节（或字节数组）
  * word 数据，16位数据（或字数组）
  * dword 数据，32位数据（或双字数组）
  * qword 数据，64位数据（或4字数组）
  * flt 浮点数据，32位（或浮点数组）
  * dbl 浮点数，64位（或双精度数组）
  * tbyte 浮点数，80位（或扩展精度浮点数）
  * stru 结构体(或结构体数组)
  * algn 对齐指示
  * unk 未处理字节
  * 字节相关
    * db=1个字节
    * dw=2个字节
    * dd=4个字节

## 举例

* sub
  * sub_11326A84
    * ![ida_sub_example](../assets/img/ida_sub_example.jpg)
* unk
  * unk_5922000
    * ![ida_example_unk](../assets/img/ida_example_unk.jpg)
* qword
  * qword_3A97BE0
    * ![ida_example_qword](../assets/img/ida_example_qword.jpg)

## 具体含义

### qword

对于qword：

* 常常是：常量字符串
* 偶尔是：其他类型
  * 比如字典的指针等等

详见：

* 【已解决】IDA中抖音AwemeCore中字符串const char* qword_3893908的原始字符串
* 【已解决】iOS逆向心得：如何从对x8的adrp和ldr计算出对应的qword字符串值
  * 核心逻辑是：
    * qword_xxx的xxx是二进制内偏移量 + 二进制的ALSR = 实际（字符串的）地址
    * 去查看： [实际（字符串的）地址] = （即可查看到）保存了对应的字符串
* 【整理】iOS逆向心得：IDA中的unk的含义