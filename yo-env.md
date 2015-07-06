#yo在项目中的应用之环境配置

    yo的应用之环境配置
    ├── 辅助工具安装
    │   ├── compass安装 
    │   └── gulp安装
    │
    └── yo的安装及目录划分
        ├── yo安装
        └── 构建工具本地安装
    




# 辅助工具安装
## compass安装 
> 功能：sass去重，因为fekit暂时不具备去重，而compass可以解决这个问题，即安装compass去重，等fekit具备之后就不用安装了，官网 http://compass-style.org/

	
```
$ gem update --system 
$ gem install compass 
```

* 问题：由于国内网络原因（你懂的），导致 rubygems.org 存放在 Amazon S3 上面的资源文件间歇性连接失败。解决方案RubyGems 镜像-淘宝网 http://ruby.taobao.org/

## gulp安装
> 功能：sass编译工具	

	$ npm install --global gulp




# yo的安装及目录划分

##yo安装

### 方法一

	$ npm install fekit-extension-yo
	$ fekit yo -i
	
### 方法二
直接clone git@github.com:doyoe/Yo.git
复制lib目录

##构建工具本地安装

    $ npm install

##目录划分及文件夹的功能

https://github.com/guhuina/yo-useage/blob/master/yo-workingFolder.md




