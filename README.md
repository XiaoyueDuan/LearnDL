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

