# MultiResolutionMatching(Android 屏幕适配方案)

-----------------
####在这里感谢鸿洋大神，以上文件也是来自于大神的 <a href="https://github.com/hongyangAndroid/Android_Blog_Demos/tree/master/blogcodes/src/main/java/com/zhy/blogcodes/genvalues">github</a> ，详情可以参阅<a href="http://blog.csdn.net/lmj623565791/article/details/45460089">CSDN博客</a>

</p>
##一、默认支持分辨率

	
		| screen size  |
		| -----------  |
		| 480 x 320    | 
		| 800 x 480    | 
		| 854 x 480    |
		| 960 x 540    |
		| 1024 x 600   |
		| 1184 x 720   |
		| 1196 x 720   |
		| 1280 x 720   |
		| 1024 x 768   |
		| 1280 x 768   |
		| 1280 x 800   |
		| 1812 x 1080  |
		| 1920 x 1080  |
		| 2392 x 1440  |
		| 2560 x 1440  |
		
##二、用法

 
 
 * 命令格式
 			
 			java -jar AutoLayout.jar width height width,height_width,height
 			
 		
* 格式解析

	*	第一个width和height 是屏幕分辨率的基准，例如：应用UI效果图是按照 1920 * 1080个分辨率来做得，我们就生成按照这个分辨率来做基准，命令格式如下：java -jar AutoLayout.jar 1080 1920 就可以了。
	
	*   支持额外的分辨率。如果默认支持的分辨率没有当前的分辨率，则需要额外的添加 width,height_width,height 
		height_width 例如：我们需要额外支持 2310 x 1440 和 1840 x 1080 这个两个分辨率 1440,2310_1080,1840,完整命令如下：java -jar AutoLayout.jar 1080 1920 1440,2310_1080,1840

			 		
##三、效果
<img src="https://github.com/jiaowenzheng/MultiResolutionMatching/raw/master/20150503173719049.gif" width="800" height="400"/>  
