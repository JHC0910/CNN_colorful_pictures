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

##Result
對於mnist手寫辨識的資料集，其不論是測試和訓練的準確率都可輕易達到99%。
但是對於cifar10彩色圖集的辨識只能達到接近80%的測試準確率。由於測試準確率到達90%沒到太高且測試準確率也不算太低，並不算所謂overfitting。
未來只要透過將模型的層數增加應能增加準確率。

