1. 构建二元线性回归模型，其中模型中的参数使用`tf.Variable()`构建，模型的样本输入使用`tf.placeholder`代替。写出模型结构。
2. 使用`tf.placeholder`代替上述样本中的标记，写出对于一个样本的代价。



构建函数，参数为variable，未知数为placeholder，直接在函数中进行替换

cost function 基于最小二乘