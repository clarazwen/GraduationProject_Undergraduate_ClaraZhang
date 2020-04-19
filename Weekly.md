# 毕业设计完成记录  
本文档为Luwen Zhang的毕业设计完成记录  
> ### 任务书设定的预期进度安排  
> 1. 前期:  
>- 2020年1月初：确认毕业设计需完成的基本内容，查找相关文献与材料，完成开题工作；  
>- 1月-2月中：学习AR技术的原理以及熟悉Unity3D+Vuforia的开发方式，完成参考文献的阅读及翻译，学习家装设计类知识；  
> 2. 中期：  
>- 2月中-3月：完成家具三维模型库的建立，实现AR效果，使用简单的家具模型完成app功能上的实现；  
>- 3月：实现demo，完成基本功能；考虑造型的初步美观，app的基本交互设计；通过在开发过程中发现问题记录问题并及时与指导老师沟通，对预期功能进行修改与完善；准备中期答辩；  
> 3. 后期：  
>- 4月-5月：结合造型基础进行个性化的模型设计，改善装修效果以及风格的多样性。进入后期的软件完善阶段；  
>- 5月：改善app的用户体验，补充相关风格产品推荐等；同时完成毕业设计论文的撰写与格式的确认；拍摄演示视频及设计个人展板等。  


### week 1  0110  
&#8195;积极与导师沟通，确定毕业设计题目与初步开发内容。  
&#8195;完成前期调研任务，与导师见面，确定开发平台，阅读大量相关参考文献挑选合适文献；  
&#8195;撰写开题报告，确定任务书内容并联系导师签字，完成开题任务，沟通假期安排。

### week 2  0117  
&#8195;确定假期的毕设计划与进度：熟练unity的使用，通过阅读在前期调研过程中的参考文献，挑选合适的英文文献进行仔细阅读与翻译。  
&#8195;熟悉github上传文件，download代码，clone代码的方式，了解github引入图片，上传文档的方法。  
&#8195;练习使用markdown语言进行文档撰写，在「github」以「简书」上尝试使用markdown进行内容的记录。  

### week 3  0124    
&#8195;本周内阅读了一些在前期调研过程中找到的参考文献。对每一篇都进行仔细地阅读，了解论文中介绍的开发方法以及作者所使用的算法。记录对自己的毕业设计有指导意义的部分。    
&#8195;多个角度比对不同的文献，确定最为合适的外文翻译文献。    


### week 4  0131    
&#8195;着手学习如何使用Unity进行AR/VR开发，尝试了解Vuforia的工作原理以及基本操作。参考书籍及资料会在其他部分统一整理。  
&#8195;根据**技术难度，算法理解，文章长短，指导意义，与毕业设计内容的相关性**等多方面评价论文的参考价值，选定两篇文章进行翻译。  
&#8195;[AR interior designer- Automatic furniture arrangement using spatial and functional relationships.pdf](https://ieeexplore.ieee.org/abstract/document/7136652/)    
&#8195;[Markerless Augmented Reality based Interior Designing System](https://ieeexplore.ieee.org/abstract/document/8537349/)  

### week 5  0207  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/TranslationShowA.jpg" width="50%" height="50%"/></div>  

&#8195;初步完成AR interior designer论文的翻译工作。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/issueScreenshot.png" width="50%" height="50%"/></div>    

&#8195;论文中的部分「算法和专业名词解释」在[AR interior designer翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/Translation_ARInteriorDesigner_ReferenceWords.md) 中有详细解释。准备开始翻译另外一篇技术性不强，但在应用方面比较有参考价值的论文。   
&#8195;开学时间暂延后，毕设开发按照原定计划不变。  
 
