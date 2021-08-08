### Fusion Glyph Network for Chinese Named Entity Recognition

#### 模型

##### 表示层

1、BERT: 先通过BERT + CRF对参数进行fine-tuning, 然后将参数固定用于模型中，c_v

2、CGS -CNN： 经过一系列的卷积和池化层，g_v

3、Radical Embedding: 将汉字拆分成多个组成部分，然后对这多个部分做Attention得到, r_v

##### Fusion Stage

将BERT 和CGS-CNN得到的分别得到多个slice，期间要保证能最终得到的slice数量相同，然后对每个slice做外积，得到的结果Flatten后做Attention, f_v

##### Tagging Stage

将以上结果分两种情况([c_v, g_v, f_v]以及[c_v, g_v, r_, f_v])接入BiLSTM + CRF中