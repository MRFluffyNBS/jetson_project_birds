# Bird ID

Have you ever seen a bird outside and wanted to identify what species it is? This project uses machine learning using the Jetson Nano to train on a database of 10 species of birds and correctly identify them from a camera or photo. 

![birb](https://imgur.com/BQudbqA)

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
3. Next, change directories to jetson-inference/python/training/classification/models and run these commands:
```
mkdir models
cd models
wget https://www.dropbox.com/s/sy0xgzaln60l7ys/resnet18.onnx
```
You are all set to classify images! Return back to jetson-inference/python/training/classification
4. Download [this image](https://imgur.com/fnHoCtz) to jetson-inference/python/training/classification. **Make sure its renamed to blackbird.jpg!**
5. Input this code into the terminal 
```
imagenet.py --model=models/birds/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/birds/labels.txt blackbird.jpg blackbirdresult.jpg
```
6. [Congrats!](https://imgur.com/mFMUxan)
7. 

[View a video explanation here](video link)
