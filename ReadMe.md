#### 简介

#### 综述

# 北大最新《扩散模型:方法和应用》综述
* [Yang, L., Zhang, Z., Song, Y., Hong, S., Xu, R., Zhao, Y., ... & Yang, M. H. (2022). Diffusion models: A comprehensive survey of methods and applications. arXiv preprint arXiv:2209.00796.](https://arxiv.org/abs/2209.00796)
* 
[最近大火的“扩散模型”首篇综述来了！北大最新《扩散模型:方法和应用》综述，23页pdf涵盖200页文献](https://zhuanlan.zhihu.com/p/562029290)

# UCF等《视觉扩散模型》综述
* [Croitoru, F. A., Hondru, V., Ionescu, R. T., & Shah, M. (2022). Diffusion models in vision: A survey. arXiv preprint arXiv:2209.04747.](https://arxiv.org/abs/2209.04747)

* [UCF等《视觉扩散模型》综述，20页pdf详述三种通用的扩散建模框架](https://zhuanlan.zhihu.com/p/564358628)

# 视觉的有效扩散模型综述
* [Ulhaq, A., Akhtar, N., & Pogrebna, G. (2022). Efficient Diffusion Models for Vision: A Survey. arXiv preprint arXiv:2210.09292.](https://arxiv.org/abs/2210.09292)

* [视觉的有效扩散模型综述](https://www.zhuanzhi.ai/vip/c3a78910052e2d5b9a17b08e65630fc0)

# 西湖大学李子青等最新《生成式扩散模型》综述
* [Cao, H., Tan, C., Gao, Z., Chen, G., Heng, P. A., & Li, S. Z. (2022). A survey on generative diffusion model. arXiv preprint arXiv:2209.02646.](https://arxiv.org/abs/2209.02646)

* [西湖大学李子青等最新《生成式扩散模型》综述，18页pdf详解扩散模型基础、方法体系和应用](https://www.zhuanzhi.ai/document/8253c59f6277f95a1fa21b53ed48ee85)


# 肿块
*J. Zhang, E. H. Cain, A. Saha, Z. Zhu, and M. A. Mazurowski, “Breast mass detection in mammography and tomosynthesis via fully convolutional network-based heatmap regression,” in Medical Imaging 2018: Computer-Aided Diagnosis, vol. 10575\. International Society for Optics and Photonics, 2018, p. 1057525.*

这篇文章主要讲的是一个在mammography图像中寻找乳房肿块的工作。

首先，介绍一下mammography，mammography是一种x射线成像，成像过程和结果大致如下：

![Lakeside Women&#39;s Hospital](https://upload-images.jianshu.io/upload_images/1496926-4b052b38465f6c35.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



首先是heatmap regression，在FCN那篇paper（Fully Convolutional Networks for Semantic Segmentation）的第三页处有相关内容。在我看来，heatmap更像是一种模糊的语义分割而不是一个精确的语义分割，因此对于训练集的标注精确度要求可能也会小一些。

其次，loss func依据的是F-score而不是Acc。作为统计量来说，F-score相比Acc的优点是他在数据集不平衡（大量的Actual Negatives）的时候表现更好。具体来说，如这个例子中，大部分的房体都是没有肿块的False只有少部分是有肿块的。

作者还做了一个迁移学习的工作，把在Mammography上训练的网络fine-tune之后放在DBT图像上跑，也取得了比直接训练更好的结果。鉴于DBT就是一个多角度的mammography，这也没什么好奇怪的。





#### Thesis

1.  [Thijs Kooi-Computer aided diagnosis of breast cancer in mammography using deep neural networks](http://www.diagnijmegen.nl/index.php/Publication?bibkey=Kooi18)
2.  [《神经网络与深度学习》讲义](http://vdisk.weibo.com/s/ayG13we2ltDAT)，邱锡鹏。

#### 实验室

1.  [Krzysztof J. Geras](https://cs.nyu.edu/~kgeras/)     
 [ ☆Github](https://github.com/nyukat)

2. [Linda Moy](https://nyulangone.org/doctors/1922064559/linda-moy) Breast MRI 
3.  [Rami Ben-Ari,Research Staff Member , IBM](http://benarirami.com/)
[IBM](https://researcher.watson.ibm.com/researcher/view_person_pubs.php?person=il-RAMIB&t=1)
[Personal](https://www.cs.bgu.ac.il/~rba/)

4.  [Li Shen,Icahn School of Medicine at Mount Sinai](http://labs.neuroscience.mssm.edu/project/shen-lab/)
[scholar.google](https://scholar.google.com/citations?user=3QhdnTYAAAAJ)
[linkedin](https://www.linkedin.com/in/lshen/)
 [ ☆Github](https://github.com/lishen)
5.  [breast imaging (Haifa Labs,IBM)](https://www.research.ibm.com/haifa/dept/imt/mia_research.shtml#Approach)
[Computer vision algorithms](https://www.research.ibm.com/haifa/dept/imt/mia_research.shtml)

6. [Thijs Kooi](http://www.thijskooi.com/index.php)
[Github](https://github.com/thijskooi)
[Linkedin](https://de.linkedin.com/in/thijs-kooi-0a72b126)
[Diagnostic Image Analysis Group](http://www.diagnijmegen.nl/index.php/Home)
7. [Martel Lab](http://martellab.com/research/computer-aided-diagnosis-for-mri-screening-of-the-breast-in-high-risk-women/) Breast MRI & Whole Slide Images
8.[Gabriel Maicas](https://cs.adelaide.edu.au/~gabriel/) Breast MRI
9.[Gustavo Carneiro](https://cs.adelaide.edu.au/~carneiro/)



#### 经典论文

1.  [Wu, Nan, et al. "Deep Neural Networks Improve Radiologists' Performance in Breast Cancer Screening." arXiv preprint arXiv:1903.08297 (2019).](https://openreview.net/pdf?id=SkxYez76FE)
[openreview](https://openreview.net/forum?id=SkxYez76FE&noteId=SkxYez76FE)
2. [Ribli, Dezső, et al. "Detecting and classifying lesions in mammograms with deep learning." Scientific reports 8.1 (2018): 4165.](https://www.nature.com/articles/s41598-018-22437-z)

4.  [Kooi, Thijs, et al. "Large scale deep learning for computer aided detection of mammographic lesions." Medical image analysis 35 (2017): 303-312.](https://www.researchgate.net/profile/Geert_Litjens/publication/305825605_Large_Scale_Deep_Learning_for_Computer_Aided_Detection_of_Mammographic_Lesions/links/5ad850bcaca272fdaf803805/Large-Scale-Deep-Learning-for-Computer-Aided-Detection-of-Mammographic-Lesions.pdf).


#### Code

1.  [2019-Deep Neural Networks Improve Radiologists' Performance in Breast Cancer Screening](https://github.com/nyukat/breast_cancer_classifier)
2.  [2017-Breast density classification with deep convolutional neural networks](https://github.com/nyukat/breast_density_classifier)
3.  [2017-High-resolution breast cancer screening with multi-view deep convolutional neural networks](https://github.com/nyukat/BIRADS_classifier)
4. [2017-End-to-end Training for Whole Image Breast Cancer Diagnosis using An All Convolutional Design](https://github.com/lishen/end2end-all-conv)
[Discuss-End-to-end Training for Whole Image Breast Cancer Diagnosis using An All Convolutional Design](https://www.synapse.org/#!Synapse:syn4224222/discussion/threadId=2694)
[Breast cancer diagnosis using deep residual nets and transfer learning](https://www.synapse.org/#!Synapse:syn9773182/wiki/)
5. [DM Challenge Yaroslav Nikulin (Therapixel) source code](https://www.synapse.org/#!Synapse:syn9819697)

#### Dataset

1.  Data1
    官方网站：[Data1](https://www.tensorflow.org/) 
    


#### Challenge

1.  [[The Digital Mammography DREAM Challenge](https://www.synapse.org/#!Synapse:syn4224222)
](https://www.synapse.org/#!Synapse:syn4224222/wiki/401743)
2.  [https://github.com/ty4z2008/Qix/blob/master/dl.md](https://github.com/ty4z2008/Qix/blob/master/dl.md)
3. [PERFORMS](https://performs.grand-challenge.org/Home/)

#公司：
[Vara](https://www.varahealthcare.com/)
[Merantix](https://www.merantix.com/)
[ PERFORMS.](https://performs.international/)
[Paragon](https://paragonbiosci.com/)



#FDA
[首个获 FDA 批准的 AI 乳腺癌诊断系统诞生：能降低 39% 漏诊率](https://mp.weixin.qq.com/s?__biz=MzI4MjA2MjY1Ng==&mid=2652842167&idx=2&sn=6d3c7bfa7beae79634f7f1f7e04037b6&chksm=f0743298c703bb8e5e981e5504e9a1f564f4a141eb239e332b4560f7861d522742e4c00ad14a&mpshare=1&scene=1&srcid=0724UgTTLrbOFvvkaS8HGMQN&sharer_sharetime=1564046829212&sharer_shareid=095144b48b933ab9e542b3bc79a838bf&key=a5cc6adf06aaa96ab331c5fdaa7a574a6853dcb112bd1f8601e338af12f2662ac02f26c4b232b108e0dfc3a14ce0bb7206c3b5527279cebc3ef09787d2748f514c825a24edc3d853af6297947c45e04e&ascene=1&uin=MjkyNDEyNTQyNg%3D%3D&devicetype=Windows+10&version=62060833&lang=en&pass_ticket=EqPiE3rZMOgpiY7AArJzP5ZvkLWB%2Fr6Lv425iQx9x07YlmpXKiYQ0%2B60cj12%2Foh0)
# [This AI breast cancer diagnostic tool is the first to get FDA clearance](https://www.fastcompany.com/90377791/quantx-is-first-ai-breast-cancer-diagnostic-tool-cleared-by-fda "This AI breast cancer diagnostic tool is the first to get FDA clearance")

[ScreenPoint Medical Receives FDA Clearance for Transpara Mammography AI Solution](https://www.itnonline.com/content/screenpoint-medical-receives-fda-clearance-transpara-mammography-ai-solution)
[Computers Match Accuracy of Radiologists in Screening for Breast Cancer Risk](https://spectrum.ieee.org/the-human-os/robotics/artificial-intelligence/computers-match-human-accuracy-in-screening-for-breast-cancer-risk)
#[iCAD](https://www.icadmed.com/index.html)

[The list of FDA approved algorithms in medicine](https://medicalfuturist.com/fda-approvals-for-algorithms-in-medicine)
[女性的福音：MIT研究员最新AI模型可提前5年预测乳腺癌风险！](https://mp.weixin.qq.com/s?__biz=MzAxMzc2NDAxOQ==&mid=2650372443&idx=1&sn=5d5d3a37d18ba4b1e344bbc3a5c53a1c&chksm=83904d87b4e7c491c47d346cdb715b99ed00a0a2431a1705a1bee23ba825a3015350ade6eb25&mpshare=1&scene=1&srcid=&key=311d683e94e8e056ca304b486866b26e214cc42d476eb1609f4c00f7951e2a58a136ad99c5d167997bb2dcce5dd6667e9b6ac52624d76c72f943000515298a45e6ac7c4e96c516e9ed6507cedf905634&ascene=1&uin=MjkyNDEyNTQyNg%3D%3D&devicetype=Windows+10&version=62060739&lang=en&pass_ticket=4HZyq8j%2BW0EGQZeV%2BnJEB9Mt1xlCQ8wzEWzzU%2BGjCovfTT3QE2D9YSCnsS3aqJWn)
