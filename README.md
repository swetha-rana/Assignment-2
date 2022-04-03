# Assignment-2
Part A contains the Part A of Assignment.  
Part B contains the part B of Assignmnet.  

**PART A**:
          Part A contains Three Files they are **Best_model_CNN.ipynb**, **CNN_model.ipynb**, **Guided_backpropagation.ipynb**.

**CNN_model.ipynb**
File Description: This file contains Preprocessing of the nature12k dataset and Convolutional neural network model along with the wandb sweep configuaration to find the best model.  

****Best_model_CNN.ipynb****:          
File Description: This file contains best configuration of our CNN model, generation of Prediction & original image (10 X 3) grid code along with visualisation code for filters and feature maps.  
               
**Guided_backpropagation.ipynb**
File Description: This file contains the code for applying guided back propagation on 10 neurons in the CONV5 layer and plot the images which excite this neuron.

**Important Functions**:

**Function Name:** **data**  
**Description :** This function responsible for data preprocessing, augmentation.  
**Arguments :** image_size, augment_data, batch_size.  
**Returns :** train_generator, val_generator, test_generator.  


| **Variable name** |  **Description**   |
| :------------ | :-----|
| image_size    | Size/dimension of the image           |
| naugment_data | True or Flase if True data augmentation performed else won't |
|batch_size | batch size for training (eg: 32,100)|


**Function Name:** **CNN_model**
**Description :** This function contains the CNN model and this function responsible creates the required convolutional neural network.  
**Arguments :** image_size,kernel_size,num_filters,filter_org,dropout,batch_norm,epochs,dense_size,lr.  
**Returns :** train_generator, val_generator, test_generator.  

| **Variable name** |  **Description**   |
| :------------ | :-----|
| image_size    | Size/dimension of the image           |
| num_filters | number of filters (eg: 32,64)|
|kernel_size | Filter size (eg: 3 × 3)|
| filter_org | Filter organisation (eg: same number of filters in each layer , doubling / halving in each subsequent layer) |
|dropout | drop out rate for dropout layer|
|batch_norm | for adding batch normalisation True, else Flase|
|epochs | Number of Epoches (eg:5,10)|
|dense_size | output Size of the dense layer|
|lr | learning rate (eg: 0.001,0.0001)|
