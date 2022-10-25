
## **Do vision transformers see like convolutional neural networks?**

### Problem 

How do Vision Transformers (ViT) perform image classification tasks? How is it different from the way Convolutional Neural Networks perform image classification?

Goal is to understand the differences between ViTs and CNNs in relation to image tasks. 

### Approach
- Looked at the representation structures of ViTs and CNNs 
- Analyzed use of global and local spatial information
- 

#### Prior research
- 

### Solution
- Used several ResNet CNNs and ViT models to compare using CKA
  -  Centered Kernal Alignment method to compare similarity across the model layers
- Trained models on the JFT-300M data set

- Found that more ResNet layers were used to complete tasks that ViT models can do using fewer layers

![image](https://user-images.githubusercontent.com/64801054/197649996-377a5da4-7466-4834-a3a7-2423add0561d.png)

- ViT models have more similarity between lower and higher layers than ResNet models

![image](https://user-images.githubusercontent.com/64801054/197417979-e5afa940-8594-4228-8b85-d371a6243f92.png)

### Questions:


### Additional resources


### Sources
