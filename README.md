# Atmosphere
制作大气层整合包总结

第一弹：制作大气层整合包的个人总结

首先谢谢论坛各位大佬们的教程，我在此总结下大气层整合包的制作，论坛有很多大佬都在分享大气层整合包，我也尝试用过很多，这么多整合包用下来可以说学会了怎么动手整合，总结如下

1.大气层整合包都源于三样玩意儿，分别是Atmosphere，Hekate，Sigpatch，感谢paulzheng大佬解释的三件套。这当中，所有整合包的Atmosphere和Sigpatch都一样的，区别就是Hekate的启动设置，ak478bb大佬的教程手把手教你选择大气层启动设置选项，只要会Hekate_ipl.ini编辑。大佬还提供Sigpatch制作方法。

2.根据yuanbanban大佬的教程 +++整合大气层就像搭积木，欢迎讨论+++，所以如对Hekate的启动设置不喜欢，就修改“迷你包”的设置，而特斯拉插件包和相册NRO软件包都通用，可用在任何大气层整合包上，还可以根据说明书删掉不需要的插件。

3.谢谢paulzheng大佬的教程浅谈玩家的大气层atmosphere个人整合包。虽一开始看得云里雾里，但跟着前面大佬的整合包琢磨之后回过头再来就很好懂了。

现在我根据大佬们教程，对平时用的整合包进行了重编，插件只留特斯拉和超频，相册也只有下面这个，平时用的超级稳定，感谢，哈哈哈哈哈！

第二弹：乐享纯净包+乐享搭配包=乐享大气层整合包

乐享纯净包，https://www.91tvg.com/thread-296138-1-1.html

乐享搭配包，https://www.91tvg.com/thread-296598-1-1.html

第三弹：发布奇想大气层纯净包

奇想纯净包，https://www.91tvg.com/thread-297945-1-1.html

大气层原版引导和Fss0引导没有大的区别，这几天研究了Hekate_ipl的启动设置，已经搞懂Fusee引导，Fss0引导的区别。就这4点

1.Fusee引导只要Atmosphere能支持SW最高系统破解就可以，Fss0引导要满足Hekate和Atmosphere同时支持SW最高系统的破解。

2.Fusee引导和Fss0引导的sigpatch中的FS和Loader补丁位置不一样，进入系统玩破解，玩插件和软件都没有区别。

3.Fusee引导是通过EMUMMC.ini自动识别虚拟系统和真实系统，有虚拟就进入，没有虚拟或者虚拟关闭就进入真实系统。

4.最重要的是Fss0引导可以设置为定向虚拟系统或者真实系统，但是它也可以像Fusee引导一样自动识别真实系统和虚拟系统。

看下面这个Hekate_ipl中的设置

1. Fusee引导

[ATM-AUTO]

payload=bootloader/payloads/fusee.bin

icon=bootloader/res/fusee.bmp

2. Fss0引导，定向虚拟

[ATM-EMU]

emummcforce=1

fss0=atmosphere/package3

kip1patch=nosigchk

atmosphere=1

logopath=bootloader/bootlogo.bmp

icon=bootloader/res/emunand.bmp

所以看上面，只要删掉emummcforce=1，就变成了fss0引导的自动识别，也是大气层自动识别。对于Fusee引导，就是payload是fusee.bin，对于Fss0引导，就是fss0=atmosphere/package3，另外加上kip1patch=nosigchk，atmosphere=1作补充就可以了。

