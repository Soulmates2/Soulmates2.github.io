---
layout: project
title: Score-based Point Cloud Denoising
subtitle: "Reimplement the paper (Deep Learning)"
---
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

**2022 Spring KAIST 3D ML Project**

In this work, we reimplement and reproduce [Score-Based Point Cloud Denoising](https://arxiv.org/abs/2107.10981) (ICCV 2021).

{%
	include image_with_caption.html
	url="/assets/projects/2022_score-based_denoising/main_method.png"
	width="100%"
%}

Score-denoise [1] constructs the model that predicts the score of the distribution,
and performs <b>gradient ascent</b> using the predicted score to denoise the point cloud.
We use the same experimental setup as the original paper.
We use PU-Net [2] dataset for training and testing our model, and PC-Net [3] dataset for testing only. 
We evaluate our model using two metrics: Chamfer distance (CD) [4] and point-to-mesh distance (P2M) [5]. 
Our model shows results that are almost similar to the author’s model, but slightly inferior. 
Especially for unsupervised learning, our model shows a slightly better result than the authors’ model.
In summary, our achievements are:
- We implemented the whole code for original paper with a very basic skeleton code,
- We achieved almost similar but slightly inferior performance compared to the authors’ model.

[Github](https://github.com/Soulmates2/Score-Based-Point-Cloud-Denoising), 
[Report](https://soulmates2.github.io/assets/projects/2022_score-based_denoising/Score_Based_Point_Cloud_Denoising.pdf)
<br/> &nbsp;&nbsp;&nbsp;&nbsp;

**Poster**
{%
	include image_with_caption.html
	url="/assets/projects/2022_score-based_denoising/poster.png"
	width="100%"
%}
<br/> &nbsp;&nbsp;&nbsp;&nbsp;

**References**

[1] Luo Shitong and Hu Wei. [Score-Based Point Cloud Denoising](https://arxiv.org/abs/2107.10981). ICCV 2021.<br/>
[2] Yu Lequan et al. [PU-Net: Point Cloud Upsampling Network](https://arxiv.org/abs/1801.06761). CVPR 2018.<br/>
[3] Rakotosaona Marie-Julie et al. [PointCleanNet: Learning to denoise and remove outliers from dense point clouds](https://arxiv.org/abs/1901.01060). Computer Graphics Forum, 2020.<br/>
[4] Fan Haoqiang et al. [A Point Set Generation Network for 3D Object Reconstruction from a Single Image](https://arxiv.org/abs/1612.00603). arXiv 2016.<br/>
[5] Ravi Nikhila et al. [Accelerating 3D Deep Learning with PyTorch3D](https://arxiv.org/abs/2007.08501). arXiv 2020.