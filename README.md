# blackbox-attack


### About

Implementations of the blackbox attack algorithms in Pytorch

### Model description 

There are two CNN models: a simple model and C&W model.

Simple Model:

stride = 1, padding = 0

Layer 1: Conv2d 5x5x16, BatchNorm(16), ReLU, Max Pooling 2x2

Layer 2: Conv2d 5x5x32, BatchNorm(32), ReLU, Max Pooling 2x2

Layer 3: FC 10

C&W model:
This can be found in C&W paper their paper for MNIST data. (https://arxiv.org/abs/1608.04644)


### Pre-requisites

The following steps should be sufficient to get these attacks up and running on
most Linux-based systems.

```bash
conda install pytorch torchvision -c pytorch
```
   
#### To run the Pytorch on simple model (python3.6):

```bash
python3 blackbox_attack_mnist_simple.py
```

#### To run the Pytorch on C&W model without GPU:

```bash
python3 blackbox_attack_mnist.py
```

#### To run the Pytorch on C&W model with GPU:

```bash
python3 blackbox_attack_mnist_gpu.py
```


