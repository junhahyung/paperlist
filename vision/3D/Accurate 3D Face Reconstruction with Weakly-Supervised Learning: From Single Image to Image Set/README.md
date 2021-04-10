![image](https://user-images.githubusercontent.com/42991683/114264439-f502c900-9a25-11eb-928b-84ce821a7a6c.png)

## 3DMM
- based on 3DMM model
- the problem is simplified to getting parameters for 3DMM


## Loss
- use both pixel level loss(photometric + landmark location) and perception level loss
- photometric loss uses attention mask based on skin color
- landmark location loss uses 2d sparse landmakr(2d) (predict 3d landmark and projecting it to 2d)
- perceptual loss to solve local minima problem

## Regularization
![image](https://user-images.githubusercontent.com/42991683/114264669-2c25aa00-9a27-11eb-809a-58ab8c3887ef.png)
- Enforce Gaussian prior on mean face of 3DMM

![image](https://user-images.githubusercontent.com/42991683/114264692-4c556900-9a27-11eb-85ec-05a8a79635ad.png)
- penalize texture map variance

## Weakly-supervised neural aggregation for multi-image reconstruction
- additional Confidence-Net trained to predict confidence of each of the different images of the same instance(dimension same as identity parameter dimension)
![image](https://user-images.githubusercontent.com/42991683/114264769-c4bc2a00-9a27-11eb-9a46-732251ef9e9d.png)
- aggregate identity parameters into one

## Dataset
### RNET
- CelebA
- 300W-LP
- I-JBA
- LFW
- LS3D

### CNET
- 300W-LP
- Multi-PIE
- in-house face recognition dataset(?)
