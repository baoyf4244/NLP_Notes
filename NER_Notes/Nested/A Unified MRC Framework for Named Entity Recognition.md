### A Unified MRC Framework for Named Entity Recognition

#### 优势

1、天然能处理重叠实体

2、可以编码实体类别的先验信息（问题中自带实体类别信息）

#### 模型

1、query生成：将标注说明作为问题，编码成（问题，答案，上下文）

2、编码层：利用BERT编码，问答对处理成[[CLS],问题，[SEP], 上下文]形式，接入BERT

3、区间选择：训练两个二分类器，一个对起始位置分类，另一个对结束位置分类

4、区间分类：对任意起始位置，选取其后的所有结束位置，生成实体区间，将区间头尾拼接，进行二分类（由于问题里已经有了类别信息，所以只分类是不是实体就可以了）