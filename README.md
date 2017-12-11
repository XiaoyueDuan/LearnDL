# 学习DL过程中的作业
学习[fasf.ai](http://www.fast.ai/)Part 1过程中的作业，使用Jupiter NoteBook，Python3。

## 作业一：调用Keras的VGG16实现猫狗图片区分
- 数据来源：[Kaggle](https://www.kaggle.com/c/dogs-vs-cats)
- 结果：见lesson1/lesson1_hw.ipynb
- 小节：入门作业，学习过程有问题，在后续学习中注意参数含义的学习。
- 数据存储格式：
<ol>mini_dogscats/
<ol>test/
    <ol>1.jpg</ol>
    <ol>2.jpg</ol>
    <ol>...</ol></ol>
<ol>train/
    <ol>cat/
      <ol>cat0.jpg</ol>
      <ol>cat1.jpg</ol>
      <ol>...</ol></ol>
    <ol>dog/
      <ol>dog0.jpg</ol>
      <ol>dog1.jpg</ol>
      <ol>...</ol></ol></ol>
  <ol>valid/
    <ol>cat/
      <ol>cat0.jpg</ol>
      <ol>cat1.jpg</ol>
      <ol>...</ol></ol>
    <ol>dog/
      <ol>dog0.jpg</ol>
      <ol>dog1.jpg</ol>
      <ol>...</ol></ol></ol>
</ol>

## 作业二：Finetune VGG16，修改最后一层从1000维输出为2维输出
结果：**0.16476**
实现流程：
1. 修改Vgg16网络最后一层，从1000维输出为2维输出
2. 训练新网络获得权重，并通过测试validate集查看该网络的表现
3. 在训练集上进行预测
4. 提交结果

在作业二中几个值得注意的地方：
- 我们使用sgd作为优化器，学习率设为```1e-3```
- test文件夹内的文件格式应为
```
test1/
    test/        # could be any name
        1.jpg
        2.jpg
        ...
```
        
而不是
```
test/        # could be any name
    1.jpg
    2.jpg
    ...
```
- 生成的结果顺序为字母表顺序，即：
```
    1.jpg
    10.jpg
    100.jpg
    1000.jpg
    1001.jpg
    ...
```
我们使用正则表达式提取文件中的数字重新排序，得到
```
    1.jpg
    2.jpg
    3.jpg
    4.jpg
    5.jpg
    ...
```