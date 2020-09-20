# CNN_colorful_pictures

## 採用資料集
**cifar10** & **mnist手寫辨識**

## 使用模型
Convolutional Neural Network
~~~js
model.add(Conv2D(filters = 32, kernel_size = (3,3), input_shape = (32,32,3), activation = 'relu', padding = 'same'))
model.add(MaxPooling2D(pool_size = (2,2)))
model.add(Conv2D(filters = 64, kernel_size = (3,3), activation = 'relu', padding = 'same'))
model.add(Dropout(0.25))
model.add(MaxPooling2D(pool_size=(2,2)))
model.add(Flatten())
model.add(Dropout(0.25))
model.add(Dense(1024, activation = 'relu'))
model.add(Dropout(0.25))
model.add(Dense(10, activation = 'softmax'))
~~~



