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
  

### 2. Semi-supervised GAN (SGAN)

#### Aim - To solve the problem of class imbalance by generating images using SGAN

a) Make sure to have installed keras library

b) Execute the code in the same order as given or else there might be some error- 'img GAN.ipynb'

c) First, the Fashion-mnist dataset is loaded from keras library and the testing and training datasets are combined, and they are reshaped and converted into float32 datatype.

![image](https://user-images.githubusercontent.com/66245321/147775926-93af2a1e-e700-4ece-8488-2577097860fd.png)


d) Since Fashion-mnist is a perfectly balanced dataset with 7000 samples per class, it’ll be made imbalanced by taking only 869 samples for classes 0,4 and 8 each.

e) After this KNN model is built on the processed dataset.

f) Then the Semi-supervised GAN - SGAN is built

g) In the summarise_performance() function the already built KNN model will be used as a criteria to add generated samples in the imbalanced dataset.

h) Then a Decision tree model will be built on the balanced dataset and the accuracy and the no.of misclassified samples are noted.



### 3. SMOTE (To compare the efficiency of SGAN wrt SMOTE)

#### Aim - Training a SMOTE just to check if SGAN performs better than other synthetic image generating models

a) Similarly, the same pre-processing(combining testing and training datasets, reshaping the dataset to 2D dataset and converting the pixels into float32 datatype and bringing them into the range [-1,1] )is done for SMOTE- 'SMOTE.ipynb'

b) The SMOTE model is built and the imbalanced dataset is made balanced

c) Then a Decision tree model will be built on the balanced dataset and the accuracy and the no.of misclassified samples are noted.
