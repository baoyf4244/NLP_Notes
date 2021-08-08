### An Encoding Strategy BasedWord-Character LSTM for Chinese NER 

#### Lattice LSTM 劣势

1、有时不能选择正确的路径，最终会退化成基于词的模型，引入分词错误

2、不能并行化：与字绑定的词的长度和数量不同

#### 模型

##### 词-字编码层

##### 词编码策略

1、选取最短的

2、选取最长的

3、将词的Embedding取平均

4、自注意力机制

##### WC-LSTM

将字Embedding 和  按编码策略编码好的词Embedding 拼接 接入双向LSTM

##### 解码层

CRF 