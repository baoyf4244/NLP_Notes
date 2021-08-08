### Neural Architectures for Nested NER through Linearization

#### 标签编码

1、先出现的实体优先

2、长实体优先

#### 模型：

##### 1、LSTM-CRF：将多个标签当成一类

优势：简单高效

劣势：实体类别大大增加

##### 2、seq2seq

