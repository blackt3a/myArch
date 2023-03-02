环境

arch[安装](https://arch.icekylin.online/guide/rookie/pre-install.html)

关于archlinux[没声音](https://forum.manjaro.org/t/no-output-or-input-devices-found-manjaro/87606)



###### pwndbg

因为现在pip不推荐使用sudo安装，所以需要加--user,不然会崩

安装pwndbg会顺带把pwntools装好，不用再麻烦了

```shell
git clone https://github.com/pwndbg/pwndbg
cd pwndbg
./setup.sh --user
```



###### debtap

方法一

```shell
git clone https://github.com/helixarch/debtap
cd debtap
sudo cp debtap /usr/local/bin
```

方法二

```
yay -S debtap
```

使用前需执行`sudo debtap -u`更新

可能遇到的问题：因为其脚本中对deb包的解析是来自ubuntu官方源，可能更新不成功。

而常用的终端代理设置(export)并不能将问题解决，因为其不能控制所有代理，不能被`all_proxy`的名字骗了

解决方法一

将`/user/bin/debtap`脚本中地址换源

```shell
ftp.debian.org
archive.ubuntu.com
换成国内源，如清华源
```

解决方法二

使用

```shell
proxychains yay -S debtap #(需额外安装)
```



###### qemu

```shell
sudo pacman -S qume
```



###### LibcSearcher

```shell
pip install LibcSearcher
```



###### one_gadget

```shell
sudo pacman -S ruby
sudo gem install one_gadget
#网络问题改代理
#sudo proxychains gem install one_gadget
```



###### ropper

```shell
pip install ropper
```



###### ROP_gadget

```
git clone https://github.com/JonathanSalwan/ROPgadget.git
cd ROPgadget
sudo python3 setup.py install
```

###### seccomp-tools

```shell
sudo proxychains gem install seccomp-tools
```



###### patchelf

```shell
sudo pacman -S patchelf
```



###### 搭建arm交叉编译环境

待定。。。

https://knomori.com/index.php/2021/04/27/archlinux%E4%B8%8B%E6%90%AD%E5%BB%BAarm%E4%BA%A4%E5%8F%89%E7%BC%96%E8%AF%91%E7%8E%AF%E5%A2%83/

https://blog.csdn.net/weixin_39912984/article/details/116854780

https://aijishu.com/a/1060000000023713

https://zhuanlan.zhihu.com/p/113084121





今天的风甚是喧嚣啊！