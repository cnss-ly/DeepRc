## Task01

### deepcrossing介绍

deepcrossing是一个真正的把深度学习架构应用于推荐系统中的模型，解决了特征工程、稀疏向量稠密化， 多层神经网络进行优化目标拟合等一系列深度学习再推荐系统的应用问题。

模型的输入包含类别型特征（如广告id）和数值型特征（如广告预算）。

模型结构包括四种层：Embedding层，Stacking层，Residual Unit层和Scoring层。

模型输出为预测点击率。

### Embedding

通过单层神经网络将稀疏的类别型特征稠密化，转化为embedding向量。

借助tensorflow.keras.layers下的Embedding()类构建。

### Stacking

数值型特征不需要经过Embedding层，直接进入Stacking层。Stacking层用于将Embedding层的输出特征和数值型特征拼接在一起，构成包含所有特征的特征向量。

组合输入的两种特征。

### Residual Unit

Residual Unit层为不含卷积操作的多层残差网络。

### Scoring

点击率预测是一般是一个二分问题，使用一个逻辑回归得到分数输出。

