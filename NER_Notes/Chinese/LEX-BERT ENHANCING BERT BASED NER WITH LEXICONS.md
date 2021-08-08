### LEX-BERT: ENHANCING BERT BASED NER WITH LEXICONS

#### 相比于FLAT的优势

1、不需要词的Embedding信息

2、FLAT 不能引入词的类型信息

3、内存消耗更少，推理速度更快

#### LEX-BERT V1

在词的左右边界插入词的类型信息， 如[v]...[/v]

#### LEX-BERT V2

1、将词的类型信息全部加入到句子末尾，并引入位置信息

2、改进BERT的attention机制，词只和词作attention，类型信息和词及类型信息做attention



