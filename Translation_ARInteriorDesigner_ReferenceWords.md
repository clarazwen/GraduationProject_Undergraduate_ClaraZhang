## 根据环境语意的特定词汇翻译：
* proportional:成比例的，按照比例的
* perimeter：周长
* skirting：踢脚线
* pseudocode：伪代码
* candidate：候选的
* arbitrary：任意的
* the embedded motion sensors：嵌入式运动传感器
* by default：默认情况下
* a short-cut key：快捷键
* manipulate：操纵
* panel：面板
* respectively：分别
* avoid them from overlapping to each other：以避免它们彼此重叠
* deduce：推断
* undergoing：进行
* fixed by calibrating：通过校准固定
* ease：缓解
## 翻译的比较模糊的句子：
*RANSAC is an algorithm that used to cluster inline points in a point cloud.*

RANSAC是一种用于在点集对内联点（？）进行聚类的算法。

*the inliers of P*

内联点（？）

*topped by some very big number as maximum iterations*

一些非常大的数如最大迭代次数达到上限

*The Floor level slidebar on the left-hand side enables user to fine tune the vertical position of any highlighted plane under noisy environment;*

左侧的地面水平滑块使用户可以在嘈杂的环境下微调任何突出显示平面的垂直位置。

*The scaling of a furniture model need match distance changing between KINECT and the farthest perimeter of the largest supporting plane. *

家具模型的缩放需要匹配Kinect和最大支撑平面的最远周长之间的距离变化。

*by dividing the by dP/dW*

比例参数由dP/dW相除所确定。

*via optimizing an objective function subjected to their geometry and functionality requirements.*

3D家具模型会根据其几何和功能要求通过优化目标函数自动进行布置。

*Also, the obstacles might eaten some backside floor estimated by the plane fitting algorithm, except the obstacles are backed by the wall.*

此外，障碍物可能会吞掉平面几何算法估计出的一些后部地板，除非障碍物是靠墙支撑的。

## 需要着重理解的方法部分：
*As a special feature, our system is able to rotate the furniture to face to the centre of the room model automatically, which ensures they are always backing the wall.*

作为一项特殊功能，我们的系统可以自动旋转家具使其面向房间模型的中心，从而保证它们始终背靠墙。

*Constraints C: A hard constraint is imposed, which consider the overlapping area of any two furniture models are forced to be zero.*

约束C：强制限定了约束，它考虑到任何两个家具模型重叠面积必须为0；

*Automatic arrangement: We treat this as an optimization problem. We use a graph G to represent the arrangement of the furniture. We write the above relationships into equations and put them together into the following objective function:*

自动布置：我们将其视为优化问题。我们使用图形G表示家具的布置。我们将以上的关系写为方程式并且将它们放到以下目标函数中：

*Through a few iterations, the updated V ′ contains the optimized positions and orientations of each furniture model. Figure 9 shows the arrangement results of two examples set of furniture. The upper and lower rows showed the result of furniture of different shapes and sizes.*

通过几次的迭代，更新的V‘包含每个家具模型的优化位置和方向。图9表示了两个示例家具组的布置结果。上排和下排显示了不同形状和大小的家具的结果。

*We assumed that most of the furniture models are putting on the floor. Although our method is capable to recognize more possible supporting planes such as the top surface of a coffee table, however there are still some out-of-sight points, for example, the supporting planes high above the ”eye-level” of the KINECT are unable to be estimated.*

我们假设大多数的家具模型都被放在地上。尽管我们的方法能够识别更多可能的支撑平面，如茶几表面；但是仍然存在一些视线外的点，例如高于Kinect的“视野高度”的支撑平面是无法估计的。














