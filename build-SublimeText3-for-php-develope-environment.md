### Sublime Text 3 配置适合PHP的开发环境

> 虽然有很多优秀的PHP集成开发环境，但是我自己比较喜欢使用文本编辑器来进行PHP开发。
一方面原因是文本编辑器启动迅速、轻量；另一方面原因是PHP集成开发环境如Zend Studio这类基于Eclispe开发的集成环境经常抽风。
所以Sublime Text便成了我的开发首选文本编辑器。

话不多说，开启我们的Sublime Text的配置之旅吧：

##### 一、下载Sublime Text 3
Sublime Text [下载地址](http://www.sublimetext.com/3)

##### 二、安装Sublime Text包管理工具：Package Control
* 2.1 通过工具栏View -> Show Console 或简单的 *"Ctrl + `"*快捷键调起控制台，并输入

`` import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read()) ``

* 2.2 安装完成就可以在Preferences工具栏下看到 *Package Control* 及*Package Setting*选项

**Pcakage Control使用**

使用*" Ctrl + Shift + P  "*快捷键唤起命令行输入框，输入``install``选择*Package Control:install package*选项进入包安装命令行

#### 三、下面开始下载PHP开发的插件
###### 3.1 PHP开发插件
DocBlockr：自动给函数变量增加注释功能，它支持的语言有Javascript, PHP, ActionScript, CoffeeScript, Java, Objective C, C, C++

Sublime CodeIntel:：代码自动提示

Alignment ：代码对齐

ConvertToUTF8：支持 GBK, BIG5, EUC-KR, EUC-JP, Shift_JIS 等编码的插件

###### 3.2 JavaScript插件
JsFormat：JS格式化

###### 3.3 Html插件
Emmet：HTML代码生成器

###### 3.4 其它插件 
FileDiffs：文件夹比较插件
[Side Bar](https://github.com/titoBouzout/SideBarEnhancements)：增强边侧栏
[AutoFileName](https://github.com/BoundInCode/AutoFileName):自动补全文件路径

#### 四、编程字体及主题
字体：InputMono[Input: Fonts for Code](http://input.fontbureau.com/) 

主题:


##### 参考资料

1. [Sublime Text 3设置吊炸天PHP开发环境](http://blog.csdn.net/heiyeshuwu/article/details/51859571)
2. [sublime text 3 插件：package control] (http://frontenddev.org/article/sublime-does-text-3-plug-in-package-control.html)
3. [Sublime Text 3 绝对神器](http://www.cnblogs.com/bananaplan/p/Sublime-Text-3-Powerful.html)
4. [使用Emmet加速Web前端开发] (http://www.w3cplus.com/tools/using-emmet-speed-front-end-web-development.html)
5. [超全Sublime Text指南](https://github.com/jikeytang/sublime-text)
6. [有哪些适合用于写代码的西文字体](https://www.zhihu.com/question/20299865)
