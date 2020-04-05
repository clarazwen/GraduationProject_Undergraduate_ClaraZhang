## 毕业设计相关记录
本仓库为clarazhang的毕业设计记录。  
- **周报内容**  请查看详细周报记录：[进度汇报](https://github.com/clarazwen/ProgressReport/blob/master/Weekly.md)  
- **参考资料**  请查看整个毕设的完成过程所用到的全部参考资料：[参考资料](https://github.com/clarazwen/ProgressReport/blob/master/References/References.md)  
- **问题与解决** 请查看遇到的问题与解决方式的详细记录：[问题与解决](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md)
### 毕业设计题目
《Implementation of personalized home decoration platform based on augmented reality》  
基于增强现实的个性化家装平台  
### 文献翻译  
考虑到本毕业设计的开发内容与研究方向，选取了两篇论文进行研读与翻译。  
- [AR interior designer- Automatic furniture arrangement using spatial and functional relationships](https://ieeexplore.ieee.org/abstract/document/7136652/)  
- [Markerless Augmented Reality based Interior Designing System](https://ieeexplore.ieee.org/abstract/document/8537349/)  

部分重点词汇及模糊词汇语句记录见  
- [AR interior designer翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/Translation_ARInteriorDesigner_ReferenceWords.md)
- [Markerless Augmented Reality翻译记录](https://github.com/clarazwen/ProgressReport/blob/master/LiteratureTranslation/Translation_Markerless_ReferenceWords.md)
### 测试效果展示图片  
为将测试效果的图片集中于一部分展示，在本仓库中建立了一个单独的文件夹进行[效果展示](https://github.com/clarazwen/ProgressReport/tree/master/Pictures/TestPictures_Tutorial)  

### 参考资料  
自毕业设计开始，调研与产品分析，GitHub使用教程，markdown语言学习，iOS开发指南，ARKit入门等教程均记录在此。包括[参考链接](https://github.com/clarazwen/ProgressReport/blob/master/References/References.md#%E5%8F%82%E8%80%83%E9%93%BE%E6%8E%A5%E9%83%A8%E5%88%86)，[参考文献](https://github.com/clarazwen/ProgressReport/blob/master/References/References.md#%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE)，[参考书籍](https://github.com/clarazwen/ProgressReport/blob/master/References/References.md#%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE)。

### 问题与解决  
- 已解决  
  - [问题1](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%981):在尝试第一个AR Demo过程中，很多教程中会提到安装初期即选择Vuforia进行安装，但是实际安装时并没有这个模块（Mac Unity 2019.2.21f1）；    
  - [问题2](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%982):网上或是参考书中的内容在进行Vuforia完成第一个AR demo时都有提及到关于「XR setting」的修改，在实际操作中未找到相关设置；   
  - [问题3](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%983)  :学习过程中了解到Vuforia主要使用各种「识别」的方式来实现AR效果，然而本毕业设计并不涉及到图像识别；   
  - [问题4](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%984):使用git命令提交文件时出错； 
  - [问题5](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%985):XCode在使用真机（ipad）调试时出现部分问题；
  - [问题6](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%986):缺失PlaneNode类的内容；  
  - [问题9](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%989):Unity与iOS原生代码交互，在unity中实现在xcode上已实现的AR效果。
  - [问题10](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9810):解决模型文件格式问题。
  - [问题11](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9811):Unity-ARKit-Plugin在asset store中不再支持  
  - [问题12](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9812):测试样例ARKitRemote运行起来非常的卡顿，界面刷新非常慢。  
  - [问题13](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9813):ARSession中arsession.Raycast()函数丢失   
  - [问题14](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9814):.max文件只能用3dmax打开，而macOS无法下载3Dmax   
  - [问题15](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9815):苹果免费的开发app ID一周只有10个，超过10个使用之前用过的id即可。   
  - [问题19](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9819):这个我不打算解决并且我也解决不了...在将摄像头对准墙壁或其他比较干净整洁的平面时，往往无法识别到特征点.
  - [问题17](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9817)已解决，可以检测垂直平面    
- [问题18](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9818)由于模型的预设不一致，方向角度不一样，导致相同的触屏手势会造成不同的位移。  
  - [问题21](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9821):iOS开发问题「apple mach -o linker(id) error」


- 未解决  
  - [问题16](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9816):iOS与unity代码间的交互   
  - [问题20](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9820):放进来的模型位置不稳定  
  - [问题22](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9822):macOS系统升级的问题。  



其余待更新。  
