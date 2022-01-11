# Session 13 Classes

## Class 1

```
class PatchEmbeddings(nn.Module):
Image to Patch Embedding.


    def __init__(self, image_size=224, patch_size=16, num_channels=3, embed_dim=768):
        super().__init__()
        image_size = to_2tuple(image_size)
        patch_size = to_2tuple(patch_size)
        num_patches = (image_size[1] // patch_size[1]) * (image_size[0] // patch_size[0])
        self.image_size = image_size
        self.patch_size = patch_size
        self.num_patches = num_patches

        self.projection = nn.Conv2d(num_channels, embed_dim, kernel_size=patch_size, stride=patch_size)

    def forward(self, pixel_values):
        batch_size, num_channels, height, width = pixel_values.shape
        # FIXME look at relaxing size constraints
        if height != self.image_size[0] or width != self.image_size[1]:
            raise ValueError(
                f"Input image size ({height}*{width}) doesn't match model ({self.image_size[0]}*{self.image_size[1]})."
            )
        x = self.projection(pixel_values).flatten(2).transpose(1, 2)
        return x

```

- Parameters

  - image size
  - Patch size
  - num of channels
  - embed dim

- Convert image size and patch size into tuple

```
def to_2tuple(x):
  if isinstance(x, collections.abc.Iterable):
    return x
  return x, x
```

- Convolution layer

```
nn.Conv2d(num_channels, embed_dim, kernel_size=patch_size, stride=patch_size)

```

We will be getting the shape with batch, embedding and number of patches in the image

Once we flatten the image we will be having embedding dimension and the number pixels in the image say (768 \* 196) in our example

And we will pass to forward function
