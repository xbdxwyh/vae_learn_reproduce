# vae_learn_reproduce
 learn vae simple

学习VAE的基本原理后参考网上的知识对VAE的pytorch版本的简单复现

### 数据集
数据集选了最简单的手写数字，直接从torchvision加载，也可以换别的记得改网络大小

### 关于代码
VAE-multi-linear是选择了多层线性层做编码，对手写数字进行编码和解码

VAE-conv 则是使用了卷积网络进行这些操作

### 参考

原理参考苏剑林大神的[科学空间解析](https://spaces.ac.cn/archives/5253)以及原始[VAE论文](https://arxiv.org/abs/1312.6114)中有关损失函数的一点

代码部分主要参考了[苏剑林大神的keras复现](https://github.com/bojone/vae) 和 [SHEN Xiaohai的博客](https://shenxiaohai.me/2018/10/20/pytorch-tutorial-advanced-02/)

### 结果
具体超参数我没有怎么设置，随便写了写，50个epoch后，大致结果如图所示
![采样并重建图片](/vae_mnist/reconst-51.png "采样并重建图片，原始图片为左列，重建图片为右列")

![采从噪声重建图片](/vae_mnist/sampled-51.png "从噪声直接重建图片")

可以看到VAE生成的图片还是偏模糊的，但是训练确实很稳定，另外还有一点，VAE的Loss数值相对会比较高，因为有重建项的计算。
