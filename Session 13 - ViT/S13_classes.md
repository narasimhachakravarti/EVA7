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

## Class 2

```
class ViTEmbeddings(nn.Module):

    def __init__(self, config):
        super().__init__()

        self.cls_token = nn.Parameter(torch.zeros(1, 1, config.hidden_size))
        self.patch_embeddings = PatchEmbeddings(
            image_size=config.image_size,
            patch_size=config.patch_size,
            num_channels=config.num_channels,
            embed_dim=config.hidden_size,
        )
        num_patches = self.patch_embeddings.num_patches
        self.position_embeddings = nn.Parameter(torch.zeros(1, num_patches + 1, config.hidden_size))
        self.dropout = nn.Dropout(config.hidden_dropout_prob)

    def forward(self, pixel_values):
        batch_size = pixel_values.shape[0]
        embeddings = self.patch_embeddings(pixel_values)

        cls_tokens = self.cls_token.expand(batch_size, -1, -1)
        embeddings = torch.cat((cls_tokens, embeddings), dim=1)
        embeddings = embeddings + self.position_embeddings
        embeddings = self.dropout(embeddings)
        return embeddings
```

- Define the classification token with the embedding dimension nn.Parameter(torch.zeros(1, 1, 768))

- We will add positional embedding with the shape (197 \* 768)

```
 self.patch_embeddings = PatchEmbeddings(
            image_size=config.image_size,
            patch_size=config.patch_size,
            num_channels=config.num_channels,
            embed_dim=config.hidden_size,
        )
```

Pass image size, patch size, num of channels and embed dim to the Parch embedding class.
