### LEARNING_RATE = 0.01  , STEP = 10000 AND ACTIVATION = RELU

BATCH_SIZS = 16	 ACC = 0.9342

BATCH_SIZS = 32	 ACC = 0.9348

BATCH_SIZS = 64	 ACC = 0.9378

模型收敛速度相似

###  BATCH_SIZE = 32 , STEP = 10000 AND ACTIVATION = RELU

LEARNING_RATE = 0.01 ACC = 0.9348

LEARNING_RATE = 0.03 ACC = 0.9585

LEARNING_RATE = 0.05 ACC = 0.9663

LEARNING_RATE = 0.07 ACC = 0.9721

LEARNING_RATE = 0.09 ACC = 0.9754

随着LEARNING_RATE增大，收敛速度增大，准确率提高，达到0.05时，准确率出现局部降低。当增加一层sigmoid时，LEARNING_RATE达到0.07时，准确率局部降低，增长较为均衡，但准确率最终低于单层relu。

### LEARNING_RATE = 0.01  , STEP = 10000 AND BATCH_SIZE = 32

ACTIVATION = RELU  ACC = 0.9348

ACTIVATION = SIGMOID  ACC = 0.9000

ACTIVATION = TANH  ACC = 0.9325

ACTIVATION = LEAKY_RELU  ACC = 0.9325

ACTIVATION = ELU  ACC = 0.9251

Relu收敛速度远快于sigmoid和tanh

### 正态分布初始化tf.random_normal_initializer(stddev=0.01)

0.9229 增长速度快

### 固定值初始化

### tf.constant_initializer(0.01, dtype = tf.float32)

0.5012 增长速度慢

### 均匀分布初始化 tf.random_uniform_initializer(0, 0.5, dtype=tf.float32)

0.1106 很难找

### 添加sigmoid隐藏层

    cov2 = tf.keras.layers.Dense(
        128,
        kernel_initializer=tf.random_normal_initializer(
            stddev=0.01),
        activation=tf.nn.sigmoid)(cov1)
0.91

