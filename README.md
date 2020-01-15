# Fashion Mnist TensorFlow JS Classifier 

This repository contains a Convolutional Neural Network build with TensorFlow JS that trains on the [Fashion Mnist sprited dataset](https://storage.googleapis.com/learnjs-data/model-builder/fashion_mnist_images.png) and allow user to draw images to predict, all this running on the Chrome Web Browser.  

## Setting up  

In order to the model runs properly you need to download [Google Chrome](https://www.google.pt/intl/pt-PT/chrome/?brand=CHBD&gclid=EAIaIQobChMIv-vZmImG5wIVBA6RCh3kWQNmEAAYASAAEgKDmvD_BwE&gclsrc=aw.ds) and install the [Web Server for Chrome extension](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb). 

## Running

1. [Fork and clone](https://guides.github.com/activities/forking/) this repository.

2. Open the **Web Server for Chrome** extension. You can do so by accessing the `chrome://apps` url in the Chrome search bar. 

3. Click the **"Open Folder"** button, select and open the directory to where you cloned this repository. 

4. Click the generated **Web Server URL**. It will display for you the files of the directory. 

5. Click the `index.html` file and the application will automatically load and train. 

6. When training is done you will be able to draw in the black canvas to make predictions. 

## Model 

### Architecture 

```
_________________________________________________________________ 
Layer (type)                 Output shape              Param #   
================================================================= 
conv2d_Conv2D1 (Conv2D)      [null,26,26,16]           160       
_________________________________________________________________ 
max_pooling2d_MaxPooling2D1  [null,13,13,16]           0         
_________________________________________________________________ 
conv2d_Conv2D2 (Conv2D)      [null,11,11,64]           9280      
_________________________________________________________________ 
max_pooling2d_MaxPooling2D2  [null,5,5,64]             0         
_________________________________________________________________ 
flatten_Flatten1 (Flatten)   [null,1600]               0         
_________________________________________________________________ 
dense_Dense1 (Dense)         [null,128]                204928    
_________________________________________________________________ 
dense_Dense2 (Dense)         [null,10]                 1290      
================================================================= 
Total params: 215658 
Trainable params: 215658 
Non-trainable params: 0
``` 

### Data: 

* **Dataset total size:** 70000 
* **Dataset used size:** 7000 (10%) 
* **Training data size:** 6000 
* **Testing data size:** 1000 


### Training 

* **Epochs:** 20 
* **Batch size:** 128 
* **Optimizer:** Adam 
* **Loss function:** Categorical Crossentropy . 