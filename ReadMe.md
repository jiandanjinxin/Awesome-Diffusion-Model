#### 简介

#### 综述

# 北大最新《扩散模型:方法和应用》综述
* [Yang, L., Zhang, Z., Song, Y., Hong, S., Xu, R., Zhao, Y., ... & Yang, M. H. (2022). Diffusion models: A comprehensive survey of methods and applications. arXiv preprint arXiv:2209.00796.](https://arxiv.org/abs/2209.00796)

* [最近大火的“扩散模型”首篇综述来了！北大最新《扩散模型:方法和应用》综述，23页pdf涵盖200页文献](https://zhuanlan.zhihu.com/p/562029290)

# UCF等《视觉扩散模型》综述
* [Croitoru, F. A., Hondru, V., Ionescu, R. T., & Shah, M. (2022). Diffusion models in vision: A survey. arXiv preprint arXiv:2209.04747.](https://arxiv.org/abs/2209.04747)

* [UCF等《视觉扩散模型》综述，20页pdf详述三种通用的扩散建模框架](https://zhuanlan.zhihu.com/p/564358628)

# 视觉的有效扩散模型综述
* [Ulhaq, A., Akhtar, N., & Pogrebna, G. (2022). Efficient Diffusion Models for Vision: A Survey. arXiv preprint arXiv:2210.09292.](https://arxiv.org/abs/2210.09292)

* [视觉的有效扩散模型综述](https://www.zhuanzhi.ai/vip/c3a78910052e2d5b9a17b08e65630fc0)

# 西湖大学李子青等最新《生成式扩散模型》综述
* [Cao, H., Tan, C., Gao, Z., Chen, G., Heng, P. A., & Li, S. Z. (2022). A survey on generative diffusion model. arXiv preprint arXiv:2209.02646.](https://arxiv.org/abs/2209.02646)

* [西湖大学李子青等最新《生成式扩散模型》综述，18页pdf详解扩散模型基础、方法体系和应用](https://www.zhuanzhi.ai/document/8253c59f6277f95a1fa21b53ed48ee85)


# Github Awsome-Diffusion-Model
1. *https://github.com/heejkoo/Awesome-Diffusion-Models*

2. *https://github.com/YangLing0818/Diffusion-Models-Papers-Survey-Taxonomy*

3. *[深入浅出详解扩散模型：首篇综述与Github论文分类汇总](https://www.zhuanzhi.ai/document/5e5c5e21b4dd39c404005e9fcbbb74aa)*



#### Videos

1.  [详解扩散模型：从DDPM到稳定扩散，附Slides与视频](https://www.zhuanzhi.ai/vip/399b8910da08e2d3bc730c0743857e50)
2.  [《神经网络与深度学习》讲义](http://vdisk.weibo.com/s/ayG13we2ltDAT)，邱锡鹏。

#### 博客

1.  [生成扩散模型漫谈：统一扩散模型（理论篇）](https://mp.weixin.qq.com/s/vwytsN2PkM_P2dVhDi2wzw)     

2.  [生成扩散模型漫谈：DDIM = 高观点DDPM](https://mp.weixin.qq.com/s/70hLn8JVuP1f0-NndwGK9w)

3.  [生成扩散模型漫谈：一般框架之ODE篇](https://mp.weixin.qq.com/s/kBY8LBVpmLeX4sdKXMJr1A)

4.  [生成扩散模型漫谈：最优扩散方差估计（上）](https://mp.weixin.qq.com/s/ai24h-pR3JC3WmRmxUEeFA)



#### 经典论文

1.  [【NeurIPS2022】扩散视觉反事实解释](https://www.zhuanzhi.ai/vip/9e3c00f8bdd63a1065ca83ce6d06b978)

    [Code](https://github.com/valentyn1boreiko/DVCEs)
    
    视觉反事实解释(VCEs)是理解图像分类器决策的重要工具。它们是“小”但“现实”的图像语义变化，改变了分类器的决策。当前生成VCEs的方法局限于对抗鲁棒模型，通常包含非现实的人工制品，或者局限于类别较少的图像分类问题。在本文中，我们通过扩散过程为任意ImageNet分类器生成扩散视觉反事实解释(DVCEs)来克服这一问题。对扩散过程的两个修改是我们的DVCEs的关键:首先，自适应参数化，其超参数在所有图像和模型中都具有泛化性，再加上距离正则化和扩散过程的后期开始，使我们能够生成对原始图像具有最小语义变化但分类不同的图像。其次，我们通过对抗鲁棒模型的锥正则化确保扩散过程不会收敛到琐细的非语义变化，而是生成目标类的真实图像，分类器获得了高可信度。代码可在https://github.com/valentyn1boreiko/DVCEs下获得。
    

2. [英伟达&Google最新《基于扩散的去噪生成建模基础与应用》教程，182页ppt带你学习高保真图像生成](https://www.zhuanzhi.ai/vip/abfbb1753f79f7596e11fbdda8cfcc34)

   https://cvpr2022-tutorial-diffusion-models.github.io/

3. #### Diffusion相关论文

   ### [3.1-DDPM：Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239)
   
   ### [3.2-iDDPM：Improved Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2102.09672)
   
   ### [iDDPM-Code](https://github.com/openai/improved-diffusion)
   
   ### [3.3-DDIM：Denoising Diffusion Implicit Models](https://arxiv.org/abs/2010.02502)
     
   ### [3.4-NCSN_v1：Generative Modeling by Estimating Gradients of the Data Distribution](https://arxiv.org/abs/1907.05600)   
  
   ### [NCSN_v1-Code](https://github.com/ermongroup/ncsn)
   
   ### [3.5-NCSN_v2：Improved Techniques for Training Score-Based Generative Models](https://arxiv.org/abs/2006.09011)
  
   ### [NCSN_v2-Code同NCSN_v1](https://github.com/ermongroup/ncsn)
   
   ### [3.6-NCSN_v3：Score-Based Generative Modeling through Stochastic Differential Equations](https://arxiv.org/abs/2011.13456)
  
   ### [NCSN_v3-Code](https://github.com/yang-song/score_sde)
   

#### Code

1.  [首个中文Stable Diffusion模型开源，IDEA研究院封神榜团队开启中文AI艺术时代](https://mp.weixin.qq.com/s/mtZ8K6d2ST5Mkj3JZUHwqA)

2.  太乙 Stable Diffusion 纯中文版本：https://huggingface.co/IDEA-CCNL/Taiyi-Stable-Diffusion-1B-Chinese-v0.1

    太乙 Stable Diffusion 中英双语版本：https://huggingface.co/IDEA-CCNL/Taiyi-Stable-Diffusion-1B-Chinese-EN-v0.1
   
3.  [improved DDPM代码讲解](https://www.bilibili.com/video/BV1sG411s7vV/?spm_id_from=333.880.my_history.page.click&vd_source=68b8dcbf12aa4787d80601b51d31e25a)

4.  [DDIM代码讲解](https://www.bilibili.com/video/BV1JY4y1N7dn/?spm_id_from=333.788.recommend_more_video.1&vd_source=68b8dcbf12aa4787d80601b51d31e25a)




