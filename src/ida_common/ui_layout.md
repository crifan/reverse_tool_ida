# 界面布局

此处整理，IDA中关于界面显示和布局方面的内容。

## 导航条=navigator

关于这个：

`Navigation band`=`navigator`=`navbar`=`导航栏`=`导航条`

有专门的介绍

[Igor’s tip of the week #49: Navigation band – Hex Rays (hex-rays.com)](https://hex-rays.com/blog/igors-tip-of-the-week-49-navigation-band/)

![ida_ui_navigator](../assets/img/ida_ui_navigator.png)

有空可以好好学习看看

## 切换显示模式

### `Text View`和`Graph View`

`IDA View-A`：在`Text View`和`Graph View`模式之间切换

![ida_view_graph_view](../assets/img/ida_view_graph_view.jpg)

这个叫做：`Graph View`=图形视图

好处：方便看函数调用的逻辑关系

如果想要切换到：`文本模式`，`汇编模式`

则可以：`右键`-》`Text View`

![ida_context_text_view](../assets/img/ida_context_text_view.jpg)

![ida_asm_text_view](../assets/img/ida_asm_text_view.jpg)

同理，从Text View想要切换到Graph View，也可以：

`右键`-》`Graph View`

![ida_from_text_to_graph](../assets/img/ida_from_text_to_graph.jpg)

回到了：graph视图

![ida_return_graph_view](../assets/img/ida_return_graph_view.jpg)

### 函数调用图 和 `Text View`

从函数调用图 切换到原先汇编指令形式：

![ida_func_call_to_text](../assets/img/ida_func_call_to_text.jpg)

切换到：`IDA View`

![ida_view_normal](../assets/img/ida_view_normal.jpg)

## 如何把浮动窗口`Output Window`固定到底部

问题：IDA中的`Output Window`，不知何故，悬浮在主体窗口上面了：

![output_window_float](../assets/img/output_window_float.jpg)

希望是：能固定到底部或左下角等位置

解决办法：

`IDA`->`Window`->`Reset desktop`

![window_reset_desktop](../assets/img/window_reset_desktop.jpg)

可以恢复IDA桌面原始布局

-》从而使得此处的`Output Window`，恢复最初的位置=固定在最底部的位置

![output_window_bottom](../assets/img/output_window_bottom.jpg)
