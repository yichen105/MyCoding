# 环境的搭建
- 1.[Apache Tomcat下载](http://mirror.bit.edu.cn/apache/tomcat/tomcat-8/v8.5.34/bin/apache-tomcat-8.5.34-windows-x64.zip)

在google上搜索**apache tomcat 8 download**
![](https://raw.githubusercontent.com/dengxiangliu/MyWebSite/master/SSH/SetImage/11.png)
上面是下载apache tomcat 8，我们这里用的是8的版本。

![](https://raw.githubusercontent.com/dengxiangliu/MyWebSite/master/SSH/SetImage/22.png)

- 2.[Eclipse下载](https://www.eclipse.org/downloads/packages/)
![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/33.png)

**安装Eclipse略**

# Eclipse里面找不到server选项
在Eclipse中，窗口(window)——首选项(preferences)——服务器(Server)——运行时环境(Runtime Environments) ——添加(Add)，添加Tomcat服务器。对应安装的Tomcat版本选择Apache Tomcat v8.0。下一步通过“浏览(Brower)”按钮选择之前Tomcat的安装目录，指定后点击“完成”完成配置。

问题在于我的Eclipse为新版本2018-09 R,显示如图，没有server选项。

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/44.png)

**解决的方法如下：**
![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/55.png)


![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/66.png)


[kepler的网址是](http://download.eclipse.org/releases/kepler/):http://download.eclipse.org/releases/kepler/


![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/77.png)

安装完成后，server就有了，如下：


![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/88.png)


后面就可以按照常规知道的进行配置Tomcat了

# 解决java compiler level does not match the version of the installed java project facet

我第一次安装Eclipse,并且将环境搭建好之后，新建了第一个项目，报“java compiler level does not match the version of the installed java project facet”错误。如下：

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/99.png)

要解决这个问题的话，我们先找到项目所在的目录，在.settings子目录里面，用文本编辑器打开org.eclipse.wst.common.project.facet.core.xml配置文件，如图所示：

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/10.png)

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/101.png)

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/102.png)


修改蓝色画线的部分，让它与项目的编译器版本设置保持一致即可。

## 如何查看项目的编译器的版本呢？
要查看项目的编译器版本设置，在Eclipse环境中，鼠标右键选择项目，点击Properties，选择Java Compiler，可以在窗口右边看到编译器版本，如图所示：

![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/103.png)


![](https://github.com/dengxiangliu/MyWebSite/blob/master/SSH/SetImage/104.png)











