# Fine Grain Classification : Connecting Meta using Cross-Contrastive pre-training

# Presented by
yt2188@nyu.edu – Yash Thesia
sm9669@nyu.edu – Sumit Mamtani
# Abstract

Fine-grained visual classification aims to recognize the objects belonging to multiple subordinate categories of a super-category. However, this is a challenging problem as appearance information alone is often not sufficient to accurately differentiate between fine-grained visual categories. This motivates us to propose a novel and unified framework to utilize  meta-information to assist in fine-grained identification and address the joint learning of vision and various meta-information using cross contrastive pre-training. In the first step, we used three encoders for image , text and meta information and try to align the projected embeddings for better representation. Then we fine-tuned the image and meta encoder for the classification task. Experiments on the NABird dataset show that our Framework can effectively use meta-information to improve the performance of fine-grained recognition. Adding meta-information in NABird, our Framework can exceed the current Baseline by 7.83\%. Moreover, Our Framework can achieve 84.44\% on the NABirds dataset, which outperforms many of existing SotA approaches with meta information.

## Results
|                   | Accuracy on test set | 
|-------------------|------------------|
| InceptionV3       | 76.61%           | 
| InceptionV3 + Meta      | 77.56%            | 
| InceptionV3 + Contrastive learning      | 79.84%           | 
| CLIP       | 81.66%            | 
| Geoprior       | 81.50%            | 
| Ours       | 84.44%            | 

- Results and Comparisons (All the models were trained for only 200 epochs; increasing the number of epochs for training may increase the resultant the performance)

## Proposed Model - Pre-training using Cross-Contrastive loss with Meta information
![Model Architecture](figures/atten_Unet_GAN.png)

## Proposed Model - Pre-training using Cross-Contrastive loss with Meta information
![Model Architecture](figures/atten_Unet_GAN.png)

## Model visual Output: location embedding and Heat-map for European Starling bird
![Denoise a random image in original dataset](figures/results.png)


## Requirements
- 128GB RAM
- Pytorch 1.0
- Numpy + Rawpy
- Matplotlib
- GPU : Nvidia RTX1800

## References 

- [1] https://github.com/huyvnphan/Learning_To_See_In_The_Dark
- [2] https://github.com/LeeJunHyun/Image_Segmentation
- [3] https://github.com/ozan-oktay/Attention-Gated-Networks
- [4] https://github.com/aladdinpersson/Machine-Learning-Collection/tree/master/ML/Pytorch/GANs
- [6] Isola, P., Zhu, J. Y., Zhou, T., & Efros, A. A. (2017). Image-to-image translation with conditional adversarial networks. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 1125-1134).
- [7] Chen Chen, Qifeng Chen, Jia Xu, and Vladlen Koltun. Learning to see in the dark. 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition, pages 3291–3300, 2018. 2, 3, 4
