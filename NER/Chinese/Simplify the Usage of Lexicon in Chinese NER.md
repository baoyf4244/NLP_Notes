### Simplify the Usage of Lexicon in Chinese NER

#### Lattice LSTM

##### 优势

1、保证了每个字都有对应的词相匹配

2、可引入Word Embedding

##### 劣势

计算量巨大



#### 模型

1、将词的标注标签（B、M、E、S）

2、利用每个词的出现频率对pooling加权

3、将字的embedding与2中的到的embedding拼接

4、接入LSTM-CRF或其他模型



