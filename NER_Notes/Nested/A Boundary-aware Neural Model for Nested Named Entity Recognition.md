### A Boundary-aware Neural Model for Nested Named Entity Recognition

融合了了sequence labeling 和region classification 模型

#### 优势

1、利用了边界信息

2、仅对边界之间的区域进行分类，减少了计算量

#### 模型

标记：只标记BIEO边界信息，不标记实体类别

1、表示层：利用LSTM对token进行character embedding, 将character embedding与word  embedding 进行拼接

2、共享编码层：利用双向LSTM对以上表示层进行编码

3、边界分类：对编码后得到的向量接入全连接层并进行softmax，计算KL散度 loss

4、区域分类：提取BE之间的区域以及标签为B的token进行分类，对区域取mean pooling, 接入全连接层，进行softmax分类，计算KL三度loss

5、多任务分类：将3和4的loss取加权平均进行训练