### week 6  0214   
&#8195;完成了AR interior designer的论文翻译与词语整理，根据往年《毕业设计指导书》中「外文翻译」的参考格式对翻译文档的格式进行了调整，具体格式后期再进行订正与修改。   
&#8195;同样完成了Markerless Augmented Reality的论文翻译工作。  
&#8195;开始学习Unity+Vuforia+AR的开发。    
&#8195;准备下一篇论文翻译，学习unity+Vuforia+AR的初步开发。    
&#8195;调研了一些市场上已有的家具设计类app，下载安装后尝试使用此类app来找寻家居设计类的灵感。站在用户的角度，学习其用户界面与交互方式。   
### week 7  0221    
&#8195;整理了Markerless Augmented Reality陌生词汇，关键词汇与理论方法[Markerless Augmented Reality翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/Translation_Markerless_ReferenceWords.md)。    
&#8195;开始阅读借阅的关于unity+AR+Vuforia的参考书籍，着手进行开发学习。将调研过程以及查找资料过程中找到的unity+ar+vuforia的demo都测试了一下。  
&#8195;为保证开发硬件设备正常，将Android Studio连接到我自己的手机，打开USB调试并启用开发者模式。build并安装app，使用效果正常。  
- 教程中所介绍到的AR demo都是从扫描图片开始的，尝试使用ImageTarget进行测试。  
  * 在尝试第一个AR Demo过程中，很多教程中会提到安装初期即选择Vuforia进行安装，但是我的选项并没有这个模块[问题及解决1](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%981)。
  * 此外，「XR setting」以及vuforia 导入等内容，也与我的unity不符[问题及解决2](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%982)。  
- 学习过程中了解到Vuforia主要使用「识别」的方式来实现AR效果，然而本毕业设计并不涉及到图像识别[问题及解决3](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%983)  

