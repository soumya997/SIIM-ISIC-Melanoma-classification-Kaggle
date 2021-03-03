# SIIM-ISIC-Melanoma-classification-Kaggle-challange

<pre>
<img src="imgs/__results___11_1.png" width="900"> <img src="imgs/__results___12_1.png" width="900"> <img src="imgs/__results___16_1.png" width="900"> <img src="imgs/Screenshot (1000).png" width="900"> <img src="imgs/Screenshot (1001).png" width="900"><img src="imgs/Screenshot (1002).png" width="900"><img src="imgs/Screenshot (1003).png" width="900">
</pre>

## Model structure for VGG:
```python
model.add(VGG19(include_top=False, weights='imagenet', input_shape= inputShape))
model.add(Flatten())
model.add(Dense(32))
model.add(LeakyReLU(0.001))
model.add(Dense(16))
model.add(LeakyReLU(0.001))
model.add(Dense(1, activation='sigmoid'))
```

## ResNet101 Model summary:
```python
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
resnet101 (Model)            (None, 7, 7, 2048)        42658176  
_________________________________________________________________
global_average_pooling2d (Gl (None, 2048)              0         
_________________________________________________________________
dense (Dense)                (None, 1)                 2049      
=================================================================
Total params: 42,660,225
Trainable params: 42,554,881
Non-trainable params: 105,344
_________________________________________________________________

``` 
