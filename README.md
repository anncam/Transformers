
# *How do vision transformers work?*

## Problem 

How do Vision Transformers (ViT) work? 

## Approach

The authors explored:
1. what parts of multi head self attentions are helpful in optimizing neural networks?
2. if multi head self attentions act like convolutional layers, and if not, how are they different?
3. how to use both multi head self attentions and convolutional layers to our advantage?

### Prior research
- 
-

## Solution

**Vision Transformers function like transformers do on language processing tasks. ViT's just use self attention to aggregate info instead of using convolution like NNs.**

![image](https://user-images.githubusercontent.com/64801054/197888096-7dd5e6be-e87c-49a6-80e6-1dd071271f56.png)
Dosovitskiy et al. 2020

![image](https://user-images.githubusercontent.com/64801054/197893010-652a33a2-9de8-4873-8af5-afbf0cf17e24.png)


Background: 
- used vanilla ViT (Dosovitskiy et al., 2021), PiT (Heo et al., 2021), which is “ViT + multi-stage”, and Swin (Liu et al., 2021), which is “ViT + multi-stage + local MSA”.


![image](https://user-images.githubusercontent.com/64801054/197897709-cf550253-031d-4742-8e2d-7039804a98f8.png)

Proposed ***AlterNet*** model
- combines ViT and CNNs by changing ratio of multi head self attentions to convolutional layers which ended up outperforming CNNs and ViTs


## Questions:

1. Does any one have any questions?
2. somehting else 

## Additional resources

Hugging face ViT information:
https://huggingface.co/docs/transformers/model_doc/vit

Original Vision Transformer proposal paper: https://arxiv.org/abs/2010.11929
A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.

GitHub associated with Dosovitsky et al. paper: 
https://github.com/google-research/vision_transformer

## Sources

origninal paper: https://arxiv.org/abs/2202.06709v1

A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.





