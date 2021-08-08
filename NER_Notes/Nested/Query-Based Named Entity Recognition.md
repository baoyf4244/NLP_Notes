### Query-Based Named Entity Recognition

#### 优势

1、天然能处理重叠实体

2、可以编码实体类别的先验信息（问题中自带实体类别信息）

3、可以利用现有的MRC模型

#### 模型

1、编码层：BERT

2、分类层：2个三分类器，类别分别为开始位置，结束位置，起止之外的位置

3、Loss：dice loss



