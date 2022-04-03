Part_B folder contains 3 files They are Best_model_partB.ipynb, PartB.ipynb and README.md

**File name :** **PartB.ipynb**  
**File Description :** This program finetune the pre-trained model (vaInceptionV3,ResNet50,InceptionResNetV2,Xception) on the nature12k dataset and runs wandb sweeps  
**Instructions to run the file:** Open the file in google colab. Change the Wandb project name and entity in wandb.init() function call. (replace the wandb credetials with yours). The varible **pre_train_mod** is resposible for seleting the pre trained model to finetune with our data set this variable will be in pretrained_model function.

**Important Functions in the file**:  

**Function Name:** **data**  
**Description :** This function responsible for data preprocessing, augmentation.  
**Arguments :** image_size, augment_data, batch_size.  
**Returns :** train_generator, val_generator, test_generator.  

**Function Name:** **pretrained_model**  
**Description :** This function responsible for loading the pretrained model and modifying the model to use on nature12k dataset  
**Arguments :** image_size,pre_train_mod,dropout,epochs,dense_size,lr  
**Returns :** train_generator, val_generator, test_generator.

| **Variable name** |  **Description**   |
| :------------ | :-----|
| image_size    | Size/dimension of the image           |
|  pre_train_mod| based on this variable value model will load different pretrained model(eg: pre_train_mod =="InceptionV3" this will load InceptionV3 model) value of this variable should be vaInceptionV3,ResNet50,InceptionResNetV2,Xception |
|dropout | dropout rate|
|epochs  | Number of epoches|
|dense_size | ouput size of the dense layer |
|lr | learning rate (eg: 0.001, 0.0001) |

**Function Name: setRunName**
**Description :** This function responsible for creating the run name based on sweep config so that by seeing the runnames we can identify the cofiguration of the sweep.  
**Arguments :** image_size,pre_train_mod, dropout,augment_data,batch_size,dense_size  
**Returns :** run name.  

**Function name : train**  
**Description :** This function contains the config defaluts and the code for building the cnn model. We call this function from wand.agent().  
**Arguments :** None  
**Return :** None  

**File name :** **Best_model_partB.ipynb**  
**File Description :** This program builds/trains the model with best configurations and test the model on test set and logs the accuracy in wandb
**Instructions to run the file:** Open the file in google colab. Replace the Wandb credentials. This file save the CNN model with name "my_best_model.h5".You can evaluate the your/this model with test set by uploading the model in colab and changing the path in load_model() function. (please refer the last cell of this program comments for more information).

**Important Functions in the file**:  

**Function Name:** **data**  
**Description :** This function responsible for data preprocessing, augmentation.  
**Arguments :** image_size, augment_data, batch_size.  
**Returns :** train_generator, val_generator, test_generator.  

**Function Name:** **pretrained_model**  
**Description :** This function responsible for loading the pretrained model and modifying the model to use on nature12k dataset  
**Arguments :** image_size,pre_train_mod,dropout,epochs,dense_size,lr  
**Returns :** train_generator, val_generator, test_generator.

| **Variable name** |  **Description**   |
| :------------ | :-----|
| image_size    | Size/dimension of the image           |
|  pre_train_mod| based on this variable value model will load different pretrained model(eg: pre_train_mod =="InceptionV3" this will load InceptionV3 model) value of this variable should be vaInceptionV3,ResNet50,InceptionResNetV2,Xception |
|dropout | dropout rate|
|epochs  | Number of epoches|
|dense_size | ouput size of the dense layer |
|lr | learning rate (eg: 0.001, 0.0001) |

**File Name** : **README.md**  
**Description :** Contains the information about the files of Part_B 
