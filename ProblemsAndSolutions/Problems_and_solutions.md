作者：Luwen Zhang  
- 为了记录在整个毕业设计完成过程中所遇到的问题，以便于后期再次遇到相同问题时快速解决；
- 为在开发过程中遇到同样问题的同学提供有效的解决办法。
    
这里提供一个文件来记录上述内容，解决方法供参考。    

### 【问题1】  
**问题描述**：在尝试第一个AR Demo过程中，很多教程中会提到安装初期即选择Vuforia进行安装，但是我的选项并没有这个模块。Mac Unity 2019.2.21f1    
**解决办法**：新版的unity在下载时没有选择「Vuforia」这个模块。在下载时仅需下载需要的开发平台（mac，linux，android或Ios等），在完成下载并启动unity时，在「Package Manager」中选择加载「vuforia engine」即可。    

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/Problem1_a.jpg" width="50%" height="50%"/></div>     
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/Problem1_b.jpg" width="50%" height="50%"/></div>     

### 【问题2】  
**问题描述**：网上或是参考书中的内容在进行Vuforia完成第一个AR demo时都有提及到关于「XR setting」的修改,例如[Unity+Vuforia AR入门](https://www.jianshu.com/p/2fc8c986d57d) ,然而在我自己开发的过程中都没有找到这些设定修改的位置。    

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/Problem2.jpg" width="50%" height="50%"/></div>     

**解决办法**：在学习了相关教程后,思考认为可能是当前unity 版本过新。曾经出现的问题已经都修复好，现在无需进行此类冗杂的操作，也可能是mac端无需进行这些操作。       
在跳过了各类教程中这部分的步骤后，直接进行接下来的操作（如建立AR Camera，导入ImageTarget等），再运行程序，发现并未报错。   


### 【问题3】  
**问题描述**：学习过程中了解到Vuforia主要使用各种「识别」的方式来实现AR效果，然而本毕业设计并不涉及到图像识别。  

**解决办法**：在b站[ARKit入门](https://www.bilibili.com/video/av77532231)，Youtube等浏览了很多的相关学习视频。vuforia更适合于识图展示模型，ARKit无需图像识别，可以直接在当前屏幕上显示模型并对其进行处理，更适合于本毕业设计这种家居测量与模型演示的功能[演示视频：HouseAR-基于ARKit的增强现实应用](https://www.bilibili.com/video/av36920062)。  
尽管已经花费了一些时间学习了Vuforia，但是为了提高本应用的适用性以及可开发性，决定更换使用ARKit以完成后续的工作。  

### 【问题4】  
*注：对于本问题出现的原因我尚未了解，以下解决办法仅针对本情况.*   
**问题描述**：在将本地文件使用git提交到远程仓库，以及初始化git时遇到了一些问题。 在生成ssh，复制ssh，关联仓库，登陆 git@github.com 账号后都没有问题，在进行push文件时，会出现git push 时出现「Connection closed by remote host」或「Connection reset by peer」。  
**解决办法**：
- 关于「Connection closed by remote host」的问题，很多网友解释可能是[对应问题：路由器的影响](https://segmentfault.com/q/1010000006743721/a-1020000006743912)，对于这一部分其实我不是非常理解。但是对于部分回答中提到的「全局代理」等，考虑到我的电脑没有任何路由器加速设备，若是网络有影响或被拦截的话仅可能是SSR的影响。    
- 此外，部分遇到同样问题的网友解释为是网络权限限制，开启公司VPN，调整为公司内网即可。  
- 最直接的解决办法是：在使用push上传代码时，关闭ssr；对于内网等问题，在关闭ssr之后，开启了GlobalProtect(BUPT VPN)。  
- [Connection closed by remote host的对应问题：网络劫持](https://blog.csdn.net/solo_ws/article/details/52484388)，按照其中的方法，在host中加入GitHub的IP。  
~~~ 
1.# 进入终端   
sudo vi /etc/hosts  
2.# 输入 password
3.# 进入hosts，按“i”，进入编辑模式，添加host
192.30.253.112 github.com
4.# control+c 退出编辑模式
5.# 输入 :wq ，保存退出#
~~~  
全部完成上述步骤后，再次输入`git push/pull origin master`即可成功完成了从git上pull代码以及push代码到仓库上。  

### 【问题5】   
**问题描述**：在转换为使用ARKit开发之后，使用苹果生态原生开发平台进行开发。在使用XCode的ARKit，并且将在模拟器上运行完成的代码运行到真机(IPad Pro)上时，遇到了以下问题。  
1. This device is running iOS 13.3 (17C54),which may not be supported by this version of Xcode.[问题及解决参考](https://www.jianshu.com/p/49784194c913)      
2. device is busy：preparing debugger support for iPhone.    
3. Development cannot be enabled while your device is locked.       
4. [iOS真机调试问题](https://www.jianshu.com/p/99c441070b22)「The maximum number of apps for free development profiles has been reached.」  

**解决办法**：  
1. 在https://github.com/iGhibli/iOS-DeviceSupport 找到对应版本的支持文件放到` /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport `目录下。    
2. 等待。或者重启XCode，并且在IPad上删除对应的apk，再次构建项目。    
3. 原因是电脑与Ipad尚未互相信任，在将Ipad连接到Mac时都需要选择「信任本台设备」。此外，在iPad端，进入`设置->通用->设备管理->开发者app->进入对应的app`进行验证，完成验证后即可正常运行。    
4. 苹果的免费App ID只能运行2个应用程序，连接iPad 打开`Xcode->Window->Devices`，删除非本次运行的程序或者在iPad直接卸载应用也可。  

### 【问题6】    
**问题描述**：在完成平面检测代码的过程中发现缺失PlaneNode这一个类的内容，尚未找到对应文件。      
**解决办法**：  
&#8195;因为在参考书籍的后面的学习中都会接着前面的开发继续，在解决了这一个问题之后才可以进行后续的问题。否则暂时使用其他的方式进行同样功能的实现，尚不了解会对未来的开发造成什么影响。      
&#8195;对于平面检测，在网上找了其他教程同样实现了该功能。在部分代码中找到了类似作用的文件，如Plane类等。    
&#8195;在不断的寻找中，在CodeForge上找到了一个比较接近的文件[提供了PlaneNode.h的工程](http://www.codeforge.cn/article/522070)。阅读了其工程内对应的ViewController.m文件，发现对于「添加锚点」这一实现方式基本一致。  
&#8195; **0308**补充：
关于PlaneNode类，不同的教程有不同的实现方式。但是大同小异，我找到的这个也不能完全替换，也要根据接口进行实际的修改才行。对于平面上锚点的更新与删除，主要分成   
~~~  
initWithPlaneAnchor;  
updateNodeWithPlaneAnchor;    
planeNodeWithAnchor;  
removePlaneNodeWithAnchor; 
~~~  
四个函数内容。按照可成功运行的工程文件，仿照完成上述四个功能函数即可，不必过分限制于同名文件。  

### 【问题7】  
iOS开发系列   
**问题描述**：The entitlements specified in your application’s Code Signing Entitlements file are invalid, not permitted, or do not match those specified in your provisioning profile. (0xE8008016).    
**解决办法**：[类似问题参考](https://www.jianshu.com/p/1ba52e347490)，但是我自己只是重启XCode再重新构建即可。


### 【问题8】  
iOS开发系列  
**问题描述**：[access] This app has crashed because it attempted to access privacy-sensitive data without a usage description.  The app's Info.plist must contain an NSCameraUsageDescription key with a string value explaining to the user how the app uses this data.  
**解决办法**：本问题出现在构建他人的工程文件时。同样是ARKit系列的项目代码，在下载到本地进行构建尝试时，需要在info.list文件中的Information Property List加入对应camera的权限。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/info.list_1.png" width="50%" height="50%"/></div>      

同时，还要在Required device capabilities中加入新的item-arkit。只有完成上述两个设置后，才可以成功运行他人的示例代码。  

### 【问题9】 
**问题描述**：对于在unity中使用ARKit的方式，也发现了一些教程中有提到关于unity和iOS原生代码的交互问题。  
如何在Unity中加入已经在iOS原生平台上完成的功能，在unity中使用arkit sdk并生成iOS应用文件，是接下来要解决的问题。  

### 【问题10】
**问题描述**：在目前的开发中，使用到的模型都是苹果官方或者样例代码文件中使用到的模型文件，部分模型文件为.scn。  
有一些教程中有提到使用3d Max导出.scn文件，这一部分还没有尝试。  
如果使用unity的话是否模型的格式可以放宽呢？  
需要解决的是：之前找到的家具模型库的模型文件是否可以使用，且是否可以通过别的建模软件导出为所需的文件。  

### 【问题11】
**问题描述**：Unity-ARKit-Plugin在asset store中不再支持  
**解决办法**：好像是因为unity现在比较推ARFoundation，也就是ARKit和ARCore的整合插件。网络上大部分教程中所提到的插件Unity-ARKit-Plugin在asset store中不再支持，只能在网络上找网盘下载了....如有哪位同学需要该package可以联系我。  

### 【问题12】  
**问题描述**：测试样例ARKitRemote运行起来非常的卡顿，界面刷新非常慢。  
**解决办法**：几乎已经卡到没办法有任何有效的操作了，只是可以运行，但是console还是输出了许多错误。   
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/screenshot_arkitremote_test1.jpg" width="50%" height="50%"/></div>   

以上这种远程的奇怪工程我不再试了，所以这些问题我也不准备解决了。解决本问题的方式是逃避问题。下方是在csdn博客上找到的其中一种解决办法，未尝试，供参考。  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/ARkitRemoteStuck.png" width="50%" height="50%"/></div>  

### 【问题13】  
**问题描述**：ARSession中arsession.Raycast()函数丢失  
**解决办法**：参考：[unity中的提问Foundation AR, ARSessionOrigin doesn't reconize the Raycast method?](https://forum.unity.com/threads/foundation-ar-arsessionorigin-doesnt-reconize-the-raycast-method.680296/#post-5324931)以及
[在教程作者的github上的issue中的问题ARSessionOrigin has no member Raycast](https://github.com/TheUnityWorkbench/tuw-arfoundation-demo/issues/1)  
package manager中有提供ARKit，ARFoundation等包。注意不同版本下有细微的差别，比如ARKit 3.0版本就没有Raycast函数了，只能降级回1.0.0进行操作。当然，同样的功能可以使用新版本中其他的函数进行替换。   

### 【问题14】  
**问题描述**：.max文件只能用3dmax打开，而且我的MacBook pro不能安装3DMax  
**解决办法**：已经让别人把我的小dell邮寄过来了...    

### 【问题15】  
**问题描述**：近期运行的工程文件太多，而免费的开发app ID只有十个，会报以下错。  
**解决办法**：见参考[iOS真机调试-Your maximum App ID limit has been reached. You may create up to 10 App IDs every 7 days](https://www.jianshu.com/p/3e0669c23a89)。所以，开发之前确认好要设定的参数，每一次使用同样的开发者名称即可。出现了这个问题就是使用曾经用了的bundle ID即可。  

### 【问题16】
**问题描述**：考虑到unity中对ui的设计有限制，之前考虑的是iOS和unity进行交互使用，本周尝试了一下。iOS和Unity的切换的确有很多教程，但是步骤特别的多，很多设置和调整我都不知道原因....现在还没有完全实现二者的结合。    
**解决办法**：向丑陋的界面屈服。为了不影响开发进度，还是先使用了Unity的一些ui。  
接下来还是要继续尝试整合。  
- [unity与原生iOS项目的整合（一）](https://blog.csdn.net/Elena_engineer/article/details/75969617)     
- [Unity导出的iOS工程进行整合，解决CPU占用过大问题](https://www.jianshu.com/p/36f374f3e5e2)      

### 【问题17】 
**问题描述**：目前检测的平面都是水平的，没有垂直平面。也就是说，目前只能放置一些床，椅子，花盆等物体，对于门等垂直放置的家具不能放置。  
**解决办法**：ARKit1.5开始支持垂直平面检测，目前已经可以识别竖直平面了。已完成测量功能。  
尝试AR foundation的功能。  

### 【问题18】  
**问题描述**：有一个问题是unity中的，就是不同模型现有的prefab不是非常的统一。其初始状态都是不一样的，可能床是正面对着你，椅子就是背面对着你。我在设置里调整了其rotation参数，但是没有修改。  
造成结果：在屏幕上滑动手指进行更改位置的时候，由于模型的xyz方向不一样，向上/向下滑动的手势并不能造成统一的结果。也就是说，我向右滑动手指，由于其有旋转角度，模型不一样向右划。  
同样的问题存在于其他的基本变换中，大部分情况没有问题，对于一些奇怪的prefab会有缩放效果不对等问题。  
**解决办法**：这个问题的根本原因就是我不了解unity的一些基本使用....*更新：由于Prefab区分为子物体和父物体的区别，有时候修改了当前的模型但只是修改了再这个场景中的状态，而没有修改父物体的状态，再次使用的使用会造成修改无效的感觉。解决办法就是：新建一个空白的GameObject，将调整好的prefab拖进去生成新的prefab。*    
但是对于不同物体的平移与旋转角度不对情况还应继续研究。  

### 【问题19】  
**问题描述**：在将摄像头对准墙壁或其他比较干净整洁（这也是我的错吗？）的平面时，往往无法识别到特征点，不能正常工作。  
**解释**：
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/Problem19.png" width="50%" height="50%"/></div>   

这个事情可能不是我能解决的，只能尽量避开这种情况。  

### 【问题20】  
**问题描述**：在中期答辩中有提到的，关于放进来的模型位置不稳定。有的时候会跟随镜头抖动，最终飘向远方。但是有的时候又非常稳定。  
**解决办法**：只能控制变量来找出问题的原因，尽量避开这种情况。  

### 【问题21】   
**问题描述**：工程文件A的签名为A，工程文件B的签名为B。在将B导出的package放到A工程中合并的时候，会出现错误「apple mach -o linker(id) error」。  
**解决办法**：这个故事告诉我们，没事不要手欠随便改开发者名字。全程尽量使用一个名字，就算想改的规范一点，也要注意再合并之前将两个开发者签名改成一样的。导出包的时候如果多个过程的签名不一样的会出让人窒息的问题。  

### 【问题22】  
**问题描述**：新的AR Foundation出了一些考虑使用的功能，但是版本是4.0。只适合于XCode11+，但是XCode11+又只适合mac10.15+。官方文档所介绍的功能又确实值得尝试一下，所以准备多尝试一下。     
**解决办法**：不知道在座的各位有没有升级过mac系统，有什么建议或者操作。    

### 【问题23】    
**问题描述**：光照检测通过接口获得检测数值，需要支持TruthDepth相机的设备，iPad pro一代不支持。  
**解决办法**：这一部分其实也不是开发重点，只是作为一个验证的功能。所以暂时就这样了，测试一下看一下结果就好，不作为主要功能部分。将工程文件发给了其他同学，测试了光照估计的效果。效果正常，可以显示出来测试的参数。      

### 【问题24】   
**问题描述**：多个工程文件合并时，由于某个工程文件用了旧版的sdk，在Unity更新了版本之后，旧版sdk与unity新版导出iOS格式文件有所不同。  
错误显示为:Exception: Calling TargetGuidByName with name='Unity-iPhone' is deprecated.There are two targets now, call GetUnityMainTargetGuid() - for app or GetUnityFrameworkTargetGuid() - for source/plugins to get Guid instead of calling to TargetGuidByName(GetUnityTargetName()).    
**解决办法**：
[参考链接](https://stackoverflow.com/questions/60459020/how-to-fix-bug-in-ironsource-unity-sdk-on-ios)，对于本unityarkitplugin,将对应文件的第170与171行替换为
~~~
proj.AddFrameworkToProject(proj.GetUnityFrameworkTargetGuid(), "ARKit.framework", false);
string target = proj.GetUnityFrameworkTargetGuid();
~~~  


## 开发过程中可能会踩的坑  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/NameChanged.png" width="40%" height="40%"/></div>     

在正式版ARKit中，一些函数名称有修改，在后续若碰到这样的情况可以如此解决。   

~~~  
ARWorldTrackingSessionConfiguration->ARWorldTrackingConfiguration;  
ARSessionConfiguration->ARConfiguration;  
~~~    
