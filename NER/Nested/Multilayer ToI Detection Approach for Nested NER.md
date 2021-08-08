### Multilayer ToI Detection Approach for Nested NER
#### 模型

1、表示层：word embedding + character embedding + POS emebdding

2、编码层：Bi-LSTM

3、对偶Transformer层：在原来的基础上加入掩码矩阵

4、卷积层

5、HAT pooling