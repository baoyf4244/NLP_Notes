### Deep Exhaustive Model for Nested Named Entity Recognition

#### 模型

1、词表示层：character编码和word Embedding 拼接

2、编码层：使用双向LSTM进行编码

3、区域分类层：设置最大实体长度，穷举句子中符合长度的区域，利用编码层得到的向量对区域进行编码（对实体头部、尾部token以及实体mean pooling后的向量进行拼接），接入softmax进行分类



#### 缺点

耗时