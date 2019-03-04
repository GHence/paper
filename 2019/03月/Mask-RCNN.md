### Mask R-CNN

```
本文主要讲解mask RCNN  这是2017年何凯明大佬又一力作

论文地址：https://arxiv.org/pdf/1703.06870v3.pdf

代码开源地址： https://github.com/ facebookresearch/Detectron

```


**摘要**

这种称为Mask R-CNN的方法通过添加一个用于预测对象掩码的分支来扩展更快的R-CNN，该分支与现有的用于边界框识别的分支并行。掩码R-CNN训练简单，只增加了一小部分开销，以更快的R-CNN，以5fps运行

 Mask R-CNN就是Faster R-CNN 加上一个用于像素语义分割的FCN。


 **Mask RCNN整体架构**

 ![mask_1](img/mask_1.png)

![](img/mask_3.png)

 ![](img/mask_2.png)
