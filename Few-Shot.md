# Table of Contents
- [Unsupervised Restoration](#unsupervised-restoration)
- [Transfer](#transfer-restoration)



# Unsupervised Restoration
### Deep Photo Enhancer ★☆
**[Paper]** (CVPR 2018 Spotlight) Deep Photo Enhancer: Unpaired Learning for Image Enhancement from Photographs with GANs <Br>
**[Author]** [Yu-Sheng Chen](https://www.cmlab.csie.ntu.edu.tw/~nothinglo/), [Yu-Ching Wang](https://www.cmlab.csie.ntu.edu.tw/~urchinwang/), [Man-Hsin Kao](https://www.cmlab.csie.ntu.edu.tw/~cindy0711/), [Yung-Yu Chuang](https://www.csie.ntu.edu.tw/~cyy/) <Br>
**[[TF-Code](https://github.com/nothinglo/Deep-Photo-Enhancer)]** **[[TF-Code2](https://github.com/pnbao/deep-photo-enhance)]**<Br>
UNet + cycGAN, 无需paired样本的图像增强方法, 可以参考, 只是代码有一点点乱


### LIR-for-Unsupervised-IR ★☆
**[Paper]** (CVPR 2020) Learning Invariant Representation for Unsupervised Image Restoration <Br>
**[Author]** Wenchao Du, Hu Chen, Hongyu Yang  <Br>
**[[Pytorch-Code](https://github.com/Wenchao-Du/LIR-for-Unsupervised-IR)]** <Br>
无监督图像恢复, 使用了GAN, 设计了各种loss
  
  
### *Bringing Old Photos Back to Life* ★☆
**[Paper]** (CVPR 2020 Oral) Bringing Old Photos Back to Life <Br>
**[Author]** [Ziyu Wan](http://raywzy.com/), [Bo Zhang](https://www.microsoft.com/en-us/research/people/zhanbo/), [Dongdong Chen](http://www.dongdongchen.bid/), [Pan Zhang](https://panzhang0212.github.io/), [Dong Chen](https://www.microsoft.com/en-us/research/people/doch/), [Jing Liao](https://liaojing.github.io/html/), [Fang Wen](https://www.microsoft.com/en-us/research/people/fangwen/)  <Br>
**[[Project](http://raywzy.com/Old_Photo/)]** <Br>
无监督老照片恢复, 用生成的老照片训练, 在真实老照片上取得好效果. 使用一个VAE将真实和生成的照片映射到相近的空间, 第二个VAE负责恢复无损照片, 中间还有一些映射等操作. 
 
 ### *Zero-Shot Image Super-Resolution with Depth Guided Internal Degradation Learning*
**[Paper]** (ECCV 2020) Zero-Shot Image Super-Resolution with Depth Guided Internal Degradation Learning <Br>
**[Author]** Xi Cheng, Zhenyong Fu, Jian Yang <Br>

### MLSR
**[Paper]** (ECCV 2020) Fast Adaptation to Super-Resolution Networks via Meta-Learning <Br>
**[Author]** Xi Cheng, Zhenyong Fu, Jian Yang <Br>
**[[TF-Code](https://github.com/parkseobin/MLSR)]** <Br>
  
  
 # Transfer Restoration
### Syn2Real ★★
**[Paper]**  (CVPR 2020) Syn2Real Transfer Learning for Image Deraining using Gaussian Processes<Br>
**[Author]** [Rajeev Yasarla](https://sites.google.com/view/rajeevyasarla/home), [Vishwanath A. Sindagi](https://www.vishwanathsindagi.com/), [Vishal M. Patel](https://engineering.jhu.edu/ece/faculty/vishal-m-patel/) <Br>
**[[Pytorch-Code](https://github.com/rajeevyasarla/Syn2Real)]**<Br>
使用高斯过程计算无标签真实数据的unsupervised loss. 从paper的实验效果来看有不错的效果, 值得一试
