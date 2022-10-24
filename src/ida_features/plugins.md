# 插件

IDA还支持插件的机制，可以扩展支持更多更强的各种功能。

常见的插件有：

* keypatch

有机会参考

[iOS重打包绕过签名校验防护 | La0s](https://la0s.github.io/2019/03/21/iOS_Resign/)

> 使用Keypatch插件patch两条汇编`MOV X0, #0` && `RET`

![Ida_plugin_keypatch_insert](../assets/img/Ida_plugin_keypatch_insert.jpg)

去试试：

* 用keypatch插件，patch打补丁，插入（汇编）指令

## 其他插件

[Third-party plugins](https://hex-rays.com/products/decompiler/manual/third_party.shtml)

->

[onethawt/idaplugins-list: A list of IDA Plugins](https://github.com/onethawt/idaplugins-list)
