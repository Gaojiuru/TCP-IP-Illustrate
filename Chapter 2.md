#chapter 2 Internet地址结构

2.2 表示IP地址
Ipv4地址表示例子：

![image](http://github.com/Gaojiuru/TCP-IP-Illustrate/raw/master/images/IPv4地址.png)

IPv6地址长度为128位，传统表示方法是采用称为块或字段的四个十六进制数，用冒号分隔
IPv6简化表示[RFC4291]：
1.一个块中前导的零不必书写
2.全零的块可以省略，并用符号：：代替（一个IPv6地址中符号：：只能使用一次）
3.在IPv6格式中嵌入IPv4地址可使用混合符号形式，紧接着IPv4部分的地址块的值为ffff，地址的其余部分使用点分四组格式
4.IPv6地址的低32位通常采用点分四组表示法

![image](http://github.com/Gaojiuru/TCP-IP-Illustrate/raw/master/images/IPv6地址.png)

[RFC5952]简化规则：
1.前导的零必须压缩
2.：：只能用于影响最大的地方（压缩最多的零），但并不只是针对16位的块。如果多个块中包含等长度的零，顺序靠前的块将被替换为：：
3.a到f的十六进制数字应该用小写表示

2.3 基本的IP地址结构

IPv4地址空间有4294967296个可能的地址，IPv6的地址个数为340282366920938463374607431768211456

最初定义Internet地址结构时，每个单播IP地址都有一个网络部分，用于识别接口使用的IP地址在哪个网络中可悲=被发现；以及一个主机地址，用于识别由网络部分给出的网络中的特定主机。地址中的一些连续位称为网络号，其余称为主机号。

![image](http://github.com/Gaojiuru/TCP-IP-Illustrate/raw/master/images/IPv4地址分类.png)

![image](http://github.com/Gaojiuru/TCP-IP-Illustrate/raw/master/images/空间划分.png)

上表显示了分类地址结构的主要使用方式，如何将不同的单播地址块分配给用户。类划分基于给定大小的可用网络数和给定网格中的可分配主机数之间的折中。

子网寻址：头盖骨子网寻址，一个站点被分配一个A类、B类或C类的网络号，保留一些剩余主机号进一步用于站点分配。该站点可能将基础地址中的主机部分进一步划分为一个子网号和一个主机号。


