## SelectionGAN:  Multi-Channel Attention Selection GAN with Cascaded Semantic Guidance for Cross-View Image Translation

> 这是ICCV2019接受的文章，采用多通道注意力机制用于跨视图图像翻译，效果不错

> 摘要
>> Cross-view image translation is challenging because it involves images with drastically different views and severe
deformation. In this paper, we propose a novel approach named Multi-Channel Attention SelectionGAN (Selection-
GAN) that makes it possible to generate images of natural scenes in arbitrary viewpoints, based on an image
of the scene and a novel semantic map. The proposed SelectionGAN explicitly utilizes the semantic information
and consists of two stages. In the first stage, the condition image and the target semantic map are fed into a cycled
semantic-guided generation network to produce initial coarse results. In the second stage, we refine the initial results
by using a multi-channel attention selection mechanism. Moreover, uncertainty maps automatically learned
from attentions are used to guide the pixel loss for better network optimization. Extensive experiments on Dayton
[42], CVUSA [44] and Ego2Top [1] datasets show that our model is able to generate significantly better results
than the state-of-the-art methods. The source code, data and trained models are available at https://github.
com/Ha0Tang/SelectionGAN.

>> 跨视图图像翻译是一项具有挑战性的工作，因为它涉及的图像具有截然不同的视图和严重的变形。
在本文中，我们提出了一种新的多通道注意选择方法(Multi-Channel Attention SelectionGAN, select - gan)，
它可以根据场景的图像和一个新的语义映射生成任意视点的自然场景图像。所提出的SelectionGAN明确地利用语义信息，并由两个阶段组成。
在第一个阶段，将条件图像和目标语义图输入一个循环语义引导生成网络，生成初始粗糙结果。
在第二阶段，我们使用一个多通道注意选择机制来细化初始结果。
此外，还利用从关注点自动学习的不确定度映射来指导像素损失，从而更好地进行网络优化。
在Dayton[42]、CVUSA[44]和Ego2Top[1]数据集上的大量实验表明，我们的模型能够产生比最先进的方法明显更好的结果。
源代码、数据和经过训练的模型可以在https://github.com/Ha0Tang/SelectionGAN上找到。


**相关知识点**

- attention机制
- 跨视图图像翻译：是一项从一个视点到另一个视点合成新图像的任务


### 研究背景

目前图像翻译问题的解决方案一般时基于Encoder-Decoder结构，然而这种方案在原域与目标域图像具有显著不同结构或重叠区域极少的情况下时翻译效果会大打折扣。

作者发现之前利用语义图指导图像翻译的模型对于图像细节的翻译效果不佳，作者认为这是由于语义图一般是由深度预训练模型产生，并不能保证像素级的准确性。

基于此作者提出了级联语义引导下的基于多通道注意力选择机制的图像翻译Selection GAN，其将图像翻译分为两阶段，第一个阶段用于产生粗粒度级的结果，
 第二个阶段通过多通道注意力选择机制产生更细致的结果。


 ### 相关工作



### 模型介绍

![SelectionGAN](img/SelectionGAN.png)
