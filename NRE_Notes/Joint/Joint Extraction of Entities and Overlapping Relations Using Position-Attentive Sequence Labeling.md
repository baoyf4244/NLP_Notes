### Joint Extraction of Entities and Overlapping Relations Using Position-Attentive Sequence Labeling



#### 标注方式

将长度为N句子标注N次，对序号为p的标注：如果p位置是实体的起始位置，则标注该位置为实体类型，与其有关系的位置则标注为关系类型



#### 模型

1、词表示：Character (CNN)+ Bi-LSTM

2、Position-Aware Mechanism: 对当前词、p位置的词、上下文进行Attention

3、CRF解码