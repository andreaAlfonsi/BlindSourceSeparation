# Blind Source Separation for images

The purpose of this project is to separate an image obtained as a sum of a two images into its components.

The two images img1 and img2 summed together come from different dataset: [mnist](http://yann.lecun.com/exdb/mnist/) and [fashion_mnist](https://github.com/zalandoresearch/fashion-mnist), respectively.

No preprocessing was allowed. The network takes in input the sum img1+img2 and returns the predicted components hat_img1 and hat_img2.

The metric used to evaluate the project is the mean squared error between predicted and ground truth images.

## Model

After a lot of experiments with different models based on the UNet backbone (including [UNet++](https://arxiv.org/abs/1912.05074), [DCNet](https://pubmed.ncbi.nlm.nih.gov/32444591/) and [SUnet](https://arxiv.org/abs/2202.14009)) the best results emerged with a [MultiResUNet](https://arxiv.org/pdf/1902.04049.pdf)-like structure.

In particular, the model is made of an encoder and two decoders, whose output will then be concatenated to generate the desired result.

## Data example
### Input:

![input image](/img/1.png)

### Output:

![input image](/img/2.png)
---
### Author: [Andrea Alfonsi](https://www.linkedin.com/in/andrea-alfonsi-976411152/)
