# Hierarchical Multi-Style Transfer
![Style Transfer](/images/1.png)
![Multi Style Transfer](/images/2.png)
![Multi Style Transfer](/images/3.jpg)
![Multi Style Transfer](/images/9.jpg)
![Spatial Multi Style Transfer](/images/7.jpg)
![Spatial Multi Style Transfer](/images/8.jpg)

## Features
* Single Style Transfer
* Hierarchical Multi Style Transfer (Might have to find really good hyper-parameters to get this to work. There is probably a "pull and tug" on the loss between the different styles, so won't converge well)
* Spatial Multi Style Transfer

## Supported Models
* AlexNet, npy (Not Fully Convolutional)
* VGG16, tfmodel ( Need to fix support )
* VGG19, npy (BEST RESULTS WITH THIS ONE)

## Issues
* There is a bug in the ResNet conversion. You cannot run tf.gradients from your losses to the pixels of the image with resnet. See more here: https://github.com/ry/tensorflow-resnet/issues/12
	* Try converting with Kaffe instead of Ry's converter
* Occasional saturation on images

### Citation
```
  @misc{hierarchicalmultistyletransfer,
    author = {Jason Quach},
    title = {Hierarchical Multi-Style Transfer},
    year = {2017},
    howpublished = {\url{https://github.com/nu1ptr/hierarchical-multi-style-transfer}},
    note = {commit xxxxxxx}
  }
```

## Dependencies
* opencv 3.20
* numpy
* tensorflow 1.10
* python 3
