## 写在前面。   
    我本科为bupt的数技专业，现已毕业，本文档为本科毕业设计的整体开发过程的各种记录。   
    主要是使用ARKit进行家装设计软件的开发，最终实现了一个iOS端的APP。开发过程尝试了很多办法，踩了很多的坑。  
    如果看到这篇文档的人对类似的软件开发或是增强现实应用开发过程中有什么问题也可以一起探讨一下XD   
    这个毕业设计最终成绩为优秀（90.5/100），参与了优秀毕设答辩，算是给本科画上了一个完美的句号吧～     
## 毕业设计相关记录   
- **周报内容**  请查看详细周报记录：[进度汇报](https://github.com/clarazwen/ProgressReport/blob/master/Weekly.md)   
- **第二阶段周报内容**  请查看详细周报记录：[第二阶段进度汇报](https://github.com/clarazwen/ProgressReport/blob/master/Weekly2.0.md)   
- **参考资料**  请查看整个毕设的完成过程所用到的全部参考资料：[参考资料](https://github.com/clarazwen/ProgressReport/blob/master/References/References.md)  
- **论文参考资料**  请查看整个毕业论文的完成过程所用到的参考资料：[论文参考资料](https://github.com/clarazwen/ProgressReport/blob/master/References/GraduationStudyReferences.md)  
- **问题与解决** 请查看遇到的问题与解决方式的详细记录：[问题与解决](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md)    
### 毕业设计题目
《Implementation of personalized home decoration platform based on augmented reality》  
基于增强现实的个性化家装平台    

#### 对于访问GitHub速度过慢/图片加载过慢的解决办法：
为了提高速度，可以使用HOSTS加速对Github网站加载的资源网站域名解析。   
~~~  
需添加代码
# GitHub   
192.30.253.112 github.com 
192.30.253.119 gist.github.com 
151.101.100.133 assets-cdn.github.com 
151.101.100.133 raw.githubusercontent.com 
151.101.100.133 gist.githubusercontent.com 
151.101.100.133 cloud.githubusercontent.com 
151.101.100.133 camo.githubusercontent.com 
151.101.100.133 avatars0.githubusercontent.com 
151.101.100.133 avatars1.githubusercontent.com 
151.101.100.133 avatars2.githubusercontent.com 
151.101.100.133 avatars3.githubusercontent.com 
151.101.100.133 avatars4.githubusercontent.com 
151.101.100.133 avatars5.githubusercontent.com 
151.101.100.133 avatars6.githubusercontent.com 
151.101.100.133 avatars7.githubusercontent.com 
151.101.100.133 avatars8.githubusercontent.com 
~~~
- Windows系统下：  
1. 修改 C:\Windows\System32\drivers\etc 中的hosts文件（PS：若没有修改权限，可以鼠标右键，属性，安全，修改权限。或者将hosts文件复制s到桌面，修改之后，复制到原文件夹）  
2. 将上述【需添加代码】复制到hosts文件中，保存文件，刷新GitHub  

- Mac系统下：  

1. 打开终端，编辑hosts文件  
~~~
sudo vim /etc/hosts
~~~     
2. 根据提示进行编辑，点击`i`进行Insert或者点击`E`进行Edit   
3. 添加上述【需添加代码】
4. 输入`:wq`退出界面
5. 刷新DNS
~~~
dscacheutil -flushcache
~~~     
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
  - [问题3](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%983):学习过程中了解到Vuforia主要使用各种「识别」的方式来实现AR效果，然而本毕业设计并不涉及到图像识别；   
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
  - [问题16](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9816):iOS与unity代码间的交互   
  - [问题17](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9817):已解决，可以检测垂直平面    
  - [问题18](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9818):由于模型的预设不一致，方向角度不一样，导致相同的触屏手势会造成不同的位移。  
  - [问题19](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9819):这个我不打算解决并且我也解决不了...在将摄像头对准墙壁或其他比较干净整洁的平面时，往往无法识别到特征点.     
  - [问题21](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9821):iOS开发问题「apple mach -o linker(id) error」
  - [问题22](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9822):macOS系统升级的问题。   
  - [问题23](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9823):光照估计获取数值的部分需要设备支持TrueDepth。   
  - [问题24](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9824):旧版sdk与unity新版导出iOS格式文件有所不同，导致的Calling TargetGuidByName with name='Unity-iPhone' is deprecated.     
  - [问题20](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9820):放进来的模型位置不稳定  



