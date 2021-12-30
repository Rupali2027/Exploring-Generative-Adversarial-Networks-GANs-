## Exploring-Generative-Adversarial-Networks


### 1. StackGan

#### Aim - Text to Image translation using StackGAN

##### Setup - 
a) Download the CUB_200_2011 dataset (bird dataset).
####  Number of categories: 200
####  Number of images: 11,788
####  Eg - 
  ![image](https://user-images.githubusercontent.com/66245321/147774362-249d02ee-cf5c-465f-b3ed-3235174e8c87.png)

b) Download the birds dataset (contains the word to vec embeddings of the text descriptions of every bird in the 200 categories)

c) Then run Text2Image_StackGAN.py file in the jupyter notebook.
        It conatins both the stage1 and stage2 generator and discriminator functions 
   
   Make folders - weights, test, stage2_results which will store the stage1's weights obtained while training the generator, stage1's generator output images which are of low resolution and the stage2 generator image high resolution images respectively.
  