### week 8 0228  
&#8195;整理周报内容，调整文档格式以及汇总参考链接。  
&#8195;使用Unity在手机上发布了第一个apk（简易AR Demo），并成功实现了扫描图像展示模型。  
&#8195;学习Vuforia关于识别图的星级评定的原理，关于后续识别图像的一系列修改（锐化，调整对比度等）。了解到了vuforia引擎的可以进行更改一些预设定，如user defined target building behaviour 包括「start scanning automat/stop scanning after creating a target」。   
&#8195;***补充思路:*** 在对市面上已有家装设计软件进行调研时提出想法「是否可以将360全景图展示模块加入其中」，参考「酷家」设计app。    
&#8195;~~接下来准备尝试模型交互或复杂模型的展示，思考解决Vuforia必须进行图像识别才能显示AR效果与本毕业设计无需图像识别的矛盾。[问题及解决3]~~   
&#8195;~~尝试智能地形+3D物体识别的内容，为后期开发做准备；学习关于AR内容交互的模块，包括脱卡功能，手势控制，虚拟按钮调用等，创建简单的demo进行尝试.~~    
### week 9 0306  
&#8195;在b站和youtube多看了一些相关视频，发现ARKit更加适合于本毕业设计对应内容。  
&#8195;将以下部分完成的内容提交到了GitHub上，[问题及解决4](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%984)记录了在使用Git进行提交时遇到的问题以及一些解决办法。  
&#8195;ARKit是iOS生态的开发平台，使用我自己的电脑以及平板进行了效果测试(MacBook Pro2018，Ipad Pro 9.7)。在尝试过程中遇到了许多问题，问题描述及解决方式见[问题及解决5](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%985)。  
- 使用ARKit完成了一些基本功能的实现   
  - 开发IDE为XCode，使用原生IOS开发方式，调用SceneKit实现了样例demo，进行飞机展示。  
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/plane_model.PNG" width="50%" height="50%"/></div>    

  - 使用SpriteKit，MetalKit中XCode的样例文件，实现了点击屏幕展示模型的功能。
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/cube_model.PNG" width="40%" height="40%"/></div>
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/emoji_model.PNG" width="40%" height="40%"/></div>  

  - 使用Ipad pro进行效果测试，对Arkit中世界跟踪，跟踪检测，位置坐标记录有了一定了解。  
  - 创建了single View app，从零开始实现了平面检测的代码[PlaneDetection](https://github.com/clarazwen/PlaneDetection_Demo1)，效果图及控制台输出数据如下。    
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/PlaneDetect_table.PNG" width="40%" height="40%"/></div>
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/PlaneDetect_table2.PNG" width="40%" height="40%"/></div>  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/PlaneDemo_1_Console_data.png" width="50%" height="50%"/></div>  

  - 在完成平面检测代码的过程中发现缺失PlaneNode这一个类的内容，对于该情况请见[问题及解决6](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%986)。目前使用了网络上其他教程的方法，也完成了这一部分功能的实现，运行起来暂无问题，控制台输出状态及数据也是正常合理的。  
- 当前计划    
  - ~~学习如何导入模型，所需格式及如何创建贴图；~~  
  - ~~解决PlaneNode问题；~~  
  - ~~对比Objective-C与Swift语言的优缺点，在ARKit方面上的适用性；以及OC语言在IOS AR开发上版本上的要求对后续开发是否存在影响。~~ 
 
### week 10   0313
#### 0307  
&#8195;对于[问题及解决6](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%986)中的情况，在阅读了接下来的教程中的内容，我认为应该仅是类文件缺失的原因，不涉及的ARKit的版本问题。同样，我在网上查找了类似功能的代码文件，实现方法大同小异，且同样可以运行他人的工程文件。   
&#8195;对于关于ARKit开发中的环境设置以及硬件要求，我的都是满足条件的，记录如下：  
~~~
Macbook Pro(2018)、XCode(Version 9.4.1)；  
iPad Pro(9.7 inch)，iOS 13.3;
Unity:2019.2.21f1与2017.4.36c1  
~~~    
&#8195;此外，关于Objective-C语言与Swift语言的选择问题。对于iOS/Mac的开发，目前主流都为swift语言，Xcode官网的更新都是只有swift的介绍，学习的话当然也是以它为主。其实在之前的开发过程中，部分教程中使用OC语言进行入门的介绍，因此我也按照一些参考资料来使用OC语言进行尝试。但是后期的开发不是只在iOS原生开发平台上进行的，开发平台仍然是Unity。   
&#8195;Unity支持ARkit，并且苹果最新发布的ARKit3.0的主要功能在ARFoudation已经集成进来了（尽管新功能都是动作捕捉，面部追踪等我用不到的）。  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/ARFoundation-ARCore-ARKit.jpg" width="50%" height="50%"/></div>    

&#8195;所以接下来在XCode上进行iOS的原生开发学习过程，会根据可以找到的教程来决定使用语言，而实际的开发过程会在Unity中进行。    
&#8195;新的功能实现：  
- 实现了简单的ui，点击【开启AR】才能开启摄像头进入界面。点击屏幕展示家具模型，模型大小随摄像头点击位置的远近有变化。至少加载了一个家具模型，和毕业设计中的家居设计有了关系....    

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/showChair.png" width="40%" height="40%"/></div>      

- 实现了点击模型进行模型材质的更换，具体为更换模型的纹理贴图等外部表现。   
这一部分与预期计划的调整模型外观，如材质，颜色等相匹配。接下来需要尝试更换为实际开发所用的家具模型再进行对应功能的实现。     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/tap_changeTexture_1/tap_changeTexture_7.png" width="40%" height="40%"/></div>     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/tap_changeTexture_1/tap_changeTexture.gif" width="40%" height="40%"/></div>     

- 尝试了AR测量，运行了现有demo实现了使用ARRuler在现实世界中进行测距，这个功能与iPhone/iPad中的测距仪应用起来的方式是一样的。  
这一部分与预期计划中的判断家具尺寸是否符合当前房屋尺寸的功能比较匹配。目前也只是一个别人的单个功能的小demo，接下来仔细了解一下其实现方式，重新进行功能开发。  

### 0308  
&#8195;在不同的教程中找到了不同的实现平面检测的办法，在更改源代码中planeNode内容时，发现了另外一种效果更优的实现方式，目前已整合到自己的代码中。前后两类识别效果对比如下：  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/PlaneDetect_bed.PNG" width="35%" height="35%"/></div>   <div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/PlaneDetect_method2_img1.png" width="35%" height="35%"/></div>     
&#8195;对比可以看出，新方法对于识别的效果要更好。生成的平面状态要更加的稳定，识别范围更广，可以补充到平面更多的边缘。    

接下来的计划：
- ~~[问题与解决9](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%989)学习unity与iOS原生代码之间的交互。~~  
- ~~尝试实现模型尺寸的调整等。~~  
- ~~了解具体所需模型的格式，使用【非官方测试模型/非他人代码所提供的模型】进行展示。~~  
- 一些功能其实还和预期效果有很大差别。比如现在放置椅子模型这个，它没有对场景中其他物体进行检测，也就是说，它就算一只脚在床上一只脚在地上也不会出现问题....顶多是模型覆盖上去了，应该会有物体检测和碰撞检测的方法吧。  

#### 0313  成功使用unity再次完成了之前的功能，并进行了一些补充。  
- 学习了ARKit在Unity中的使用，首先在unity中加载相关的package； 
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/TestPictures_Tutorial/ARpackageImport.png" width="50%" height="50%"/></div>     

- 第一个样例工程是ARKit Remote：是使用远程的方式将iPad扫描到的影像在unity的Game中进行展示，同时实现点击显示模型的效果。
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/ARKitRemoteShot1.png" width="50%" height="50%"/></div>     

套娃式展示，电脑端截屏。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/ARKitRemoteShot2.png" width="50%" height="50%"/></div>     

iPad端的截屏。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/UnityARKitFirstTest1.png" width="50%" height="50%"/></div>     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/UnityARKitFirstTest2.png" width="50%" height="50%"/></div>     

（但这个例子其实一点用也没有....见[问题12](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9812)）


- 参考 [Getting Started With ARFoundation in Unity (ARKit, ARCore)](https://www.youtube.com/watch?v=Ml2UakwRxjk&feature=youtu.be) ，非常系统地实现了一些基础功能。
  - 首先进行初始的参数设定修改。 

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/InitParameter.png" width="50%" height="50%"/></div>  

  - 对「点击屏幕放置模型」的视觉效果做改善。 
调用ARsession和AR session origin，将ARCamera作为主摄像机。使用Raycast函数进行射线检测，从而确定模型的目标放置位置。  
  
  - 使用Quad并增添贴图的方式丰富了候选位置的展示图片。
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/IndexQuad.png" width="50%" height="50%"/></div> 

  - 导入了小飞机的模型，并且通过调整quality中shadow distance的具体参数，改善了其阴影效果以及提高模型细节展示。以下是飞机排队的展示（bushi。
    
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/ToyPlanePlacement1.png" width="50%" height="50%"/></div>      

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UnityARKitFirst/ToyPlanePlacement2.png" width="50%" height="50%"/></div>   

- 实现了对放置到场景中的模型的一些简单操作，如模型的平移，旋转，缩放。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/GestureMove/BedPlacementMiddle.png" width="50%" height="50%"/></div>   

  - **放大模型的一种比较好的方式是缩小场景的尺寸。** 如果直接调整模型的scale，有的时候过分缩放会改变物体的客观物理现象。在这里，我们选择调整AR session origin的scale进行反向缩放。比如要将模型缩小为1/10，只要将AR session origin的scale调整为10即可。毕竟AR是将真实世界和虚拟世界结合在一起的技术，有的尺寸不能仅满足于虚拟世界，而要和现实世界的物体进行一个对比。以下是捏挤屏幕进行缩放的效果图。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/GestureMove/BedPlacementBig.png" width="50%" height="50%"/></div>     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/GestureMove/BedPlacementSmall.png" width="50%" height="50%"/></div>     

#### 对上次内容的解释
- 关于.scn的格式问题。在iOS开发中，因为Scenekit和Xcode是可以进行三维建模的，经了解.scn是SceneKit对应的场景文件的文件后缀，独立存在于xcode平台。对其他格式的文件，可以使用.dae格式进行中转，再在xcode中转换为.scn文件。其实还是挺麻烦的...  
- 在使用unity中的ARKit插件，以及AR Foundation插件后，模型的格式不再是一个棘手的问题。在Assets store中就可以下载到较多完成的家具模型。[问题14](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9814)

#### 注意  
- 为了避开点击屏幕放置模型与缩放手势的冲突，设定了三只手指同时点击屏幕才能进行模型的摆放；一只手指滑动进行模型的平移，两只手指的挤捏实现模型的旋转和缩放；  

#### 任务安排
- 曾在iOS开发中实现的点击切换材质/颜色尚未实现，这一部分没有类似的教程，只能自己摸索一下。  

- 接下来的学习会多学习unity的开发。目前的开发都比较散，属于独立功能与独立功能的开发。接下来要想出一个整体的逻辑架构，不能总是散装着来....   
因为unity可以和iOS进行交互，也就是说可以在一个iOS工程中加入AR的工程。所以，我准备使用iOS进行app界面设计与不涉及到AR功能的界面的开发，再在unity中进行AR功能的开发将其整合进入总的iOS工程中。毕竟unity中build iOS端的应用的方式也是先生成.xcodeproj文件，再在xcode中将应用发布到iPad上。也就是，总体的框架与AR无关的放在iOS端，一些与AR相关的功能放在unity中实现。  
- 目前对家具放置等情况，它其实没有摆放到实际的地面上，就是很虚伪。然而宜家的AR视频中就非常非常的真实，这部分需要仔细思索一下....  
- 对于模型尺寸等问题，进行缩放之后需要和AR Ruler联系起来。毕竟毕业设计中对模型进行缩放的初衷是为了「找到适合自己房间的家具的合适尺寸」。因此我们需要提供调整之后对应真实世界的尺寸，这一部分使用AR Ruler比较合适。  

### week 12 0320  
#### 增加功能：  
- 完善了一些功能，*模型的拖动调整位置* ，对于已经放入场景中但觉得效果不好的模型-> *双击即可删除模型* ；  
- 选择是否开启平面检测，如果开启该功能并且检测到了平面即显示指示图标；

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo1.png"  width="50%" height="50%"/></div>     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo2.png"  width="50%" height="50%"/></div>    

- 选择对应的toggle，放置对应的模型，并且可以任意对其进行变换（目前只用了toggle和button来实现，之后再进行美化...）；   
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo3.png"  width="50%" height="50%"/></div>   

- 双击模型删除模型；  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo4.png"  width="50%" height="50%"/></div>    

- 更改了对应的toggle之后，可以放置不同的模型（飞机），同样进行基本变换；
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo5.png"  width="50%" height="50%"/></div>    

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo6.png"  width="50%" height="50%"/></div>   

- 放置不同风格的床，变换，删除；  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo7.png"  width="50%" height="50%"/></div>   

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo_1.gif"  width="50%" height="50%"/></div>   

- 使用unity的ui完成了*模型选择*功能的完成。选中不同的模型即可在屏幕上放置不同的模型(这是gif图，但是它总不动...)； 
 
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/PlaceAndChangeDemo/PlaceAndChangeDemo_2.gif"  width="50%" height="50%"/></div>   

- 尝试了AR Paint功能，本意是直接在空间中进行绘制示意图，起到标记等功能。搜集了一些现有的演示gif，感觉效果比较一般。要么能绘制但是识别效果很差很不稳定，要么只能在当前视窗绘制，没有位置记录的功能。这个功能待考虑和尝试。（图）    
- 实现了AR Measure，用了ARKit本身插件中的unity AR generate Plane脚本生成平面。可以测量当前场景的两点间的距离或三点平面的面积。误差比较小，基本控制在1cm之内。可完善。   
  - 首先调用插件中的AR generate plane生成可检测距离的平面，在测量点上点击「mark」放置标记。放置两个标记即可显示当前两点的「实际距离」，结果比较准，控制在1cm的误差之内(这俩也是gif图，但是它有时候就不动...)；  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/ARMeasure/ARMeasure_01.gif"  width="50%" height="50%"/></div>     

- 再继续放置一个marker，即可测量三点间的面积。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/ARMeasure/ARMeasure_02.gif"  width="50%" height="50%"/></div>   

- 实现了不同场景之间的切换，功能也同样可以使用。   

#### 存在问题：  
- 将unity和iOS工程的整合比我想的要难许多....我以为就修改些参数改一下入口就行了。现在使用unity的ui在进行开发，先完成功能，再不断尝试二者的整合。  
- 整体性不强，ui急需完善。参考iOS端自带的AR工具，如测距仪。

#### 任务安排：  

- 增加场景保存的功能：对于放入场景的家具模型，经调整完成后保存其位置和其他基本设置。可以接着进行其他模型的操作，而不会影响前一个模型的状态。  
- 手指拖动模型更改位置的优化，不能总靠揣摩着来...  
- 位置测量的完善，将当前的测量两点间距离的功能进行后续的开发，完成一些不规则平面墙壁边缘的距离闭环标记以及加和，同时可以简单估算场景内的实际面积。预期效果如下：  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/BasicFunction/ARMeasure/HouseAR2.png"  width="50%" height="50%"/></div>   

- 对于更换模型，目前使用的只是文字的指示，准备加入模型缩略图展示再进行选中的功能，同时加入模型材质或颜色的更换。  
- iOS的UI设计也要一直跟着。  
- 一个问题：中期检查都要准备啥....（（（（（（

### week 13 0327  

这周好多时间放在整合，调整UI，写检查表做ppt上面了，周报记录的比较简单。  
- 了解了一下prefab的存在子物体与父物体等....更改好了满足状态的prefab后再创建新的prefab。解决了模型初始设置角度不同，导致的更改prefab参数不起作用，旋转方向不一致的问题；  
- 更换ARKit版本为1.5，补充了垂直平面检测的功能。在测量中进行测试，效果良好，误差仍然在1cm内。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/IntermediateInspection/Pictures/ARVertical.gif" width="50%" height="50%"/></div>     

- AR测量加入了多边形面积的测量；  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/IntermediateInspection/Pictures/ARArea.gif" width="50%" height="50%"/></div>      

- 加入了新的家具模型，设计了简单的UI，使用Toggle做了不同家具间的切换；  
   
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/IntermediateInspection/Pictures/model2.gif" width="50%" height="50%"/></div>     

- 准备中期答辩，提交中期检查表，指导记录，准备了答辩ppt以及录制了简单的演示视频；  
- 调整了应用名称，加载了应用的icon。  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/IntermediateInspection/Pictures/icon.png" width="50%" height="50%"/></div>     

#### 下周计划：
- 既然已经完成了垂直平面的检测，尝试放置竖直方向的物体，比如装饰画等。  
- 增加大量的家具模型，提高可供选择的模型数量；   
- 开始尝试样板间的AR展示；   
- 查缺补漏，将之前曾经规划过的功能整理一下，尽量实现出来。   

### week14 0403   
> 1．多点连续测量：目前的距离测量只有单次两点间的距离，不能记录上一次的测量结果。接下来进行多个标记间的连续两点距离的测量与保存。完成闭环式的轮廓，以形成家居设计图中的户型尺寸草图。   
> 2．已放置在场景中的模型，其尺寸没有和真实世界的家具尺寸形成参照。形成一套虚拟模型与真实家具的度量体系，为操作者提供真实数据的参考。   
> 3．补充家具模型。使用同种风格的家具，完成一套或多套家居设计样板间的AR展示。提供关键词内家具推荐，完成预期的“猜你喜欢”功能。   
> 4．完成保存已设计场景的功能，放置在场景中的模型是位置固定的，移动摄像头观察其整体摆放效果。   
> 5．改善用户界面，便于初试者上手，提高其美观度以及交互性。   
> 6．调研及开发过程使用的参考资料，遇到的问题及解决办法都有记录。根据以上记录，结合软件效果，研究基本原理，完成毕业设计论文.完成全部的功能开发与效果完善后，录制毕设的演示视频，设计个人展板。    

- 完成中期答辩，根据答辩老师意见调整了中期检查表。  
- 对接下来需要完成的任务做了简单调整，暂定了功能模块；

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/%E6%A8%A1%E5%9D%97%E4%BB%8B%E7%BB%8D.png" width="70%" height="70%"/></div>       

- 根据预期的模块内容，进行新功能的开发尝试。  
- 有很多小细节的修改，改一发而动全身，正在调整。  
- 阅读了几篇毕业论文，拟定论文大纲。  
- 为了开发新的功能，在网上查找了相关资料，有一些参考demo需要XCode11。还有一些需要解决的问题，还没有成功构建 [问题22](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9822)   

### week15 0411  
完成任务  
- 感谢教授，电脑系统和XCode都更新成功了，没有问题。   
- 运行了新的samples，效果正常，可以显示主要轮廓。接下来马不停蹄进行新的开发和整合。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/XCodeUpgrate.png" width="50%" height="50%"/></div>    

- 关于iOS和Unity跳转交互的整合。    
> Unity改变了生成的iOS Xcode和Android Gradle项目的架构。    
  - unity更新了版本之后（2019.3.4），生成的Xcode文件结构简洁了许多，和之前相比有变化。   
  - 已经实现了官方demo的跳转，参考[Unity 2019.3为原生游戏应用简化插入AR功能过程](https://yivian.com/news/62508.html) ，看起来为AR的开发提供了许多方便。   
- 根据中期意见，需要补充光照估计数值的参考。然而获得数值需要支持TruthDepth相机的设备，我的暂时不支持。将文件打包给了其他同学，成功测试了光照估计的效果，可以显示参数。见[问题23](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9823)    
- 毕业论文    
参考了往年的论文，初步拟定了论文内容，调整了一下格式。对于不确定需要指导的意见已经高亮显示了，准备发送给指导教师。

工作安排    
- 马不停蹄抓紧完成应用开发。
- 将光照检测等新尝试好的功能，补充进原有的应用中。拍摄新的测试图片。  
- 已经初步实现iOS与unity的交互，尽快尝试将自己的功能按照这种结构进行操作，然后快些尝试新的功能（AR Foundation3.0与ARKit3.0）  
- 根据指导意见，以及自己难以捉摸的想法，有逻辑地更改论文大纲。  
- 完成已确定部分的毕业论文。

### week16 0418  
完成任务：  
- 主要在完成论文（写论文为何上瘾），开启日常产出论文之后。毕设和论文一起弄了。 
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/LightEstimateMerge.png" width="50%" height="50%"/></div>     

- 重新测试了之前由于设备不支持的光照估计的功能，将其插到了主工程文件中。    
- 搜集了XR interaction的一些便捷交互动作，重新建了个小的工程文件进行开发与测试，正在和自己的主要工程进行整合。     
- 正在一步一步解决之前存在的小问题，根据记录内容进行调整，还有多个功能项目的合并。  
- 关于之前那个合并之后版本问题，隔了几天我再打开...我还没开始解决呢，它自己就好了....考虑到有问题的时候是曾经出现过的问题，感觉是build过程中哪个设置出了问题。其实没有不兼容的情况。  
- 关于论文的问题：对于有的部分，不可避免的会用到网上的资料，尤其是背景和技术原理这一类的，那这些都一定要用自己的话再说一遍吗？  
毕业论文：  
 - 调整了毕业论文的大纲，开始完成已确定部分的论文内容，已完成第一章与第二章大部分的论文初稿（进度15%）。     
 - 建立了新的文件，用来保存完成论文时用到的资料。   
工作安排：  
- 继续完成论文，根据之前的开发记录，撰写内容，不断调整。    
- 清醒一点，加速完成还没写完的代码开发，调整一下界面美观。    

暂时想到这里，待更新。
