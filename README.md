# [Real-time Facial Expression Recognition ``In The Wild'' by Disentangling 3D Expression from Identity](https://arxiv.org/abs/2005.05509):
[![Youtube Video](https://img.shields.io/badge/HD%20Video-Results-lightgrey?logo=youtube)](https://youtu.be/Gnkw6TY5ZuU)
[![arXiv Prepring](https://img.shields.io/badge/arXiv-Preprint-lightgrey?logo=arxiv)](https://arxiv.org/abs/2005.05509)

This is the official repository of our FG 2020 paper FER in-the-wild.

[Mohammad Rami Koujan](https://github.com/mrkoujan)<sup> 1</sup>,
[Luma Alharbawee](https://www.researchgate.net/profile/Luma_Alharbawee)<sup> 1</sup>,
[Giorgos Giannakakis](https://projects.ics.forth.gr/cbml/index_main.php?l=e&c=689)<sup> 2</sup>,
[Nicolas Pugeault](http://empslocal.ex.ac.uk/people/staff/np331/)<sup> 1</sup>,
[Anastasios Roussos](http://users.ics.forth.gr/~troussos/)<sup> 1,2</sup>
<br/>
<sup>1 </sup>University of Exeter
<br/>
<sup>2 </sup>Foundation for Research and Technology - Hellas (FORTH), Greece


[[Preprint]](https://arxiv.org/pdf/2005.05509.pdf)
__[FG 2020]__

### Abstract 

Human emotions analysis has been the focus of many studies, especially in the field of Affective Computing, and is important for many applications, e.g. human-computer
intelligent interaction, stress analysis, interactive games, animations, etc. Solutions for automatic emotion analysis have also benefited from the development of deep learning approaches and 
the availability of vast amount of visual facial data on the internet. This paper proposes a novel method for human emotion recognition from a single RGB image. We construct a large-scale dataset of facial videos (\textbf{FaceVid}), rich in facial dynamics, identities, expressions, appearance and 3D pose variations. We use this dataset to train a deep Convolutional Neural Network for estimating expression parameters of a 3D Morphable Model and combine it with an effective back-end emotion classifier. Our proposed framework runs at 50 frames per second and is capable of 
robustly estimating parameters of 3D expression variation and accurately recognizing facial expressions from in-the-wild images.

### Proposed Framework

![Framework Image](images/pipeline.jpg "framework image")

The figure above demonstrates an overview of the proposed framework. Motivated by the progress in the 3D facial reconstruction from images and the rich dynamic information accompanying videos of facial performances, we collected a large-scale dataset of facial videos from the internet and recovered the per-frame 3D geometry thereof with the aid of 3D Morphable Models (3DMMs) of identity and expression. The annotated dataset was used to train the proposed DeepExp3D network, in a supervised manner for regressing the expression coefficients vector e_f from a single input image I_f. As a final step, a classifier was added to the output of the DeepExp3D to predict the emotion of each estimated facial expression, and was trained and tested on standard benchmarks for FER, please see the paper for more details. 


### Citation
If you find our work useful, please cite it as follows:
```
@article{koujan2020real,
  title={Real-time Facial Expression Recognition" In The Wild''by Disentangling 3D Expression from Identity},
  author={Koujan, Mohammad Rami and Alharbawee, Luma and Giannakakis, Giorgos and Pugeault, Nicolas and Roussos, Anastasios},
  journal={arXiv preprint arXiv:2005.05509},
  year={2020}
}
```
