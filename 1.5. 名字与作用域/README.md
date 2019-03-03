1. 总结`name_scope`与`variable_scope`的作用以及异同点。
2. 构建逻辑回归模型（只有模型部分，不包括训练部分），使用`get_variable`与`variable_scope`将变量的创建与使用分开。提示：使用`tf.nn.sigmoid`实现`logistic`函数。



variable_scope包括name_scope的所有功能，并且有所添加。

logistics regression，首先取一个未预测的x，带入函数中，得到该x对应的y