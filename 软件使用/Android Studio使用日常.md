# Android Studio使用日常 

[TOC]

# 1.常用快捷键

 - `Ctrl+Alt+F` 提取全局变量(快速将局部变量变为全局)

 - `alt+enter` 这个是`Android Studio`神快捷键。如果你还认为`Alt＋Enter`键是导入包，那就大错特错了。以后有事没事就按下吧。它会根据不同的情况给出操作建议，大大提高工作效率。

 - `Ctrl+Alt+V` 快速将返回的东西定义成对象(类似于`eclipse`的`ctrl+2`)

 - `alt+shift+r`  快速重命名

 - `Ctrl+Alt+Space`:智能提示代码

 - `alt + insert`  快速实现父类的构造方法(getter,setter,equals,hashCode,toString等)

 - `Alt+Shift+P`:实现接口方法
 - `Ctrl+Alt+T` : 快速实现很多东西,比如`if/else`,`try_catch`
 
![](http://olg7c0d2n.bkt.clouddn.com/17-2-26/48308793-file_1488118565497_bfe1.png)

 - `Ctrl+delete`(或`Ctrl+Backspace`) 快速删除当前单词

 - `Ctrl+Q`  快速返回刚才编辑的地方
 - `Ctrl+O`  重写父类的方法(还可以跳转到某个方法所在行)
 
 - `Shit+Alt+M` 提取方法
	
 - `shift+F10`  快速运行项目
 - 快速遍历集合:你可以输入myList.for，然后按下Tab键，就会自动生成for循环代码。	
 - `ifn`  快速补全代码,判断是否变量为null

 - 按两次Shift:Search Everywhere

 - `Alt+1`  项目显示/隐藏

 - `Ctrl+shift+R`  Go To File

 - `Ctrl+E` 打开最近文件列表

 - `alt+home` 导航栏

 - `Ctrl+P` 显示所选方法的参数

 - `Ctrl+ -`快速折叠当前的代码块

 - `Ctrl+ +`快速展开当前折叠的代码块

 - `Ctrl+Shift+ -` 快速折叠所有代码

 -  `Ctrl+Shift+ +`  快速展开所有折叠的代码

# 2.Logcat使用

>打开 `LogCat`在搜索框右侧的`No Filters`中选择 `Edit Filter Configuration`选项,然后在`Name`中输入过滤器的名称，在`by Package Name`中输入你的应用的`Package Name`就可以了。然后在搜索框右侧的过滤器选项中选择你刚选择过滤器就可以了。

- logi 自动补全一条完整的打印语句(还有logd等)

# 3.快速生成构造函数,Setter,Getter,ToString()方法

>在类中,有两种方式：

 - 方式一：Code-->Generate
 - 方式二：通过快捷键`Alt+Insert`

# 4. 关于VersionName和VersionCode

在 Android Studio 中，对于 VersionName 和 VersionCode 的声明转移到了 Module 的build.gradle文件中。请修改build.gradle 的以下部分

		defaultConfig {
	        minSdkVersion 16
	        targetSdkVersion 21
	        versionCode 2
	        versionName "2.0"
	    }

# 5. 获取Android机中的文件
>利用Android Device Monitor工具

点击`Android Studio`导航栏中的`Tools`->`Android`->`Android Device Monitor`,效果如下图:

![Android Device Monitor工具](http://olg7c0d2n.bkt.clouddn.com/17-2-24/49351660-file_1487943471539_4208.png)

和eclipse上面的简直一毛一样.爽....

# 6. 在代码中快速跳转至函数的api

![](http://olg7c0d2n.bkt.clouddn.com/17-2-27/71297359-file_1488172308728_20ad.png)

如图,当需要查看该函数有什么功能,或者该类.直接点击这个按钮即可快速跳转到该函数的api(会打开浏览器).该按钮的快捷键是`Shift+F2`

# 7. 将源码大小浓缩

将源码根目录下的build和app下面的build删除,源码瞬间从几十M变为几百K

# 8. 引入别人的SDK

- app模块下有个libs目录,用来存放Jar包的

- src/main/jniLibs  这里是专门用来存放so文件的

# 9. 在Android Studio中使用实时模板

- newInstance - 在Fragment中生成静态newInstance函数
- Toast - 生成 Toast.makeText(context, "", Toast.LENGTH_SHORT).show();
- fbc - 写出findViewById并cast
- const - 定义一个android风格的int常量
- logd - 生成 Log.d(TAG, "");
- logm - 记录当前方法名称及其参数
- logr - 当前方法的result结果
- logt - 静态logtaf与当前类名
- **psf** - public static final
- sout - 将字符串打印到System.out
- soutm - 将当前类和方法名称打印到System.out
- soutp - 将方法参数名称和值打印到System.out
- visible - Set view visibility to VISIBLE
- gone - Set view visibility to GONE
- noInstance - 私有空构造函数来禁止实例创建

# 10. 后缀代码在Android Studio中完成

  + `<expr>.null` will auto complete to `if(<expr> == null)`
  + `<expr>.nootnull` will auto complete to `if(<expr> != null)`
  + `<expr>.var` will auto complete to `T name = <expr>`
  + `<expr>.field` will auto complete to create a global field variable `field = <expr>`
  + `<ArrayExpr>.for` will auto complete to `for(T item : <Arrayexpr>)`
  + `<ArrayExpr>.fori` will auto complete to `for(int i = 0; i < <Arrayexpr>.length; i++)`
  + `<ArrayExpr>.forr` will auto complete to `for(int i = <Arrayexpr>.length - 1; i > 0 ; i--)`


Complete list of available postfix code completion can be found at **Settings** → **Editor** → **Postfix Templates**

# 11. 全局搜索替换

1.选中要替换的项目。

2.右键选择“Replace in Path..”

3.搜索要替换的字符串，find 键 替换即可
