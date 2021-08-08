### CNN-Based Chinese NER with Lexicon Rethinking

#### Lexicon-based CNNs

1、CNN：用于捕获1-n gram特征， C

2、将ngram特征与Lexicon特征做Attention， X

#### Lexicon Rethinking

1、将每层的C、Lexicon特征以及顶层的X做Attention，得到X‘

2、将每层的X’ 做Attention，得到的结果，再将每层的结果进行拼接得到最终的多层次结果

#### CRF

