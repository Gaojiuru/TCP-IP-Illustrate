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

IPv4地址空间有4294967296个可能低地址，IPv6的地址个数为340282366920938463374607431768211456
