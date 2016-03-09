# uploadJcenter
##### [Jcenter](https://bintray.com/bintray/jcenter)是类似maven仓库的网站。

android推荐使用它来分享aar，格式为:

&emsp;compile 'groupId:定义的项目名:项目版本'

&emsp;compile 'com.android.support:appcompat-v7:23.0.1'

&emsp;com.android.support 就是android为support定义的gruopId,

&emsp;appcompat-v7即关于v7兼容包的appcompat,23.0.1是定义为android 6.0的兼容.

这个技能点还是要点出来的，就去学习了，然后分享一下。不过，网上资料还是蛮多的，把我借鉴的资料也列出来.
其实还是有很多已经总结出来的经验，因为已经前辈为我们开辟出了道路，坑坑洼洼也全踩遍了.

##### experience
&emsp;1.在成功上传完了一个项目之后，当我下次又去上传的时候，发现，按照之间的配置总是出现401错误，总是不成功。检查好几遍，并没有发现错误所在。在之后一个偶然，通过一个帖子上，他说他的401是username写错了,我之前上传成功，那么username肯定没有错.那么导致401的就是key了.我重新进入到bintray网站，复制了key，发现，与之前使用的是不一样的。距离上次使用bintray，过去了1个月吧。经过这个教训，发现bintray网站的key是会改变的，我猜，应该是一个月变化一次，特此记载。


##### 如何使用

- app-build.gradle

  你的library module下的build.gradle
- 项目-build.gradle

  Android studio项目下的主build-gradle
- local.properties

  Android studio项目下的默认的一个忽略文件
  
  我们在里面配置一下key等信息,但是不会上传到github

##### 资料

- [使用Gradle发布项目到JCenter仓库](http://rocko.xyz/2015/02/02/使用Gradle发布项目到JCenter仓库/)
- [如何使用Android Studio把自己的Android library分享到jCenter和Maven Central](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0623/3097.html) 
- [Android 项目打包到 JCenter 的坑](http://www.jcodecraeer.com/a/anzhuokaifa/Android_Studio/2015/0515/2873.html)
- [5分钟发布Android Library项目到JCenter](https://github.com/xiaopansky/android-library-publish-to-jcenter)
- [免费翻墙利器-蓝灯](https://getlantern.org/)

