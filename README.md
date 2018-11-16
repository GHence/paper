## 记录自己所看论文

入门AI大军，也有一段时间了。现在打算真正静心看看论文，分享到github记录个人成长经历，也是对自己的一种监督， 望大佬多多赐教。如有疑问请联系：1163753605@qq.com
***


# **日记**
---
[2018-11-16](2018/11月/7.md)：VGG和GoogLeNet 网络结构。

[2018-11-15](2018/11月/6.md): AlexNet论文。详细地解读见论文分类中地 Image CClassification AlexNet。个人笔记见[此处](2018/11月/6.md)

[2018-11-11](2018/11月/5.md)：这是arXiv上的一篇文章，上个月末被NIPS2018会议收录的来自Google Brain的论文。文中 巧妙地改造了dropout，借鉴相关论文（spatialBlock） 的方法，提出了DropBlock方法来改造CNN中的卷积层和全连接层，实验证明效果很好，值得一读
<br>

[2018-11-8](2018/11月/4.md)： 这是一篇博士论文。本论文 主要讲解三个方便的研究问题， 具体如下：
  - 基于标记一阶线性关联关系的深度学习算法
  - 基于标记高阶分层结构的多任务协同学习网络
  - 基于深度神经网络的标记结构优化学习
<br>

[2018-11-6](https://github.com/BMDACMER/paper/tree/master/2018/11%E6%9C%88/3.md): 本文采用深度卷积神经网络直接在谱域中对高光谱图像进行分类。设计的网络结果为5层--- input layer, the convolutional layer, the max pooling layer, the full connection layer, and the output layer。
<br>

[2018-11-4](https://github.com/BMDACMER/paper/tree/master/2018/11%E6%9C%88/2、REVIEW_OF_REMOTE_SENSING_IMAGE_SEGMENTATION_TECHNIQUES.md): 一篇论文。讲的是图像分割研究综述，过去与现在对图像分割的常用方法。
<br>

[2018-11-3](https://github.com/BMDACMER/paper/tree/master/2018/11%E6%9C%88/1、Region_Merging_ConsideringWithin-_and_Between-Segment_Heteroge.md): 一篇论文，关于遥感图像分割。本文提出了OHRH方法，同时考虑了分割对象之间的不同和分割后段内的相似性，相比较OH（只考虑对象间的不同）和 lambda-schedule算法（FLSA），通过五个不同研究区域，在无监督学习中表现的更好。

---
 **`论文分类`**

 ## Image Classification

 * AlexNet  
 [ImageNet Classification with Deep Convolutional Neural Networks](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)
 [中文版](http://noahsnail.com/2017/07/18/2017-7-18-AlexNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/07/04/2017-7-4-AlexNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91/)

 * VGG  
 [Very Deep Convolutional Networks for Large-Scale Image Recognition](https://arxiv.org/abs/1409.1556)
 [中文版](http://noahsnail.com/2017/08/17/2017-8-17-VGG%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/08/17/2017-8-17-VGG%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * ResNet  
 [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)
 [中文版](http://noahsnail.com/2017/07/31/2017-7-31-ResNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/07/31/2017-7-31-ResNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * GoogLeNet  
 [Going Deeper With Convolutions](https://arxiv.org/abs/1409.4842)
 [中文版](http://noahsnail.com/2017/07/21/2017-7-21-GoogleNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/07/21/2017-7-21-GoogleNet%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * BN-GoogLeNet  
 [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://arxiv.org/abs/1502.03167)
 [中文版](http://noahsnail.com/2017/09/04/2017-9-4-Batch%20Normalization%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/09/04/2017-9-4-Batch%20Normalization%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * Inception-v3  
 [Rethinking the Inception Architecture for Computer Vision](https://arxiv.org/abs/1512.00567)
 [中文版](http://noahsnail.com/2017/10/09/2017-10-9-Inception-V3%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/10/09/2017-10-9-Inception-V3%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * SENet  
 [Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507)
 [中文版](http://noahsnail.com/2017/11/20/2017-11-20-Squeeze-and-Excitation%20Networks%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/11/20/2017-11-20-Squeeze-and-Excitation%20Networks%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 ## Object Detection

 * YOLO   
 [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640)
 [中文版](http://noahsnail.com/2017/08/02/2017-8-2-YOLO%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/08/02/2017-8-2-YOLO%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * SSD  
 [SSD: Single Shot MultiBox Detector](https://arxiv.org/abs/1512.02325)
 [中文版](http://noahsnail.com/2017/12/11/2017-12-11-Single%20Shot%20MultiBox%20Detector%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/12/11/2017-12-11-Single%20Shot%20MultiBox%20Detector%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * YOLO9000  
 [YOLO9000: Better, Faster, Stronger](https://arxiv.org/abs/1612.08242)
 [中文版](http://noahsnail.com/2017/12/26/2017-12-26-YOLO9000,%20Better,%20Faster,%20Stronger%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/12/26/2017-12-26-YOLO9000,%20Better,%20Faster,%20Stronger%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * Deformable-ConvNets  
 [Deformable Convolutional Networks](https://arxiv.org/abs/1703.06211)
 [中文版](http://noahsnail.com/2017/11/29/2017-11-29-Deformable%20Convolutional%20Networks%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/11/29/2017-11-29-Deformable%20Convolutional%20Networks%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * Faster R-CNN  
 [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](https://arxiv.org/abs/1506.01497)
 [中文版](http://noahsnail.com/2018/01/03/2018-01-03-Faster%20R-CNN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2018/01/03/2018-01-03-Faster%20R-CNN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * R-FCN  
 [R-FCN: Object Detection via Region-based Fully Convolutional Networks](https://arxiv.org/abs/1605.06409)
 [中文版](http://noahsnail.com/2018/01/22/2018-01-22-R-FCN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2018/01/22/2018-01-22-R-FCN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * FPN  
 [Feature Pyramid Networks for Object Detection](https://arxiv.org/abs/1612.03144)
 [中文版](http://noahsnail.com/2018/03/20/2018-03-20-Feature%20Pyramid%20Networks%20for%20Object%20Detection%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2018/03/20/2018-03-20-Feature%20Pyramid%20Networks%20for%20Object%20Detection%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 ## OCR

 * CRNN  
 [An End-to-End Trainable Neural Network for Image-based Sequence Recognition and Its Application to Scene Text Recognition](https://arxiv.org/abs/1507.05717)
 [中文版](http://noahsnail.com/2017/08/21/2017-8-21-CRNN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2017/08/21/2017-8-21-CRNN%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)

 * CTPN  
 [Detecting Text in Natural Image with Connectionist Text Proposal Network](https://arxiv.org/abs/1609.03605)
 [中文版](http://noahsnail.com/2018/02/02/2018-02-02-Detecting%20Text%20in%20Natural%20Image%20with%20Connectionist%20Text%20Proposal%20Network%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E6%96%87%E7%89%88/)
 [中英文对照](http://noahsnail.com/2018/02/02/2018-02-02-Detecting%20Text%20in%20Natural%20Image%20with%20Connectionist%20Text%20Proposal%20Network%E8%AE%BA%E6%96%87%E7%BF%BB%E8%AF%91%E2%80%94%E2%80%94%E4%B8%AD%E8%8B%B1%E6%96%87%E5%AF%B9%E7%85%A7/)
