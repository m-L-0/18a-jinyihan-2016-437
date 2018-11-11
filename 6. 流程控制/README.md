1. 设计一个函数，要求输入两个`shape、dtype`一样的张量，输出一个同样`shape、dtype`的张量，并且输出的张量中的元素的每一个值都是输入的两个张量中对应元素最大的。即模拟`tf.maximum`的功能，但不能直接使用此函数。
2. 了解`tf.minimum`、`tf.maximum`的用法。
3. 了解`TensorArray`的基本用法，并尝试配合`tf.while_loop`配合使用。



先写出判断大小的函数

再将判断大小的函数放入循环中