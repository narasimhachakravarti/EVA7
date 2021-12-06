# Final Model

Our best notebook has been uploaded [here](https://github.com/narasimhachakravarti/EVA7/blob/main/Session%209/Session9.ipynb)
We have achieved the test accuracy of 85.74% in 24 Epochs.

Epochs - 24  
LR Scheduler - OneCycleLR

Augnmentation Techniques -

- RandomCrop(32, padding=4)
- Horizontal Flip
- CutOut(8x8)

# Other useful files

Our model can be found [here](https://github.com/narasimhachakravarti/EVA7/blob/main/Session%209/Session9.ipynb)
Our augmentations can be found [here](https://github.com/narasimhachakravarti/EVA7/blob/main/Session%209/Session9.ipynb)
Our maxLR finding file can be found [here](https://github.com/narasimhachakravarti/EVA7/blob/main/Session%209/Session9.ipynb)

## MaxLR

LR suggestion: steepest gradient
Suggested LR: **1.67E-02**

![enter image description here](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/S9_LR.png)

## Logs

The training and testing logs are as follows:
EPOCH: 0
Loss=1.5715450048446655 Batch_id=97 Accuracy=32.01: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0028, Accuracy: 4967/10000 (49.67%)

EPOCH: 1
Loss=1.3423267602920532 Batch_id=97 Accuracy=48.26: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0023, Accuracy: 5901/10000 (59.01%)

EPOCH: 2
Loss=1.234212040901184 Batch_id=97 Accuracy=54.60: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0020, Accuracy: 6480/10000 (64.80%)

EPOCH: 3
Loss=1.0588511228561401 Batch_id=97 Accuracy=59.15: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0018, Accuracy: 6877/10000 (68.77%)

EPOCH: 4
Loss=1.0679857730865479 Batch_id=97 Accuracy=62.24: 100%|██████████| 98/98 [00:56<00:00, 1.72it/s]

Test set: Average loss: 0.0017, Accuracy: 6957/10000 (69.57%)

EPOCH: 5
Loss=0.8818085789680481 Batch_id=97 Accuracy=64.91: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0016, Accuracy: 7234/10000 (72.34%)

EPOCH: 6
Loss=0.9683289527893066 Batch_id=97 Accuracy=66.82: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0014, Accuracy: 7629/10000 (76.29%)

EPOCH: 7
Loss=0.882307767868042 Batch_id=97 Accuracy=69.35: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0013, Accuracy: 7736/10000 (77.36%)

EPOCH: 8
Loss=0.8606860041618347 Batch_id=97 Accuracy=71.06: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0012, Accuracy: 7872/10000 (78.72%)

EPOCH: 9
Loss=0.7854738831520081 Batch_id=97 Accuracy=72.82: 100%|██████████| 98/98 [00:56<00:00, 1.72it/s]

Test set: Average loss: 0.0014, Accuracy: 7689/10000 (76.89%)

EPOCH: 10
Loss=0.7511367201805115 Batch_id=97 Accuracy=73.00: 100%|██████████| 98/98 [00:56<00:00, 1.72it/s]

Test set: Average loss: 0.0012, Accuracy: 7932/10000 (79.32%)

EPOCH: 11
Loss=0.6471362709999084 Batch_id=97 Accuracy=73.77: 100%|██████████| 98/98 [00:56<00:00, 1.72it/s]

Test set: Average loss: 0.0010, Accuracy: 8245/10000 (82.45%)

EPOCH: 12
Loss=0.6964223384857178 Batch_id=97 Accuracy=75.35: 100%|██████████| 98/98 [00:56<00:00, 1.73it/s]

Test set: Average loss: 0.0010, Accuracy: 8224/10000 (82.24%)

EPOCH: 13
Loss=0.6368026733398438 Batch_id=97 Accuracy=74.81: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0010, Accuracy: 8218/10000 (82.18%)

EPOCH: 14
Loss=0.6076942682266235 Batch_id=97 Accuracy=76.54: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0010, Accuracy: 8288/10000 (82.88%)

EPOCH: 15
Loss=0.6427207589149475 Batch_id=97 Accuracy=76.87: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0010, Accuracy: 8387/10000 (83.87%)

EPOCH: 16
Loss=0.6246633529663086 Batch_id=97 Accuracy=77.97: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0010, Accuracy: 8351/10000 (83.51%)

EPOCH: 17
Loss=0.6231288909912109 Batch_id=97 Accuracy=78.99: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0011, Accuracy: 8231/10000 (82.31%)

EPOCH: 18
Loss=0.6124181151390076 Batch_id=97 Accuracy=78.89: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0009, Accuracy: 8479/10000 (84.79%)

EPOCH: 19
Loss=0.5172697305679321 Batch_id=97 Accuracy=79.40: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0009, Accuracy: 8454/10000 (84.54%)

EPOCH: 20
Loss=0.5873700380325317 Batch_id=97 Accuracy=80.50: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0010, Accuracy: 8404/10000 (84.04%)

EPOCH: 21
Loss=0.601722240447998 Batch_id=97 Accuracy=80.50: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0009, Accuracy: 8527/10000 (85.27%)

EPOCH: 22
Loss=0.5876252055168152 Batch_id=97 Accuracy=80.78: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0009, Accuracy: 8535/10000 (85.35%)

EPOCH: 23
Loss=0.47035884857177734 Batch_id=97 Accuracy=81.36: 100%|██████████| 98/98 [00:56<00:00, 1.74it/s]

Test set: Average loss: 0.0009, Accuracy: 8574/10000 (85.74%)

## Plots

Accuracy and Error Plots:

![enter image description here](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/S9_plots.png)

## Misclassified Images

![enter image description here](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/S9_mc.png)

# Our Team

- [Narasimha Chakravarti]
- [Sijuade]
- [Nipon Chanda]
