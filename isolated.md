# BN、ReLU与Conv融合

[神经网络量化入门--Folding BN ReLU - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/176982058)

* 如果使用 ReLU 之后的 scale 和 zp，那我们就可以用量化本身的截断功能来实现 ReLU 的作用。

注：ReLU 前后应该使用同一个 scale 和 zeropoint。这是因为 ReLU 本身没有做任何的数学运算，只是一个截断函数，如果使用不同的 scale 和 zeropoint，会导致无法量化回 float 域。

注：ReLU 本身就是在做 clip。所以，我们才能用量化的截断功能来模拟 ReLU 的功能。



# GUI

图形用户界面（Graphical User Interface，简称 GUI，又称图形用户接口）是指采用图形方式显示的计算机操作用户界面。