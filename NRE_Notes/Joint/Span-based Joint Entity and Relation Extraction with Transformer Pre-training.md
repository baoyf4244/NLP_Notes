### Span-based Joint Entity and Relation Extraction with Transformer Pre-training



#### Span Classification

1、实体表示：Bert Embedding (最好max pooling)

2、实体宽度Embedding

3、上下文表示：CLS

三者拼接成整个实体表示接入全连接层做实体分类（实体类型 + None）



#### Span Filter

过滤掉非实体以及长度大于10的实体



#### Relation Classification

1、实体表示采取Span classification中的1、2两步

2、对两实体之间的字符做max pooling

3、拼接结果 [实体1，实体之间Embedding， 实体2] 及  [实体2，实体之间Embedding， 实体1]  （两实体的双向关系）

4、以上接入全连接层进行关系分类



