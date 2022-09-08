# DSM 模型

## 论文

- Vincent，Pascal, “A Connection Between ScoreMatching and Denoising Autoencoders,” 2011.

## 大概思想

这篇文章主要工作是将 denoising autoencoder 和 score mathching 联系在了一起，提出了 Denoising Score Matchine (DSM), 并且启发了后来的很多工作。

## 具体细节

### DSM 的拟合数据和 score matching 的区别：

score matching 拟合的是原始数据的 log 梯度，
DSM 拟合加了噪声的数据 log 梯度（和 denoising autoencoder 做法相似）

### 在数据里加噪声动机：

（i）和 denoising autoencoder 里提的差不多；

（ii）原始 score matching 里面如果数据不多的话，梯度估计的不准，那后期在采样时，样本质量不太高，在数据上做点扰动，可以起到一定数据增广的效果，再者可以控制噪声力度（可控制生成数据和原数据的相似度），类似 DDPM 的思想；
（iii）作者通过添加高斯噪声最后推导出一个新的公式，这个新的公式比原来的 score matching 的要好，后面会说明。
### Denoising Autoencoder 简介
**(i)加噪声的数据：**
对于输入数据 $x \in \mathbb{D^n}$，在上面添加一个方差为$\sigma^2 I$高斯噪声, 这里$I$是单位阵，$\sigma^2$对应他对角线上的噪声强度，那么输入数据就变成了$\tilde{x}=x+\epsilon, \epsilon \sim N(0, \sigma^2 I)$ 也是高斯分布.
$q(\tilde{x}|x)=N(x, \sigma^2 I)=\frac{1}{(2 \pi)^{d/2} \sigma^d } exp^{ -\frac{1}{2\sigma^2}\|\tilde{x}-x\|^2}$, 扰动之后的data 是之前数据的一个条件分布。

**(ii)降噪自编码器：**
要加噪的数据通过自编码器来恢复没有噪声的数据，来学到一个对数据的鲁棒的表示， 对应object function 为：$L_\theta= \mathbb{E}_{q_{\sigma}(\tilde{x},x)} [ \| decoder(encoder(\tilde{x})) -x \|^2]$

**(iii)denoising score matching：**
还是原始的score matching的目标函数：$L=\frac{1}{2} \mathbb{E}_{p_{data}}[ \| \nabla_x \log p _{data} (x)- \nabla_x \log p_\theta(x)\|^2 ]$
DSM是从添加了噪声的数据分布中进行采样，因此目标函数变为：
$L=\frac{1}{2} \mathbb{E}_{q_{\sigma}({\tilde{x}|x})}[ \| \nabla_\tilde{x} \log_{q_{\sigma}({\tilde{x}|x})} (\tilde{x})- \nabla_\tilde{x} \log p_\theta(\tilde{x})\|^2 ]$<br>
**注意：**
（i）对于原始的score matching, 数据分布是不知道的，但是对于加了噪声之后的噪声分布$q$是知道的。
$\nabla_\tilde{x} \log_{q_{\sigma}({\tilde{x}|x})} (\tilde{x})= \nabla _\tilde{x} log {\frac{1}{(2 \pi)^{d/2} \sigma^d } exp^{ -\frac{1}{2\sigma^2}\|\tilde{x}-x\|^2}}= -\frac{\tilde{x}-x}{\sigma^2}$ 
最后的object function是
$L=\frac{1}{2} \mathbb{E}_{q_{\sigma}({\tilde{x}|x})}[ \| \nabla_\tilde{x} \log p_\theta(\tilde{x}) +\frac{\tilde{x}-x}{\sigma^2}\|^2 ]$ <br>
（ii）比原始实现的好处是没有二阶导数了，对于目标函数的第一项可以用一个神经网络来估计模型的梯度。实现也更加简单了。
