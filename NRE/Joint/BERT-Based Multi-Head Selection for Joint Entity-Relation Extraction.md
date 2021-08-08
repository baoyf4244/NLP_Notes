### BERT-Based Multi-Head Selection for Joint Entity-Relation Extraction
#### pipeline 方式的劣势

1、误差传播

2、忽略实体抽取和关系分类的关系

3、效率低下

#### 模型架构

1、编码层：BERT，在原有基础上引入语义增强

2、实体识别层：CRF

3、Soft Label Embedding:  将进入CRF之前的logits作为Embedding

4、关系分类：Multi-Head Selection