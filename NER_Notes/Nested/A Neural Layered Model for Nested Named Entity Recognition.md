### A Neural Layered Model for Nested Named Entity Recognition

#### 模型

1、词表示层：character编码和word Embedding 拼接

2、Flat NER Layer: 将此表示向量接入LSTM + CRF层，预测最内层的实体标签

3、Stacking Flat NER Layer:  根据以上的实体标签抽取实体，将实体所包含的token编码后向量做mean pooling, 非实体token保持不变，重新组合成句子向量表示，将此向量再次接入Flat NER Layer, 重复知道再无任何实体标签产出



#### 缺点

误差传播