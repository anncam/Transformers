
# *How do vision transformers work?*

## Problem 

How do Vision Transformers (ViTs) work and what role does multi head self attention play in ViT models? 

## Approach

The authors explored:
1. what parts of multi head self attentions are helpful in optimizing neural networks?
2. if multi head self attentions act like convolutional layers, and if not, how are they different?
3. how to use both multi head self attentions and convolutional layers to our advantage?


## Solution

**Vision Transformers function like transformers do on language processing tasks. ViT's just use self attention to aggregate information instead of using convolution like CNNs.**

![image](https://user-images.githubusercontent.com/64801054/197888096-7dd5e6be-e87c-49a6-80e6-1dd071271f56.png)
Dosovitskiy et al. 2020

1. images are split into "patches" which act as sequence tokens in this case
2. patches are flattened
3. get linear embedding from patches
4. add positional embeddings to the patches
5. feed into a transformer encoder
6. pretrain using labeled images
7. finetune model later for image classification

**Models used in experiment:**
- vanilla ViT
- PiT (which is “ViT + multi-stage”) 
- Swin (which is “ViT + multi-stage + local MSA")
- ResNet 

![image](https://user-images.githubusercontent.com/64801054/197905222-4ba2c073-f018-407b-aa5a-c556744b6566.png)

- ViT models show more similarity between higher and lower layers
- multi head self attentions aggregate feature maps while convolutional layers diversify them
- multi head self attentions improve model accuracy and robustness

![image](https://user-images.githubusercontent.com/64801054/197897709-cf550253-031d-4742-8e2d-7039804a98f8.png)

Proposed ***AlterNet*** model to incorporate the advantages of ViT and CNN models: 
- Combines ViT and CNNs by changing ratio of multi head self attentions to convolutional layers 
- Ended up outperforming CNNs and ViTs even on very small data sets

## ViT Example code:
https://github.com/anncam/Transformers/blob/main/ViT_example.ipynb

### Analysis: 

My only issue with this paper is that I don't feel like the title really matches the content. The title gives the impression that the paper is going to focus on the basics of how Vision Transformers work, which it did some what, but it also focused on proposing a new model. The authors could have added more information on vision transformers in general to supplement their AlterNet model idea. 

## Questions:

1. How do you think that global and local spatial location informaiton would play a role in how a vision transformers performs?  
2. 
3. Does anyone have any other questions? 


## Additional resources

Overview of how ViTs work: 
https://theaisummer.com/vision-transformer/

GitHub ViT example code:
https://github.com/The-AI-Summer/self-attention-cv

Hugging face ViT information:
https://huggingface.co/docs/transformers/model_doc/vit

Original Vision Transformer proposal paper: https://arxiv.org/abs/2010.11929
A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.

GitHub associated with Dosovitsky et al. paper: 
https://github.com/google-research/vision_transformer

## Sources

origninal paper: https://arxiv.org/abs/2202.06709v1

A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.

Kaggle CiFar1o ViT example:
https://www.kaggle.com/code/lonnieqin/cifar10-classification-vision-transformer/notebook

