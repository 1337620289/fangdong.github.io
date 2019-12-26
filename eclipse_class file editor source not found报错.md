# eclipse:class file editor source not found报错
具体的错误代码如下：
```javascript
java.lang.ClassNotFoundException: Didn't find class "XXX.XX.XXX.XXXView" on path: DexPathList[[zip file "/data/app/XXX.XXX.XX-1.apk"],nativeLibraryDirectories=[/data/app-lib/XXX.XXX.XX-1, /vendor/lib, /system/lib]]
```
这个问题我遇到了，刚开始也是不知道怎么解决摸不到头脑，找老师问了问
也没有解决，最后还是在网上寻找到了解决办法。

方法有很多，我就说一下我自己解决问题的方法吧。
	
就是要将自己的sdk重新压缩一下，再导入到自己的class就行了。

例如我的，下图是我的sdk目录，只需要将sdk压缩重新导入即可。
![sdk所在目录](https://img-blog.csdnimg.cn/20191226140038185.png)
导入完成就没有这个报错啦，亲测有效！
