# **SPATIAL TRANSFORMER NETWORKS**

https://colab.research.google.com/drive/1dJNab8v6YVTOtYaVUjTVQA1tJxE_5vje

Spatial transformer networks are a generalization of differentiable attention to any spatial transformation. Spatial transformer networks (STN for short) allow a neural network to learn how to perform spatial transformations on the input image in order to enhance the geometric invariance of the model. For example, it can crop a region of interest, scale and correct the orientation of an image. It can be a useful mechanism because CNNs are not invariant to rotation and scale and more general affine transformations.

# **DEPICTING SPATIAL TRANSFORMER NETWORKS**

Spatial transformer networks boils down to three main components :

The localization network is a regular CNN which regresses the transformation parameters. The transformation is never learned explicitly from this dataset, instead the network learns automatically the spatial transformations that enhances the global accuracy.
The grid generator generates a grid of coordinates in the input image corresponding to each pixel from the output image.
The sampler uses the parameters of the transformation and applies it to the input image.

Test set: Average loss: 0.2254, Accuracy: 9388/10000 (94%)

Train Epoch: 2 [0/60000 (0%)] Loss: 0.408567
Train Epoch: 2 [32000/60000 (53%)] Loss: 0.371109

Test set: Average loss: 0.1318, Accuracy: 9601/10000 (96%)

Train Epoch: 3 [0/60000 (0%)] Loss: 0.319617
Train Epoch: 3 [32000/60000 (53%)] Loss: 0.474289

Test set: Average loss: 0.0986, Accuracy: 9711/10000 (97%)

Train Epoch: 4 [0/60000 (0%)] Loss: 0.144975
Train Epoch: 4 [32000/60000 (53%)] Loss: 0.398601

Test set: Average loss: 0.0791, Accuracy: 9768/10000 (98%)

Train Epoch: 5 [0/60000 (0%)] Loss: 0.156424
Train Epoch: 5 [32000/60000 (53%)] Loss: 0.075312

Test set: Average loss: 0.0696, Accuracy: 9794/10000 (98%)

Train Epoch: 6 [0/60000 (0%)] Loss: 0.133182
Train Epoch: 6 [32000/60000 (53%)] Loss: 0.129236

Test set: Average loss: 0.0711, Accuracy: 9765/10000 (98%)

Train Epoch: 7 [0/60000 (0%)] Loss: 0.088904
Train Epoch: 7 [32000/60000 (53%)] Loss: 0.049734

Test set: Average loss: 0.0770, Accuracy: 9767/10000 (98%)

Train Epoch: 8 [0/60000 (0%)] Loss: 0.191267
Train Epoch: 8 [32000/60000 (53%)] Loss: 0.092480

Test set: Average loss: 0.0587, Accuracy: 9811/10000 (98%)

Train Epoch: 9 [0/60000 (0%)] Loss: 0.129291
Train Epoch: 9 [32000/60000 (53%)] Loss: 0.186961

Test set: Average loss: 0.0618, Accuracy: 9819/10000 (98%)

Train Epoch: 10 [0/60000 (0%)] Loss: 0.050753
Train Epoch: 10 [32000/60000 (53%)] Loss: 0.089486

Test set: Average loss: 0.0495, Accuracy: 9848/10000 (98%)

Train Epoch: 11 [0/60000 (0%)] Loss: 0.261527
Train Epoch: 11 [32000/60000 (53%)] Loss: 0.067389

Test set: Average loss: 0.0457, Accuracy: 9859/10000 (99%)

Train Epoch: 12 [0/60000 (0%)] Loss: 0.066120
Train Epoch: 12 [32000/60000 (53%)] Loss: 0.044939

Test set: Average loss: 0.0484, Accuracy: 9849/10000 (98%)

Train Epoch: 13 [0/60000 (0%)] Loss: 0.047848
Train Epoch: 13 [32000/60000 (53%)] Loss: 0.061977

Test set: Average loss: 0.0431, Accuracy: 9873/10000 (99%)

Train Epoch: 14 [0/60000 (0%)] Loss: 0.012124
Train Epoch: 14 [32000/60000 (53%)] Loss: 0.058582

Test set: Average loss: 0.0419, Accuracy: 9877/10000 (99%)

Train Epoch: 15 [0/60000 (0%)] Loss: 0.051523
Train Epoch: 15 [32000/60000 (53%)] Loss: 0.091980

Test set: Average loss: 0.0653, Accuracy: 9815/10000 (98%)

Train Epoch: 16 [0/60000 (0%)] Loss: 0.072367
Train Epoch: 16 [32000/60000 (53%)] Loss: 0.049061

Test set: Average loss: 0.0461, Accuracy: 9876/10000 (99%)

Train Epoch: 17 [0/60000 (0%)] Loss: 0.117845
Train Epoch: 17 [32000/60000 (53%)] Loss: 0.123637

Test set: Average loss: 0.0435, Accuracy: 9873/10000 (99%)

Train Epoch: 18 [0/60000 (0%)] Loss: 0.256316
Train Epoch: 18 [32000/60000 (53%)] Loss: 0.109639

Test set: Average loss: 0.0420, Accuracy: 9873/10000 (99%)

Train Epoch: 19 [0/60000 (0%)] Loss: 0.026842
Train Epoch: 19 [32000/60000 (53%)] Loss: 0.123915

Test set: Average loss: 0.0463, Accuracy: 9867/10000 (99%)

Train Epoch: 20 [0/60000 (0%)] Loss: 0.127273
Train Epoch: 20 [32000/60000 (53%)] Loss: 0.105095

Test set: Average loss: 0.0385, Accuracy: 9886/10000 (99%)

[![image.png](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/s12.png)](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/s12.png)
