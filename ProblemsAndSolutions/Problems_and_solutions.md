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
<div align=center><img src=“https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/screenshot_arkitremote_test1.jpg “ width="50%" height="50%"/></div>     

以上这种远程的奇怪工程我不再试了，所以这些问题我也不准备解决了。解决本问题的方式是逃避问题。下方是在csdn博客上找到的其中一种解决办法，未尝试，供参考。  
<div align=center><img src=“https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/ProblemPictures/ARkitRemoteStuck.png“ width="50%" height="50%"/></div>     

### 【问题13】  
**问题描述**：ARSession中arsession.Raycast()函数丢失  
**解决办法**：参考：[unity中的提问Foundation AR, ARSessionOrigin doesn't reconize the Raycast method?](https://forum.unity.com/threads/foundation-ar-arsessionorigin-doesnt-reconize-the-raycast-method.680296/#post-5324931)以及
[在教程作者的github上的issue中的问题ARSessionOrigin has no member Raycast](https://github.com/TheUnityWorkbench/tuw-arfoundation-demo/issues/1)  
package manager中有提供ARKit，ARFoundation等包。注意不同版本下有细微的差别，比如ARKit 3.0版本就没有Raycast函数了，只能降级回1.0.0进行操作。当然，同样的功能可以使用新版本中其他的函数进行替换。   

### 【问题14】  
**问题描述**：.max文件只能用3dmax打开，而且我的MacBook pro不能安装3DMax  
**解决办法**：已经让别人把我的小dell邮寄过来了...    




## 开发过程中可能会踩的坑  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/NameChanged.png" width="40%" height="40%"/></div>     

在正式版ARKit中，一些函数名称有修改，在后续若碰到这样的情况可以如此解决。   

~~~  
ARWorldTrackingSessionConfiguration->ARWorldTrackingConfiguration;  
ARSessionConfiguration->ARConfiguration;  
~~~    


