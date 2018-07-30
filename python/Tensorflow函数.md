#  Tensorflow函数

#####tf.truncated_normal

tf.truncated_normal(shape, mean, stddev) :shape表示生成张量的维度，mean是均值，stddev是标准差。这个函数产生正太分布，均值和标准差自己设定。这是一个截断的产生正太分布的函数，就是说产生正太分布的值如果与均值的差值大于两倍的标准差，那就重新生成。和一般的正太分布的产生随机数据比起来，这个函数产生的随机数与均值的差距不会超过两倍的标准差，但是一般的别的函数是可能的。 

#####tf.argmax

返回沿轴axis最大值的索引，第二个参数表示选取最大值的操作的进行维度，=1表示选取每一行最大值对应的下标

#####tf.reduce_mean

元素取平均，axis控制维度

#####打印出结果值

print(sess.run(a))或print(a.eval())

#####tf.nn.xw_plus_b      

x*w+b

##### lambda表达式

相当于函数简写，lambda a: a*3, a是参数，返回a *3

##### for t1,t2 in zip(xNew,wNew) 

zip():同时变化

##### [tf.concat](https://blog.csdn.net/mao_xiao_feng/article/details/53366163)

按照某一维度连接两个矩阵

