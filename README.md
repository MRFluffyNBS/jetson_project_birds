# Bird ID

Have you ever seen a bird outside and wanted to identify what species it is? This project uses machine learning using the Jetson Nano to train on a database of 10 species of birds and correctly identify them from a camera or photo. 

![add image descrition here](direct image link here)

## The Algorithm

This project employs transfer learning by retraining the Resnet-18 network on a dataset of images to correctly identify the species of birds. The trained model is then exported in onnx format and processed with TensorRT using imagenet.py. 

## Running this project

1. cd to jetson-inference/python/training/classification/data
2. Download [the bird dataset](https://www.dropbox.com/s/0cafb7h48kal5ae/birds.tar.gz?dl=0) by running
```
wget https://www.dropbox.com/s/0cafb7h48kal5ae/birds.tar.gz
```
4. Use this command to unzip the file: 
```
tar xvzf birds.tar.gz
```
3. Next, change directories to jetson-inference/python/training/classification/models and run this command


[View a video explanation here](video link)
