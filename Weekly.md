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


## week 4  0131    
&#8195;着手学习如何使用Unity进行AR/VR开发，尝试了解Vuforia的工作原理以及基本操作。参考书籍及资料会在其他部分统一整理。  
&#8195;根据***技术难度，算法理解，文章长短，指导意义，与毕业设计内容的相关性***等多方面评价论文的参考价值，选定两篇文章进行翻译。  
&#8195;[AR interior designer- Automatic furniture arrangement using spatial and functional relationships.pdf](https://ieeexplore.ieee.org/abstract/document/7136652/)    
&#8195;[Markerless Augmented Reality based Interior Designing System](https://ieeexplore.ieee.org/abstract/document/8537349/)  

## week 5  0207  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/TranslationShowA.jpg" width="50%" height="50%"/></div>  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/issueScreenshot.png" width="50%" height="50%"/></div>    

初步完成AR interior designer论文的翻译工作。  
论文中的部分「算法和专业名词解释」在[AR interior designer翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/Translation_ARInteriorDesigner_ReferenceWords.md) 中有详细解释。准备开始翻译另外一篇技术性不强，但在应用方面比较有参考价值的论文。   
开学时间暂延后，毕设开发按照原定计划不变。  
 
### week 6  0214   
&#8195;完成了AR interior designer的论文翻译与词语整理，根据往年《毕业设计指导书》中「外文翻译」的参考格式对翻译文档的格式进行了调整，具体格式后期再进行订正与修改。   
&#8195;同样完成了Markerless Augmented Reality的论文翻译工作。  
&#8195;开始学习Unity+Vuforia+AR的开发。    
&#8195;准备下一篇论文翻译，学习unity+Vuforia+AR的初步开发。    
&#8195;调研了一些市场上已有的家具设计类app，下载安装后尝试使用此类app来找寻家居设计类的灵感。站在用户的角度，学习其用户界面与交互方式。   
### week 7  0221    
&#8195;整理了Markerless Augmented Reality陌生词汇，关键词汇与理论方法[Markerless Augmented Reality翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/Translation_Markerless_ReferenceWords.md)。    
&#8195;开始阅读借阅的关于unity+AR+Vuforia的参考书籍，着手进行开发学习。    
&#8195;将调研过程以及查找资料过程中找到的unity+ar+vuforia的demo都测试了一下，连接到我自己的手机，打开USB调试并启用开发者模式。build并安装app，使用效果正常。  
- 教程中所介绍到的AR demo都是从扫描图片开始的，尝试使用ImageTarget进行测试。  
  * 在尝试第一个AR Demo过程中，很多教程中会提到安装初期即选择Vuforia进行安装，但是我的选项并没有这个模块[问题1]。此外，「XR setting」以及vuforia 导入等内容，也与我的unity不符[问题2]（mac很多的操作都不需要手动去做）。  
- 学习过程中了解到Vuforia主要使用「识别」的方式来实现AR效果，然而本毕业设计并不设计到图像识别[问题3]（在学习过程中逐渐深入学习Vuforia，寻求最佳方案。）。      

## week 8 0228（尚未更改）
### 0222 
入门就有点头秃，今天也很不快乐。  
太感人了，折腾了一个晚上unity发布apk，我终于在我的手机上安装了第一个unity app！  
### 0223
用自己的手机实现了扫描图片（我的头像），出来一个立体模型的效果。  
接下来试试交互，以及其他像样点模型的导入。我发现有些东西需要自己找解决办法，比如说现在学习到的这些方式都只能识别一个图，那我想摆很多家具怎么办。  
仍有无数的底层人民还在为毕业设计而奋斗。 
### 0224  
今天开学了  
vuforia对于识别图的星级评定的一些原理可以学习一下。    
包括本AR引擎的一些预置设定，比如user defined target building behaviour 包括{start scanning automat/stop scanning after creating a target}。
又了解到了智能地形+3D物体识别的内容，近期都要尝试一下。把类似的东西都学习一下，方便后续的自己的开发。  
了解了一些AR内容交互模块，准备学习一下脱卡功能，手势控制，虚拟按钮调用等功能。  
参考书中有提到一些比较完整的AR案例，下载示例工程进行测试，比如踢足球的小游戏。  
另外感觉很多这种类型的软件，都会有类似渲染后的结果的展示，360全景图知道是否可以加入其中，参考「酷家」设计app。  
### 0225  
整理了一下前面的一些闲言碎语的记录，之后需要提交周报的时候再好好整理有用的记录吧。  
尝试模型交互。
### 0226  
在b站看了一些教程，多尝试了些功能。
### 0227  
在b站和youtube看了许多相关的视频之后，我发现可能ARKit更适合于我的app....（vuforia更适合于识图展示模型，ARKit是凭空展示模型和测距什么的，更适合于这种家居测量与模型演示）于是今天我都在尝试使用mac+ipad pro的方式运行AR程序，修改了各种乱七八糟的设置。实现了ARkit（SceneKit）的样例demo，展示了一个小飞机。尝试代码包已经上传。  
继续尝试vuforia和ARKit的其他功能，包括在unity如何调用等。  
呜呜呜呜呜呜，加油啊！一点一点来吧。
### 0228  
使用SpriteKit以及MetalKit中XCode的样例文件，完成了点击屏幕展示模型的功能尝试。  
按照参考书编写了部分代码，使用ipad进行了世界跟踪，跟踪监测，位置坐标等功能的尝试。  
还了解了一些ARkit中的AR类的原理及基本代码。  
接下来尝试如何进行自己模型的导入，了解导入模型需要的格式以及贴图的方式。  
包括ARkit怎么在unity中调用。
### 0229  
感人，经过了乱七八糟的不屑努力，尝试了各种解决办法之后，终于在github上使用git上传了第一个代码包！是今天尝试世界跟踪的代码。（反正是成功更新了一次！  
继续学习场景理解，平面检测等部分。  
### 0301  
完成了几次开发中运行界面图片的保存，控制台输出状态的记录。  
使用ARKit原生开发，在Xcode中完成了平面检测代码的尝试。  
但是按照参考教材中的内容好像缺少了一个PlaneNode.m及PlaneNode.h的文件，在网上查找到了其他的实现方式，与原来的思路不一致。暂时运行起来没有问题，控制台台输出状态以及数据也是正常合理的。接下来继续研究PlaneNode类的具体内容到底是啥，尝试HitTest，完成平面检测后对距离的估计。  
目前识别出来的平面不是非常的全，和现有的AR软件来识别平面的效果还是不能比。  
继续学习并且进行改进。
