##yo目录命名规则及功能

### src文件夹下创建yo文件夹
> 用yo来替换之前的style文件夹

### yo文件夹下创建lib和usage
* lib放置yo的框架的基本代码（注意里面的代码不能改）
* usage放置业务代码

### usage下创建core,layout,page,module,common,export文件夹及config.rb, gulpfile.js, package.json文件（下载file）
* core 包括
* layout 布局
* page 页面级样式通常是对module的引用，每个页面建立一个page页面
* module 定义的模块m-开头的模块（包括g-）
* common g-开头 公用的片段，比module小
* export 最后编译的.css文件
* config.rb 功能：解决sass import去重
* gulpfile.js 功能： 编译.sass文件为.css文件
* package.json 功能：安装gulp，及gulp-conpass等构建工具

### 当我们需要引用yo提供的像yo-btn，yo-list，yo-header时就需要在usage下建立与yo lib相对应的element，fragement,widget

* element 放置引用yo元素及扩展 eg:yo-btn.scss代码
	
```	
	@import "../../lib/element/yo-btn";
	@include yo-btn(
		$name: buy,
		$bgcolor: $bg-light-color,
		$color: $white,
		$bordercolor:$bg-light-color,
		$radius: 2px
	);

```

* fragement 放置引用yo组件及扩展 eg：yo-header.scss

```
@import "../../lib/fragment/yo-header";
// 扩展统一的header
@include yo-header(
    $color: #fff,
    $item-color: #fff,
    $item-ico-size: .2rem
);
```

* widget 放置引用yo组件及扩展 eg：yo-tab.scss

```
@import "../../lib/widget/yo-tab";
@include yo-tab(
    $name: "switch",
    $height: .28rem,
    $font-size: .14rem,
    $on-bgcolor: #fff,
    $on-color: $text-light-color
);
```

目录结构图

![](http://guhuina.github.io/images/yo/pic.png)



##案例
当拿到ui稿时，首先看一下哪些可以用yo提供的模块，哪些需要自定以模块例如：

![](http://guhuina.github.io/images/yo/pic2.png)


