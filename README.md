# idea-setting
idea setting
<br>
# IDEA自动编译不用每次make<br>
解决idea编译慢问题<br>
https://my.oschina.net/1987times/blog/330207<br>
开启自动测试 部分在新版的为止是preference<br>

# 在Intellij IDEA中使用Debug<br>
https://www.cnblogs.com/chiangchou/p/idea-debug.html

# intellij idea怎么打开outline，即像Eclipse中的在右边显示某个类的所有方法
https://blog.csdn.net/LWJdear/article/details/76687652

# intellij idea设置默认工作目录<br>
https://blog.csdn.net/sljackson/article/details/79655427<br>

# Intellij IDEA 快捷键整理<br>
https://www.cnblogs.com/tonycody/p/3257601.html<br>

# IntelliJ IDEA 自动导入包 快捷方式
https://blog.csdn.net/hxpjava1/article/details/78135934<br>
setting在新版是preference<br>


# IDEA中怎么设置黑色或白色背景？
https://blog.csdn.net/jiangyu1013/article/details/79479687<br>

# IDEA连接Git

https://www.cnblogs.com/bongxin/p/5945085.html

摘要: Intellij IDEA作为最强大智能的IDE，内部已经集成了Git的功能，所以不用安装插件，连接Git@OSC也非常容易

首先安装git for windows 推荐使用这个：http://msysgit.github.io/ 

可以在任何目录 右键——git bash 弹出对应路径的 git 命令行窗口 而且启动速度比较快

在Intellij中Settings——Version Control——Git——Path to Git executable

找到安装git  bin目录下的git.exe



1.方法一  适用于新建项目
先在Git@OSC上创建仓库  拿到Git@OSC仓库的HTTP连接http://git.oschina.net/lujianing/GitOSC.git

在Intellij IDEA工具栏中 VCS——Checkout from Version Control——Git 粘贴 URL 然后点击CLONE 

会创建并且复制仓库文件到本地项目中  然后你就可以在本地项目中进行Git  add commit等操作了

最后可以在项目中Git ——Repositroy——PUSH  提交到Git@OSC中了（第一次提示输入账号密码）

就是这么简单 有木有....

下面是对应的一些截图













 
2.方法二  适用于已有项目
先在Git@OSC上创建仓库  拿到Git@OSC仓库的HTTP连接http://git.oschina.net/lujianing/test2.git

如果本地项目非Git项目 首先把项目变成Git的项目

在intellij中 VCS——Import into Version Control——Create Git Repository  选择你的本地项目 

通过git shell （可以安装git for window） 进入到项目目录 执行 

git remote add origin http://git.oschina.net/lujianing/test2.git

git push -u origin master  （这个是命令行提交项目可以不用执行  参考方法一中在intellij中push）

如果提交失败 请参考git提示进行解决  比如已经有remote地址 可以git remote rm origin清除

如果是仓库中有其他文件  本地项目中没有 可以参考后两个图 首先merge项目 

项目就提交到Git@OSC了   以后的再有修改提交仓库就可以参考方法一的push操作了 

就是这么简单有木有

下面是对应的一些截图











转自：https://my.oschina.net/lujianing/blog/194069

 
