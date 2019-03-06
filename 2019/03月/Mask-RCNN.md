### Mask R-CNN

```
本文主要讲解mask RCNN  这是2017年何凯明大佬又一力作

论文地址：https://arxiv.org/pdf/1703.06870v3.pdf

代码开源地址： https://github.com/ facebookresearch/Detectron

```


**摘要**

这种称为Mask R-CNN的方法通过添加一个用于预测对象掩码的分支来扩展更快的R-CNN，该分支与现有的用于边界框识别的分支并行。掩码R-CNN训练简单，只增加了一小部分开销，以更快的R-CNN，以5fps运行

 `Mask R-CNN就是Faster R-CNN 加上一个用于像素语义分割的FCN。`


 **Mask RCNN整体架构**

![mask_1](img/mask_1.png)
![](img/mask_3.png)
![](img/mask_2.png)



** 相关知识点 **

`Faster RCNN整体架构`

![Faster RCNN](img/mask_4.png)


`RPN 详见`[RPN简介](RPN.md)


`FPN 空间金字塔`


作者利用了固有的多尺度和锥形层次结构的卷积网络来构造具有边际额外成本的金字塔网络，开发具有侧向连接（Skip Connector）的自顶向下的架构，用于在所有尺度上构建高级语义特征图，依靠一种通过自上而下的路径和横向连接将低分辨率但语义强的特征与高分辨率语义弱的特征结合在一起，这样就可以获得高分辨率，强语义的特征，有利于小目标的检测。这种结构是在CNN网络中完成的，和前文提到的基于图片的金字塔结构不同，而且完全可以替代它。

![FPN](img/FPN.png)
![FPN2](img/FPN2.png)
![FPN3](img/FPN3.png)
