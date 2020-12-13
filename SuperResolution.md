# Table of Contents
- [Super Resolution](#super-resolution)
- [Video Super Resolution](#video-super-restoration)

#  Super Resolution
###  *Super-Resolution with Raw Images*
**[Paper]**  (CVPR 2019) Towards Real Scene Super-Resolution with Raw Images  <Br>
**[Author]** [Xiangyu Xu](https://sites.google.com/view/xiangyuxu/%E9%A6%96%E9%A1%B5), Yongrui Ma, [Wenxiu Sun](http://wenxiusun.com/) <Br>
**[[Project](https://sites.google.com/view/xiangyuxu/rawsr_cvpr19)]** <Br>
大致浏览, 利用Raw做细节恢复, 用RGB做Color校正.<Br> 
	
### SFTMD ★
**[Paper]**  (CVPR 2019) Blind Super-Resolution with Iterative Kernel Correction <Br>
**[Author]** [Jinjin Gu](http://www.jasongt.com/), Hannan Lu, [Wangmeng Zuo](http://www.jasongt.com/projectpages/IKC.html), Chao Dong<Br>
**[[Project](http://www.jasongt.com/projectpages/IKC.html)]** <Br>
1) 粗读, 提出一个基于深度学习的交替预测blur kernel和预测超分结果的模型, 对给定的blur有很好的效果 <Br>
2) 文中提出的预测blur kernel并用其辅助超分的思路很有意思, 但对真实图像而言无法获得真实的blur kernel用于训练, 另外论文似乎假设一张图像只有一种blur kernel, 感觉不太合理  <Br>
	
### CameraSR ★
**[Paper]**  (CVPR 2019) Camera Lens Super-Resolution <Br>
**[Author]** Chang Chen, Zhiwei Xiong, Xinmei Tian, Zheng-Jun Zha, Feng Wu<Br>
**[[Code & Data](https://github.com/ngchc/CameraSR)]** <Br>
文章认为普通的插值退化不能模拟由于焦距-FOV变化带来的退化 (其实这是一个无论从分析上还是工程中都很明显的事实...). 最重要的贡献是提出了一个真实DSLR和手机的数据集, 但是在生成单反数据集时, 貌似没有考虑焦距变化带来的景深变化.
	
### DPSR ★
**[Paper]**  (CVPR 2019) Deep Plug-and-Play Super-Resolution for Arbitrary Blur Kernels <Br>
**[Author]** [Kai Zhang](https://cszn.github.io/), [Wangmeng Zuo](http://homepage.hit.edu.cn/wangmengzuo), [Lei Zhang](http://www4.comp.polyu.edu.hk/~cslzhang/)<Br>
**[[Pytorch-Code](https://github.com/cszn/DPSR)]** **[[Pytorch-IR-Toolbox](https://github.com/cszn/KAIR)]** <Br>
1. 把HR到LR的退化解释成bicubic降采样+非盲blur kernel退化+加性高斯白噪声的过程. 
2. 将求解过程用HQS变量分裂法分解为去模糊和超分+去噪两步, 第一步在频谱域求闭式解, 避免了模糊现象; 第二步可以使用现有的SR方法, 只需额外加入一噪声level. 采用迭代的形式交替求解.
3. 非盲kernel这个先验其实挺强的, 而且只在生成的数据集上做了实验. 但是实际效果来看, 在真实图像上的效果的确很不错.
	
### GRSNet ★
**[Paper]**  (CVPR 2020) Guided Frequency Separation Network for Real-World Super-Resolution <Br>
**[Author]** Yuanbo Zhou, Wei Deng, Tong Tong, Qinquan Gao<Br>
**[[Pytorch-Code](https://github.com/fzuzyb/2020NTIRE-Guided-Frequency-Separation-Network-for-RWSR)]** <Br>
使用一套基于GAN的无监督方案生成真实LR图像对, 在该方案中提出了所谓颜色引导生成器网络, 用于产生AdaIn中的参数. 

### MAFFSRN ★☆
**[Paper]**  (arXiv 2008) Ultra Lightweight Image Super-Resolution with Multi-Attention Layers <Br>
**[Author]** Abdul Muqeet, Jiwon Hwang, Subin Yang, Jung Heum Kang, Yongwoo Kim, Sung-Ho Bae<Br>
**[[Code](https://github.com/AbdulMoqeet/MAFFSRN)]** <Br>
轻量级超分网络, 在AIM 2020上取得了不错的成绩, 结构可学习
	
### RFDN ★☆
**[Paper]**  (arXiv 2009) Residual Feature Distillation Network for Lightweight Image Super-Resolution <Br>
**[Author]** Jie Liu, Jie Tang, Gangshan Wu<Br>
**[[Pytorch-Code](https://github.com/njulj/RFDN)]** <Br>
AIM2020-ESR冠军方案, 基于IDN提出了几点改善.


# Video Super Resolution
### STARnet
**[Paper]**  (CVPR 2020) Space-Time-Aware Multi-Resolution Video Enhancement <Br>
**[Author]** [Muhammad Haris](https://alterzero.github.io/), [Greg Shakhnarovich](https://ttic.uchicago.edu/~gregory/), [Norimichi Ukita](https://www.toyota-ti.ac.jp/Lab/Denshi/iim/ukita/)<Br>
**[[Pytorch-Code](https://github.com/alterzero/STARnet)]** <Br>
