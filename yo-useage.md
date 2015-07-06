#yo在项目中的应用之使用
> yo 官网：http://ued.qunar.com/mobile/yo/demo/

## config文件
> config文件的作用是重新定义yo变量，从而生成我们项目style

1. 参考lib/variables.scss 设置$setting, $base, $media-types, $ico, $flex...
2. 安需要配置$loading, $input, $btn, $badge...
3. 在模块中引入yo元素的样式代码



## 扩展mixin的使用
> 当我们的元素不单有一种style的时候，引用mixin



##案例 

### config.scss文件

    $loading: (
        // {Length} 菊花大小
        ico-size:     .5rem,
        // {Color} 菊花颜色
        ico-color:    #212121,
        // {Color} mask颜色
        mask-bgcolor: rgba(0, 0, 0, .1),
        // {Color} 背景颜色
        bgcolor:      null,
        // {Length} 字号
        font-size:    .14rem,
        // {Color} 文本颜色
        color:        map-get($base, color),
        // {String} loading的ico编码，自定义的webfont
        content:      "\f089"
    );

	
### Element文件夹下yo-loading.scss文件

	@import "../../lib/element/yo-loading";

	//mixin的使用
	@include yo-loading(
    	$name: b,
    	$bgcolor: #666,
    	$mask-bgcolor: rgba(0, 0, 0, .2),
		$ico-color: #00afc7,
    	$color: #00afc7
	);

