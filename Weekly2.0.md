# 毕业设计完成记录  
本文档为Luwen Zhang的毕业设计【第二阶段】完成记录

### week16 0418  
完成任务：  
- 主要在完成论文（写论文为何上瘾），开启日常产出论文之后。毕设和论文一起弄了。 
  
<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/LightEstimateMerge.png" width="50%" height="50%"/></div>     

- 重新测试了之前由于设备不支持的光照估计的功能，将其插到了主工程文件中。    
- 搜集了XR interaction的一些便捷交互动作，重新建了个小的工程文件进行开发与测试，正在和自己的主要工程进行整合。     
- 正在一步一步解决之前存在的小问题，根据记录内容进行调整，还有多个功能项目的合并。已经把自己目前的整个工程文件和iOS原生app进行了整合，可以正常跳转交互了，但是iOS的界面UI还没做，是接下来的任务。  
- 关于之前那个合并多个文件之后的版本问题，旧问题根据之前的解决办法已解决；另外的新出的问题是由于旧版sdk与新版unity之间命名冲突的问题，已解决[问题24](https://github.com/clarazwen/ProgressReport/blob/master/ProblemsAndSolutions/Problems_and_solutions.md#%E9%97%AE%E9%A2%9824)  
- 关于论文的问题：对于有的部分，不可避免的会用到网上的资料，尤其是背景和技术原理这一类的，那这些都一定要用自己的话再说一遍吗？  

毕业论文：  
 - 调整了毕业论文的大纲，开始完成已确定部分的论文内容，已完成第一章与第二章大部分的论文初稿（进度20%）。     
 - 建立了新的文件，用来保存完成论文时用到的资料。   
 
工作安排：  
- 继续完成论文，根据之前的开发记录，撰写内容，不断调整。    
- 清醒一点，加速完成还没写完的代码开发，调整一下iOS的界面美观。    
### week17 0425  
完成工作：   
- 尝试在界面中加入了一些UX内容，是iOS风格的动画，起到引导的作用。  

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/UX%26UI/UX2.jpg" width="50%" height="50%"/></div>  

- 测量功能的后续完善：在之前开发的基础上实现了连续的多点的测量，可以任意放置多个标记测量每两个点之间的距离，也补充进入了一键清除场景内所有标记点的功能（面积方面就不再补充新内容了）。然而引入了新的条件控制之后还没有调整界面交互。   
放置标记和测量的方式还是比较随意，接下来准备加入测量过程中的UX引导，比如可视化连接线等。    

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/Measure/RepeatedlyMeasure1.png" width="50%" height="50%"/></div>  

- 使用AR Portal的方式进行了样板间的展示，点击检测到的平面之后就会以当前平面为地面放置一个虚拟的房间。因为还没有找到合适的丰富的家居场景，目前房屋内还只有墙体，地板，门，壁画和电视等。不过都有贴图和材质，所以看起来效果还可以。  
- 根据测试设备统一了工程文件中的屏幕尺寸，效果稍微好了点儿。   
- 统一了不同功能工程文件中的不同开发方式，将全部已实现功能和整体框架结合之后更新了一下。  

毕业论文（35%，1.2w+）：   
- 完成了论文前两章全部和第三章大部分内容，对标注出来的网上的资料重新进行内容理解与修改。    
- 其余内容，如测试和未来展望等内容要等代码这边全都完成再写。   

工作安排：  
- 继续写论文，完成第三章和第四章中可以完成的内容。  
- 多点测量目前还必须在检测到的平面上进行，调整为「不需检测平面即可进行测量」，再补充一点动态效果进去。   
- portal的部分要补充样板间的更多模型，或者再找找有没有成型较为完整的房屋场景，添加多种风格的样板间。    
- iOS正在学习界面UI怎么做，还没完成....（崩溃    
### week18 0503    
完成工作：  
- iOS首页的设计基本完成了，剩里面具体的功能准备用产品原型软件（墨刀之类的）直接做出来，不实现功能。大概内容如下：       

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/iOSUI1.0.jpg" width="50%" height="50%"/></div>     

等所有unity方面的工作完成之后，两个工程整合起来就ok了，这个已经比较熟练了。      
- 完成了测量可视化，以及闭环绘制曲线。使用了LineRenderer绘制线段或自定义曲线，研究怎么把组件结合到AR上研究了很久。使用LineRenderer可以调整线条的各种参数，粗细颜色等，目前在调整细节。     

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/LineRenderRefer.jpg" width="50%" height="50%"/></div>     

这个图是完成过程中参考资料的图。完成周报时间有限，目前自己没录制GIF图。效果还行。      
-  实现了样板间的展示，各种建模网站淘宝asset store买了不少....因为全虚拟模型不能接受真实世界光照的作用，需要自己建立光源。正在挑选和调整初始位置，灯光参数啥的。已经测试过了个别模型，可以在AR场景中使用，效果良好。         

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/ARHouseModel1.jpg" width="50%" height="50%"/></div>     

- 下载的模型除了asset store，其他的全是.max格式的。解决了3dmax使用Vray建模之后，Unity不识别材质的问题。[3dmax+VRay导入到unity中如何保持效果正常](https://blog.csdn.net/linyisonger/article/details/82795684) （这个如果找同学帮忙的话可能会麻烦死...    

毕业论文：   
- 论文在写主要的第四章了，等基本完成之后再写测试过程，未来和展望完成了主要的点。    

工作安排：   
- 对着任务书，中期检查表等整理了一下要完成的内容。   

<div align=center><img src="https://github.com/clarazwen/ProgressReport/blob/master/Pictures/0503ToDO.png" width="90%" height="90%"/></div>     

- 把后续工作基本完善，做一下iOS还没完成的内容界面。   
- 完成毕业论文全部内容，自我查重。  

暂时想到这里，待更新。
