# ViT

Notebook for ViT [here](https://colab.research.google.com/drive/1yMIhArfET1yKL9zX3ajYBrgM-KfWTshd#scrollTo=r2FCZBftGAa_)

v = ViT(
dim=128,
image_size=224,
patch_size=32,
num_classes=2,
transformer=efficient_transformer,
channels=3,
)

## Parameters

- `image_size`: int.  
  Image size. If you have rectangular images, make sure your image size is the maximum of the width and height
- `patch_size`: int.  
  Number of patches. `image_size` must be divisible by `patch_size`.  
  The number of patches is: `n = (image_size // patch_size) ** 2` and `n` **must be greater than 16**.
- `num_classes`: int.  
  Number of classes to classify.
- `dim`: int.  
  Last dimension of output tensor after linear transformation `nn.Linear(..., dim)`.
- `channels`: int, default `3`.  
  Number of image's channels.

## Data set

os.makedirs('data', exist_ok=True)
train_dir = 'data/train'
test_dir = 'data/test'

## Data sample

![image](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/session13.png)

## Epochs

100%
313/313 [02:38<00:00, 2.26it/s]
Epoch : 1 - loss : 0.6713 - acc: 0.5798 - val_loss : 0.6722 - val_acc: 0.5831

100%
313/313 [02:38<00:00, 2.24it/s]
Epoch : 2 - loss : 0.6600 - acc: 0.5926 - val_loss : 0.6506 - val_acc: 0.6119

100%
313/313 [02:38<00:00, 2.30it/s]
Epoch : 3 - loss : 0.6502 - acc: 0.6085 - val_loss : 0.6517 - val_acc: 0.6019

100%
313/313 [02:38<00:00, 2.28it/s]
Epoch : 4 - loss : 0.6463 - acc: 0.6115 - val_loss : 0.6438 - val_acc: 0.6185

100%
313/313 [02:38<00:00, 2.29it/s]
Epoch : 5 - loss : 0.6420 - acc: 0.6218 - val_loss : 0.6396 - val_acc: 0.6268

100%
313/313 [02:38<00:00, 2.28it/s]
Epoch : 6 - loss : 0.6339 - acc: 0.6305 - val_loss : 0.6262 - val_acc: 0.6383

100%
313/313 [02:38<00:00, 2.32it/s]
Epoch : 7 - loss : 0.6272 - acc: 0.6406 - val_loss : 0.6266 - val_acc: 0.6331

100%
313/313 [02:38<00:00, 2.34it/s]
Epoch : 8 - loss : 0.6231 - acc: 0.6429 - val_loss : 0.6145 - val_acc: 0.6472

100%
313/313 [02:38<00:00, 2.25it/s]
Epoch : 9 - loss : 0.6190 - acc: 0.6461 - val_loss : 0.6371 - val_acc: 0.6145

100%
313/313 [02:38<00:00, 2.27it/s]
Epoch : 10 - loss : 0.6104 - acc: 0.6553 - val_loss : 0.6145 - val_acc: 0.6570

100%
313/313 [02:39<00:00, 2.26it/s]
Epoch : 11 - loss : 0.6071 - acc: 0.6608 - val_loss : 0.6120 - val_acc: 0.6564

100%
313/313 [02:37<00:00, 2.30it/s]
Epoch : 12 - loss : 0.6021 - acc: 0.6663 - val_loss : 0.6007 - val_acc: 0.6744

100%
313/313 [02:36<00:00, 2.31it/s]
Epoch : 13 - loss : 0.5974 - acc: 0.6702 - val_loss : 0.6110 - val_acc: 0.6616

100%
313/313 [02:36<00:00, 2.32it/s]
Epoch : 14 - loss : 0.5966 - acc: 0.6740 - val_loss : 0.5943 - val_acc: 0.6703

100%
313/313 [02:37<00:00, 2.27it/s]
Epoch : 15 - loss : 0.5945 - acc: 0.6769 - val_loss : 0.5906 - val_acc: 0.6770

100%
313/313 [02:37<00:00, 2.28it/s]
Epoch : 16 - loss : 0.5883 - acc: 0.6810 - val_loss : 0.5979 - val_acc: 0.6764

100%
313/313 [02:37<00:00, 2.35it/s]
Epoch : 17 - loss : 0.5870 - acc: 0.6848 - val_loss : 0.5883 - val_acc: 0.6816

100%
313/313 [02:37<00:00, 2.30it/s]
Epoch : 18 - loss : 0.5837 - acc: 0.6816 - val_loss : 0.5862 - val_acc: 0.6839

100%
313/313 [02:37<00:00, 2.30it/s]
Epoch : 19 - loss : 0.5803 - acc: 0.6893 - val_loss : 0.5917 - val_acc: 0.6828

100%
313/313 [02:37<00:00, 2.26it/s]
Epoch : 20 - loss : 0.5828 - acc: 0.6842 - val_loss : 0.5867 - val_acc: 0.6784
