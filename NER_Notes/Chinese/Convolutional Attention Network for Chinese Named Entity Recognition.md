### Convolutional Attention Network for Chinese Named Entity Recognition

#### Convolutional Attention layer

#### 表示层

1、Character Embedding

2、Segmentation Mask:   采用BMES编码

3、位置编码：在大小为k的窗口中，字符所在的位置编码为1，其他位置编码为0

##### Local Attention 层

在大小为k的窗口中，利用local attention捕获中心字符与上下文之间的关系

##### CNN + Sum Pooling

#### BiGRU with Global Attention

##### BiGRU 编码

##### Global Attention

##### CRF