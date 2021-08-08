#### Multi-Grained Named Entity Recognition

##### 模型结构

###### 检测器

1、词表示层：Word Embedding + POS Embedding + character Embedding

2、句子表示层：双向LSTM  + ELMO 拼接，然后再次接入双向LSTM

3、检测层：以每个词为中心，挑选R个候选实体，接入2分类器，判断是不是实体

###### 分类器

1、词表示层：Word Embedding + POS Embedding 复用检测器的，character Embedding

重新训练

2、实体表示层：将实体上下文头尾向量进行拼接作为实体向量，将实体向量与上下文句子向量做attention，在将结果接入双双向LSTM，将得到的头尾向量拼接再与实体向量拼接作为最终表示结果

3、分类网络：构建(N+1)分类器, N代表实体类型数量，1代表非实体情况，采用hinge-ranking loss

