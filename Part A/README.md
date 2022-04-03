**PART A**:  
          Part A contains Three Files they are **Best_model_CNN.ipynb**, **CNN_model.ipynb**, **Guided_backpropagation.ipynb**.

**CNN_model.ipynb**  
File Description: This file contains Preprocessing of the nature12k dataset and Convolutional neural network model along with the wandb sweep configuaration to find the best model.  
**Instructions to run the file:** Open the file in google colab. Change the Wandb project name and entity in wandb.init() function call. And run the file. By changing the sweep config variable parameters we can build the model for different configurations.  
  
**Important Functions in the file**:  

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


****Best_model_CNN.ipynb****:          
File Description: This file contains best configuration of our CNN model, generation of Prediction & original image (10 X 3) grid code along with visualisation code for filters and feature maps.  
**Instructions to run the file:**  Open the file in google colab. Change the Wandb project name and entity in wandb.init() function call. And run the file to get best model accuracy on the test data and 
plot the 10 x 3 grid containing sample images from the test data and predictions made by model 
and visualise all the filters in the first layer of your best model for a random image from the test set. Download the "my_best_model_A.h5" cnn model for future use or to test the guided_backpripagation.ipynb  
  
**Important Functions in the file**:  

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



**Guided_backpropagation.ipynb**  
File Description: This file contains the code for applying guided back propagation on 10 neurons in the CONV5 layer and plot the images which excite this neuron.
**Instructions to run the file:** Open the file in google colab. upload the cnn model you want to perform guided backpropagation or upload the "my_best_model_A.h5" which was generated while running the Best_model_CNN.ipynb file. And run the file to apply guided back propagation on any 10 neurons in the CONV5 layer and plot the images which excite this neuron.  

**Important Functions in the file**:  

**Function name:** **select_random_image**  
**Description  :** selects the random image from the path provided from random class.  
**Arguments    :** path (path of the data set where you want to select the image randomly. This path should contain the classes as folders. By default nature12k data set has this structure)  
**Returns      :** selected image  

**Function name:** **guided_back_propagation**  
**Description :** performs guided back propagation and plots the images that excite the neuron  
**Arguments   :** number_of_neurons,model,image  
**Returns     :** Zero  

| **Variable name** |  **Description**   |
| :------------ | :-----|
| image    | image to perform back propagation            |
| model | cnn model instance |
|number_of_neurons | Number of neurons to see what excite those neurons|
