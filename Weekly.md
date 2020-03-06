# 毕业设计完成记录
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

初步完成AR interior designer论文的翻译工作。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/issueScreenshot.png" width="50%" height="50%"/></div>    

论文中的部分「算法和专业名词解释」在[AR interior designer翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/Translation_ARInteriorDesigner_ReferenceWords.md) 中有详细解释。准备开始翻译另外一篇技术性不强，但在应用方面比较有参考价值的论文。   
开学时间暂延后，毕设开发按照原定计划不变。  
 
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
  * 在尝试第一个AR Demo过程中，很多教程中会提到安装初期即选择Vuforia进行安装，但是我的选项并没有这个模块[问题1]。
  * 此外，「XR setting」以及vuforia 导入等内容，也与我的unity不符[问题2]（mac很多的操作都不需要手动去做）。  
- 学习过程中了解到Vuforia主要使用「识别」的方式来实现AR效果，然而本毕业设计并不涉及到图像识别[问题3]（在学习过程中逐渐深入学习Vuforia，寻求最佳方案。）。      

### week 8 0228  
&#8195;整理周报内容，调整文档格式以及汇总参考链接。  
&#8195;使用Unity在手机上发布了第一个apk（简易AR Demo），并成功实现了扫描图像展示模型。  
&#8195;学习Vuforia关于识别图的星级评定的原理，关于后续识别图像的一系列修改（锐化，调整对比度等）。了解到了vuforia引擎的可以进行更改一些预设定，如user defined target building behaviour 包括「start scanning automat/stop scanning after creating a target」。   
&#8195;***补充思路:*** 在对市面上已有家装设计软件进行调研时提出想法「是否可以将360全景图展示模块加入其中」，参考「酷家」设计app。    
&#8195;~~接下来准备尝试模型交互或复杂模型的展示，思考解决Vuforia必须进行图像识别才能显示AR效果与本毕业设计无需图像识别的矛盾。[问题3]~~      
&#8195;~~尝试智能地形+3D物体识别的内容，为后期开发做准备；学习关于AR内容交互的模块，包括脱卡功能，手势控制，虚拟按钮调用等，创建简单的demo进行尝试.~~    
### week 9 0306  
&#8195;在b站和youtube多看了一些相关视频，发现ARKit更加适合于本毕业设计对应内容。  
&#8195;将以下部分完成的内容提交到了GitHub上，[问题4]记录了在使用Git进行提交时遇到的问题以及一些解决办法。  
&#8195;ARKit是iOS生态的开发平台，使用我自己的电脑以及平板进行了效果测试(MacBook Pro2018，Ipad Pro 9.7)。在尝试过程中遇到了许多问题，问题描述及解决方式见[问题5]。  
- 使用ARKit完成了一些基本功能的实现   
  - 开发IDE为XCode，使用原生IOS开发方式，调用SceneKit实现了样例demo，进行飞机展示。  
  
<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/plane_model.PNG" width="50%" height="50%"/></div>    

  - 使用SpriteKit，MetalKit中XCode的样例文件，实现了点击屏幕展示模型的功能。
  
<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/cube_model.PNG" width="40%" height="40%"/></div>
<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/emoji_model.PNG" width="40%" height="40%"/></div>  

  - 使用Ipad pro进行效果测试，对Arkit中世界跟踪，跟踪检测，位置坐标记录有了一定了解。  
  - 创建了single View app，从零开始实现了平面检测的代码[PlaneDetection](https://github.com/clarazwen/PlaneDetection_Demo1)，效果图及控制台输出数据如下。    
  
<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/PlaneDetect_table.PNG" width="40%" height="40%"/></div>
<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/PlaneDetect_table2.PNG" width="40%" height="40%"/></div>  

<div align=center><img src="https://github.com/clarazwen/showPicture/blob/master/PlaneDemo_1_Console_data.png" width="50%" height="50%"/></div>  

  - 在完成平面检测代码的过程中发现缺失PlaneNode这一个类的内容，尚未找到对应文件[问题5]。目前使用了网络上其他教程的方法，也完成了这一部分功能的实现，运行起来暂无问题，控制台输出状态及数据也是正常合理的。  
- 当前计划    
  - 学习如何导入模型，所需格式及如何创建贴图；  
  - 解决PlaneNode问题；  
  - 对比Objective-C与Swift语言的优缺点，在ARKit方面上的适用性；以及OC语言在IOS AR开发上版本上的要求对后续开发是否存在影响。  
