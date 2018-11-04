# REVIEW OF REMOTE SENSING IMAGE SEGMENTATION TECHNIQUES

---

# 遥感图像分割技术综述

**摘要**

Image segmentation is an important tool in image processing and can serve as an efficient front end to sophisticated algorithms and thereby simplify subsequent rocessing. Image segmentation by region merging follows a particular order in the choice of regions. The target of segmentation is always to simplify and/or change the representation of a graphic into something that is more meaningful and simpler to analyze. Image segmentation is normally used to locate objects and boundaries (lines, curves, etc.) in images. To improve segmentation accuracy and the correctness, this paper proposed a Dynamic Statistical Region Merging (DSRM) algorithm to find the automatically select scale value. The purpose of this paper is to gather various segmentation techniques that can be used for the segmentation of remote sensing images (RSI). The paper provides good starting for researchers to find automatically select scale value using the combination of DSRM and fuzzy logic.

Keywords
Image segmentation, Multi-scale segmentation, Remote sensing image segmentation, Dynamic statistical region merging, Region growing. 


图像分割是图像处理中的重要工具，可以作为复杂算法的有效前端，从而简化后续的处理。 通过区域合并的图像分割遵循区域选择中的特定顺序。 分割的目标始终是简化和/或将图形的表示更改为更有意义且更易于分析的内容。 图像分割通常用于定位图像中的对象和边界（线，曲线等）。 为了提高分割精度和正确性，本文提出了一种动态统计区域合并（DSRM）算法来寻找自动选择比例值。 本文的目的是收集各种可用于遥感图像（RSI）分割的分割技术。 本文为研究人员提供了良好的启动，可以使用DSRM和模糊逻辑相结合的方式自动选择比例值。

---

DSRM特点：


+ 最先测试最相似的区域。刚开始时，重新定义了基于区域的不相似性，然后，动态更新不相似性并在合并任务期间调整测试顺序。 因此，模糊边缘和渐变区域几乎不会导                                     致错误合并。
+ 此外，我们将DSRM扩展到多波段遥感图像，并将其用于多尺度分割。


SRM特点：

+ 也能够构建层次结构，但是在测试区域合并之后的顺序上存在一些问题。
+ 它仅使用相邻像素的灰度差来定义不相似性，具体取决于您的测试顺序
+ 像素差异非常小时，比如 模糊边缘和渐变区域上，SRM可能导致合并错误。
                    随着区域增长，一个对象很容易与下一个对象在模糊边缘或渐变区域上合并，从而导致分割不足  
  
***********************************

第二部分 介绍了文献调查  近年来各学者关于图像分割这块的研究方法  

第三部分  使用的技术方法

3.1 Region Splitting and Merging  区域分裂和合并

区域分裂与合并是从整个图像出发，不断分裂得到各个子区域，然后再把前景区域合并进去，实现目标提取。分裂合并的假设时对于一幅图像，前景区域由一些相互连通的像素组成，因此，如果把一幅图像分裂到像素级，那么就可以判定该像素是否为前景像素，当所有像素点或者子区域完成判断以后，把前景区域或者像素合并就可以得到前景目标。

在这类方法中，最常用的方法时四叉树分解法。设R代表整个正方形图像区域，P代表逻辑谓词。基本分裂合并算法步骤如下：
1）对于一个区域，如果H(Ri) = FALSE 就将其分裂成不重叠的四等份
2）对于相邻的两个区域Ri和Rj，它们也可以大小不同（即不在同一层），如果条件H(RiURj) = TRUE 满足，就将它们合并起来。
3）如果进一步的分裂合并都不可能，则结束

分裂合并算法的关键就是 分裂合并准则的设计。这种方法对复杂图像的分割效果较好，但是算法比较复杂，计算量大，分裂还可能破坏区域的边界。
选用合适的均匀性测试准则P对于提高图像分割质量十分重要，当均匀性测试准则P选择不当时，很容易会引起“方块效应” 参考：https://blog.csdn.net/bagboy_taobao_com/article/details/5666109#commentBox


3.2 K-Means Clustering

详情可参考博客： https://blog.csdn.net/violethan7/article/details/78350353

3.3 Thresholding
 
阈值分割 时最经典的分割技术，也是最简单实用的。许多情况下，图像中目标区域与背景区域或者说不同区域之间其灰度值存在差异，此时可以将灰度的均一性作为依据进行分割。阈值分割即通过一个或几个阈值将图像分割成不同的区域。

