# Concrete-Crack-Segmentation

This is a two-phase project where the improvement has been made upon the implementation of U-Net in phase 1.

## Phase 1 - Implementation of U-Net for Concrete Crack Segmentation

### Introduction

U-Net is a convolutional neural network (CNN) architecture specifically designed for image segmentation, particularly in biomedical imaging [1], though it’s now widely used in other domains. Considering its capability of identifying image paterns, it has also been implemented for Concrete Crack Segmentation [2, 3, 4, 5, 6].

<img width="1050" height="407" alt="image" src="https://github.com/user-attachments/assets/507e5384-20fb-4c01-8819-987f554b8b19" />

_U-Net Architecture_

### Dataset

With the masked image set provided by Eric Bianchi and Matthew Hebdon [7], we can train our own network and perform further analysis upon the result. 

<img width="960" height="240" alt="image" src="https://github.com/user-attachments/assets/03e314d1-f3b9-4ff7-8bcb-eac24a04cc40" /> 

_Masked Image_

### Training

Please note that the dataset includes two subsets: CFD, and Crack 500, we created the training set and trained the Phase 1 network on both of them, and tested the trained result with images outside of the training set. The network setup and training can be found in 'Traditional U-Net.ipynb'.

<img width="1089" height="403" alt="image" src="https://github.com/user-attachments/assets/b8d908f8-97c0-47cd-90ae-20b1fedb8aa2" />

### Testing

_Testing Result of Network Trained on Both Subsets_

The network is capable to deliver result in accuracy.

## Phase 2 - Improvement of U-Net on Shallow Crack Segmentation

### Introduction

A question has risen while testing the network with dataset: 

**The accuracy of result is highly depend on the similarity between the training set and testing set, is that possible to have a network trained on one dataset (with similar pattern) and still be capable to segment crack on another dataset (with different patterns)?**

<img width="580" height="407" alt="image" src="https://github.com/user-attachments/assets/9b9a3681-7c81-4402-b3ca-ca6d2530200d" />

_Testing Result If Trained on Crack 500 and Tested on CFD_

To answer the question, we need to understand what patterns 

## Abstract
Comparison between Traditional U-Net and Inception U-Net while training on biased dataset. For the detailed instruction, please view Instruction.ppt.
### Result with U-Net
![image](https://github.com/TensorYue/Concrete-Crack-Segmentation/assets/112973740/c3e10175-2e13-48d4-af7c-ed818044adc6)
### Restul with Inception U-Net
![image](https://github.com/TensorYue/Concrete-Crack-Segmentation/assets/112973740/2fe61ed0-54c1-41d2-9c90-0ff08cdcb88d)


## References

[1]	O. Ronneberger, P. Fischer, T. Brox (2015) U-net: Convolutional networks for biomedical image segmentation, International Conference on Medical Image Computing and Computer-assisted Intervention, https://doi.org/10.1007/978-3-319-24574-4_28 Munich, Germany.

[2]	Zhenqing Liu, Yiwen Cao, Yize Wang, Wei Wang  (2019) Computer vision-based concrete crack detection using U-net fully convolutional networks, Automation in Construction, 104 129-139, https://doi.org/10.1016/j.autcon.2019.04.005

[3]	F. Chen, M. Jahanshahi  (2018) NB-CNN: deep learning-based crack detection using convolutional neural network and Naïve Bayes data fusion, IEEE Trans. Ind. Electron. 65 4392–4400, https://doi.org/10.1109/TIE.2017.2764844

[4]	R. Li, Y. Yuan, W. Zhang, Y. Yuan (2018) Unified vision-based methodology for simultaneous concrete defect detection and geolocalization, Comput. Aided Civ. Inf. Eng. 33 527–544, https://doi.org/10.1111/mice.12351

[5]	Y. Cha, W. Choi, O. Büyüköztürk (2017) Deep learning-based crack damage detection using convolutional neural networks, Comput. Aided Civ. Inf. Eng. 32 361–378, https://doi.org/10.1111/mice.12263

[6]	C. Dung, L. Anh (2019) Autonomous concrete crack detection using deep fully convolutional neural network, Autom. Constr. 99 52–58, https://doi.org/10.1016/j.autcon.2018.11.028

[7]	Eric Bianchi, Matthew Hebdon (2021) Concrete Crack Conglomerate Dataset https://doi.org/10.7294/16628596

[8]	Cheng, D., & Lam, E. Y. (2021) Transfer learning U-Net deep learning for lung ultrasound segmentation. arXiv preprint arXiv:2110.02196

[9]	Christian Szegedy, Wei Liu, Yangqing Jia, Pierre Sermanet, Scott Reed, Dragomir Anguelov, Dumitru Erhan, Vincent Vanhoucke, Andrew Rabinovich (2015) Going deeper with convolutions, IEEE Conference on Computer Vision and Pattern Recognition (CVPR),  https://doi.org/10.48550/arXiv.1409.4842 Boston, USA
