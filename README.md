cjm-pytorch-utils
================

<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->

## Install

``` sh
pip install cjm_pytorch_utils
```

## How to use

### pil_to_tensor

``` python
from cjm_pytorch_utils.core import pil_to_tensor
from PIL import Image
from torchvision import transforms
```

``` python
img_path = img_path = '../images/cat.jpg'
src_img = Image.open(img_path).convert('RGB')
print(f"Source Image Size: {src_img.size}")

img_tensor = pil_to_tensor(src_img, [0.5], [0.5])
img_tensor.shape, img_tensor.min(), img_tensor.max()
```

    Source Image Size: (768, 512)

    (torch.Size([1, 3, 512, 768]), tensor(-1.), tensor(1.))

### tensor_to_pil

``` python
from cjm_pytorch_utils.core import tensor_to_pil
```

``` python
tensor_img = tensor_to_pil(transforms.ToTensor()(src_img))
tensor_img
```

![](index_files/figure-commonmark/cell-5-output-1.png)