阈值分割方法的核心在于如何寻找适当的阈值。最常用的阈值方法是基于灰度直方图的方法，如最大类间方差法(OTSU)、最小误差法、最大熵法等。此类方法通常对整幅图像使用固定的全局阈值，如果图像中有阴影或亮度分布不均等现象，分割效果会受到影响。基于局部阈值的分割方法对图像中的不同区域采用不同的阈值，相对于全局阈值方法具有更好的分割效果，该方法又称为自适应阈值方法。其中阈值的选取一般是基于图像的局部统计信息，如局部方差、局部对比度以及曲面拟合阈值等。无论是基于全局阈值还是局部阈值，阈值方法通常受噪声影响较大。为了得到较好的分割结果，通常还需要与其他图像处理技术，如图像去噪等相结合。

阈值分割的优点是计算简单、运算效率较高、速度快。阈值的选择需要根据具体问题来确定，一般通过实验来确定。对于给定的图像，可以通过分析直方图的方法确定最佳的阈值，例如当直方图明显呈现双峰情况时，可以选择两个峰值的中点作为最佳阈值。

参考： https://blog.csdn.net/u010368556/article/details/70175380


3.4  Region Growing 区域生长

区域生长的基本思想是将具有相似性质的像素集合起来构成区域。具体先对每个需要分割的区域找一个种子像素作为生长的起点，然后将种子像素周围邻域中与种子像素有相同或相似性质的像素(根据某种事先确定的生长或相似准则来判定)合并到种子像素所在的区域中。将这些新像素当作新的种子像素继续进行上面的过程，直到再没有满足条件的像素可被包括进来。这样一个区域就长成了。

区域生长需要选择一组能正确代表所需区域的种子像素，确定在生长过程中的相似性准则，制定让生长停止的条件或准则。相似性准则可以是灰度级、彩色、纹理、梯度等特性。选取的种子像素可以是单个像素，也可以是包含若干个像素的小区域。大部分区域生长准则使用图像的局部性质。生长准则可根据不同原则制定，而使用不同的生长准则会影响区域生长的过程。

区域生长法的优点是计算简单，对于较均匀的连通目标有较好的分割效果。它的缺点是需要人为确定种子点，对噪声敏感，可能导致区域内有空洞。另外，它是一种串行算法，当目标较大时，分割速度较慢，因此在设计算法时，要尽量提高效率。
---------------------
原文：https://blog.csdn.net/u010368556/article/details/70175380

3.5 Fuzzy C- Means Algorithm 

参考博客： https://blog.csdn.net/jia20003/article/details/8800197

Fuzzy C-means算法主要是比较RGB空间的每个像素值与Cluster中的每个中心点值，最终给每个像素指派一个值(0~1之间)说明该像素更接近于哪里Cluster的中心点，模糊规则是该像素对所有cluster的值之和为1。简单的举例：假设图像中有三个聚类cluster1，cluster2，cluster3，像素A对三个聚类的值分别为a1, a2, a3, 根据模糊规则a1 + a2 + a3 = 1。更进一步，如果a1最大，则该像素比较接近于Cluster1。计算总的对象值J：



二：算法流程

初始输入参数:

a.      指定的聚类个数numberOfClusters,

b.      指定的最大循环次数maxIteration

c.      指定的最小终止循环差值deltaValue

大致流程如下：

1.      初始化所有像素点值与随机选取每个Cluster的中心点，初始化每个像素点P[i]对应

Cluster的模糊值p[i][k]并计算cluster index。

2.      计算对象值J

3.      计算每个Cluster的颜色值，产生新的图像像素

4.      计算每个像素的对应每个cluster的模糊值，更新每个像素的Cluster Index

5.      再次计算对象值J，并与第二步的对象值相减，如果差值小于deltaValue或者达到最大

循环数，停止计算输出结果图像，否则继续2 ～ 4


3.6  Artificial Neural Networks  



3.7 Dynamic Statistical Region Merging

最先测试最相似的区域。刚开始时，重新定义了基于区域的不相似性，然后，动态更新不相似性并在合并任务期间调整测试顺序。 DSRM的准确度高于SRM，其计算复杂度近似为线性。


4、Comparison Table

5、Conclusion and Future Scope

本文讨论了分割性能与规模密切相关，但在大多数现有研究中手动选择尺度。此外，在现有研究中不使用模糊逻辑来找到自动尺度值。 因此，将来使用模糊逻辑和动态统计区域合并（DSRM）的组合来设计算法，以便自动选择比例值。








****************************************************************************************

论文链接地址：http://pdfs.semanticscholar.org/71bd/3e87594a1d3467809e545cb3261e641fbac8.pdf

