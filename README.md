# zhuabao
今天给大家介绍一款mac版抓包工具.[抓包工具下载地址](https://github.com/mar-sir/zhuabao/blob/master/mitmproxy-0.17.1-osx.zip)点击download下载.你也可以搜索mitmproxy关键 字下载.为了使用方便，我们先配置一下mac的环境变量
##环境变量配置
* 打开Finder,按shift+alt+h键，找到Program文件夹并打开新建一个文件夹名字叫'zhuabao'(名字任取):
![](https://github.com/mar-sir/zhuabao/blob/master/step1.png?raw=true)
* 打开.bash_profile文件，这里我在终端输入 atom ./.bash_profile,我是用atom打开的这个文件，你们可以用其他方式打开，不会的自行google或着百度.
在添加两句话：
        export zhuabao=~/Program/zhuabao
        export PATH=$zhuabao/bin:$PATH
   如图:
![](https://github.com/mar-sir/zhuabao/blob/master/step2.png?raw=true)

* 以上完成的话，只要把下载好的压缩包解压以后放到Program下面的zhuabao文件夹即可。如图:
![](https://github.com/mar-sir/zhuabao/blob/master/step3.png?raw=true)
配置完毕!之后在终端输入 source ~/.bash_profile,让修改立即生效,在终端输入 zhuabao(你放在Program/zhuabao里面你修改的名字)，回车，如果出现如下图
![](https://github.com/mar-sir/zhuabao/blob/master/step5.png?raw=true)
则大功告成一阶段。
[配置环境变量可参考](http://www.cnblogs.com/caowei/p/mac-path_2013-08-26.html)
##抓包演习
####设置代理
将手机和电脑连接同一wifi，然后看图：
![](https://github.com/mar-sir/zhuabao/blob/master/step4.png?raw=true)
####电脑端操作
```
mitmproxy -b ip -p port
代理:   手动 
主机名: ip
端口:   port
```
打开终端，输入zhuabao（你自己修改的名字） -b  ip(你本机IP地址) -p 3563（你的代理端口号，这里我之前设置的是3563）,回车，然后我们用自己的手机
打开一个网站，你就可以在你自己的终端上看见：
![](https://github.com/mar-sir/zhuabao/blob/master/step6.png?raw=true)
双击其中一条你可以发现：
![](https://github.com/mar-sir/zhuabao/blob/master/step7.png?raw=true)
写到这里已经说完了。
##补充
在这个工具里面，q（返回）,C（清除所有缓存）,?(帮助)，至于更多的功能有待各位开发。 
