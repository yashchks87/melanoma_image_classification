# Dog and cats image classification
Convolutional neural networks using DNN to classify images between dogs and cats

## Project brief
Hello world of computer vision dataset of Dogs and Cats image is used to perform. Dataset was taken from Kaggle. Supervised computer vision problem; used DNN models to train model. 

### Dataset Description
Dataset contains more than 25000 training and 12500 test image dataset. Which contains primarily Dogs and Cats as images. Target variable is defined as 1 = Dog and 0 = Cat.

## Project flow
* Data processing was handeled by some list of python libraries such as Glob for gettting all image files. Heavy emphasis on Tensorflow dataset API for preparing dataset for Neural netowrk. Data collected and then created user defined functions.
* Created different visualizations which can able to support the claim made on dataset and which can be identified as fact from visualizations.
* Dataset has many different images with different dimensions such as 1024x1024, 64x64 and many other image dimensions. Due to that neural network can't accept different dimenstion image so fixed dimension image was taken as 64x64. **The reason for this is that as we increase dimension size it starts overfitting data. And reducing than this creates underfit.**
* Kept all channels data which is RGB 3 channels data. Used tensorflow string class to make sure to fetch class label. 
* As whole model is implemented with GPU different charactics like Autotune and ignore order. As wee divide tasks of data preparation performs on CPU while neural network training happens on GPU. So ignore order hypeerparameter will help us to prepare data faster so CPU don't wait for data to come in sequence. It will start to act immediately which ever data it gets.
* While number of files in each batch is 512 images. 
* As model is creeated as very complex with many layers there is always scope of overfitting and it overfitted. So I implemented model with dropout points which can able to reduce overfitting, and I succedded too in reduce overfitting. 
* Total number of epochs projected was 70 but we used early stopping criteria model stopped at 57th epoch and on every eepoch 100 batches of data has been used.
* All above mentioned hyperparameter is taken after training with many different tuning of hyperparameters. 
* **Final accuracy for training data: 90.13 and Validation Data: 90.73**

## Data visualization
* **Number of examples of each class**
![Class Distribution](./Class distribution.png)


## Built with
* Python
* Matplotlib
* Seaborn
* Pandas
* Tensorflow
* Keras
* GPU implementation
* CV2

## Authors
* [Yash Choksi](https://www.linkedin.com/in/choksiyash/)

## Acknowledgements
* [Data set URL](https://www.kaggle.com/c/quora-insincere-questions-classification)
* [Book referred](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291)
