# c3d
this project implements action recognition algorithm proposed in (C3D: Generic Features for Video Analysis)[https://arxiv.org/pdf/1412.0767v1.pdf] with esimator of Tensorflow

### Introduction

c3d is a convolutional neural network classifying sports video clips. it is widely used as an infrastructure of latter action recognition neural networks.

### how to train

a trained model is provided on baidu cloud at

> https://pan.baidu.com/s/1KmZsUdwxw0E2Nr9DAet7ZQ

if you want to train yourself, you need (UCF101)[http://crcv.ucf.edu/data/UCF101.php] dataset. download it and extract the directory. set the root directory in create_dataset.py. then create a tfrecord format dataset with command

```bash
python create_dataset.py
```

the program will generate a trainset and a testset tfrecord file.

start the training by exeucting 

```base
python train_c3d.py
```

moniter the training process by tensorboard and stop the training when the accuracy reaches 82% which is the best accuracy c3d can reach.
