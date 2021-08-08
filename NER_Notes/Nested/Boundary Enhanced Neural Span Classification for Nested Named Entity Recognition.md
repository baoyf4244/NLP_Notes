### Boundary Enhanced Neural Span Classification for Nested Named Entity Recognition



#### span based model 的优势：

很容易找到候选实体 

#### span based model 存在的问题：

1、计算耗时

2、忽略边界信息

#### hypergraph based model 存在的问题

设计hypergraph 时耗费大量人力



#### 模型

##### LSTM编码方式

1、词表示层：[word_embeding, character emebdding, part-of-speech embedding]

2、编码层：双向LSTM

3、边界检测：将编码后得到的的向量接入MLP层进行softmax分类(两个分类器，一个判断实体起始位置，另一个判断实体结束位置)

4、实体分类：抽取起止位置之间的区域，利用注意力机制对区域编码，对其进行softmax分类



##### BERT编码方式

1、编码层：利用BERT对其编码

2、边界检测，同上

3、实体分类：采用自注意力机制对区域进行编码，将区域接入Transformer Block,  对得到的向量取其首尾进行拼接后接入MLP，进行softmax分类

