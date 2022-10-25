
## **How do vision transformers work?**

### Problem 

How do Vision Transformers (ViT) work? 

Goal is to understand:
- what parts of multi head self attentions are helpful in optimizing neural networks?
- if multi head self attentions act like convolutional layers, and if not, how are they different?
- how to use both multi head self attentions and convolutional layers to our advantage?

### Approach
- 
- 

#### Prior research
- 
-

### Solution

**Vision Transformers function like transformers do on language processing tasks. ViT's just use self attention to aggregate info instead of using convolution like NNs.**

![image](https://user-images.githubusercontent.com/64801054/197888096-7dd5e6be-e87c-49a6-80e6-1dd071271f56.png)
Dosovitskiy et al. 2020



- Used several ResNet CNNs and ViT models to compare using CKA
  -  Centered Kernal Alignment method to compare similarity across the model layers
- Trained models on the JFT-300M data set

- Found that more ResNet layers were used to complete tasks that ViT models can do using fewer layers

- ViT models have more similarity between lower and higher layers than ResNet models


### Questions:

1. Does any one have any questions?
2. somehting else 

### Additional resources

Hugging face ViT information:
https://huggingface.co/docs/transformers/model_doc/vit

Original Vision Transformer proposal paper: https://arxiv.org/abs/2010.11929
A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.

GitHub associated with Dosovitsky et al. paper: 
https://github.com/google-research/vision_transformer

### Sources

origninal paper: https://arxiv.org/abs/2202.06709v1

A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.





