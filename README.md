# Image Denoiser - AutoEncoder 
Implemented it on MNIST dataset using Pytorch and CNN.

## Table of Content
1. MNIST Dataset
2. Architecture of Model
3. Hyperparameters
4. Training
5. Results 

### MNIST Dataset
MNIST dataset which stands for Modified National Institute of Standards and Technology dataset. It is a dataset of 60,000 small square 28×28 pixel grayscale images of handwritten single digits between 0 and 9. 

![This is an image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQI3MtlwiEYvnWsRhIV1sWYa16YjBdYn1ICMeoe0vUw_GNeGZMjcC74WkXz1CdnOpMqb8k&usqp=CAU)

### Architecture of Model

|     Layer      | Number of Filter | Filter Size | Max Pool | Padding | Stride |
| -------------- | ---------------- | ----------- | -------- | ------- | ------ |
|     Conv1      |        16        |      3      |   None   |    1    |  None  |
|     Conv2      |        32        |      3      |   None   |    1    |  None  |
|     Conv3      |        64        |      3      |   2x2    |    1    |  None  |
| ConvTranspose1 |        16        |      2      |   None   |  None   |   2    |
| ConvTranspose2 |         1        |      2      |   2x2    |  None   |   2    |


### Hypermeters 

| Hypermeters   | Value |
| ------------- | ----- |
| Epochs        | 20    |
| Learning Rate | 0.01  |
| Momentum      | 0.9   |

### Training 
**Noise Added**
Random noise added via torch.randn() such that we can change noise by changing noise factor. We can also add Gaussin noise,salt noise and many more types of noises.

### Result 
**Output (Denoised Image)**             

![screenshot-colab research google com-2021 10 16-23_51_36](https://user-images.githubusercontent.com/88239463/137598249-e9737d34-8a03-4ea4-adf8-a96d9e540829.png)

**Input (Noised Image)**



#### Epoch vs Loss 

![image](https://user-images.githubusercontent.com/88239463/137598311-0f7e4f0a-c724-4bba-aab5-5eccff0ae1e7.png)
