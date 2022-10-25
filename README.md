
## **Do vision transformers see like convolutional neural networks?**

### Problem 

How do Vision Transformers (ViT) perform image classification tasks? How is it different from the way Convolutional Neural Networks perform image classification?

Goal is to understand the differences between ViTs and CNNs in relation to image tasks. 

### Approach
- Looked at the representation structures of ViTs and CNNs 
- Analyzed use of global and local spatial information
- 

#### Prior research
- explored combining CNNs with self attention
- looked at using local multi headed self attention
- 

### Solution

**Vision Transformers function like transformers do on language processing tasks. ViT's just use self attention to aggregate info instead of using convolution like NNs.**

- Used several ResNet CNNs and ViT models to compare using CKA
  -  Centered Kernal Alignment method to compare similarity across the model layers
- Trained models on the JFT-300M data set

- Found that more ResNet layers were used to complete tasks that ViT models can do using fewer layers

![image](https://user-images.githubusercontent.com/64801054/197649996-377a5da4-7466-4834-a3a7-2423add0561d.png)

- ViT models have more similarity between lower and higher layers than ResNet models

![image](https://user-images.githubusercontent.com/64801054/197417979-e5afa940-8594-4228-8b85-d371a6243f92.png)

### Questions:


### Additional resources

Hugging face ViT information:
https://huggingface.co/docs/transformers/model_doc/vit

GitHub associated with Dosovitsky et al. paper: 
https://github.com/google-research/vision_transformer


### Sources

origninal paper: https://arxiv.org/abs/2108.08810

A. Dosovitskiy, L. Beyer, A. Kolesnikov, D. Weissenborn, X. Zhai, T. Unterthiner, M. Dehghani, M. Minderer, G. Heigold, S. Gelly, et al. An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929, 2020.





