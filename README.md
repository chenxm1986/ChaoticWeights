Chaotic Weights
============

This code is a simple demonstration of how to protect the weights of a neural network running on an accelerator like GPU and NPU. The basic principle is to change the positions of the weights by an chaotic algorithm named Arnold's cat map.

This python code is a simple demonstration for the method proposed in the following paper. It is just for a function demonstration but the performance is not optimized. The latency of encryption (decryption) can be shortened by implementing the Arnold's cat map algorithm in C/C++ or CUDA.

Ning Lin, Xiaoming Chen, Hang Lu, Xiaowei Li, Chaotic Weights: A Novel Approach to Protect Intellectual Property of Deep Neural Networks, IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (IEEE TCAD), vol. 40, no. 7, pp. 1327-1339, July, 2021.

Requirements
============
Python 3.6(3.7) and PyTorch (torch==1.1.0 and torchvision==0.3.0). Please see requirements.txt for details.

Usage Example
===========
```
cd ChaoticWeights
pip install virtualenv
# Create a virtual environment
virtualenv -p python3 env
source .env/bin/activate
pip install -r requirements.txt
jupyter notebook

## An image encryted by ACM
Toy_ACM.ipynb 

## AlexNet encrypted by ACM encryption. You can try different secret keys, encryption range or layers by adjusting the relevant code.
Imagenet-Toy.ipynb

## VGG and ResNet examples
ImageNet-VGG16.ipynb
ImageNet-ResNet18.ipynb
```

Code Author
============
[Ning Lin](mailto:1586948927@qq.com), the first author of the above paper.
