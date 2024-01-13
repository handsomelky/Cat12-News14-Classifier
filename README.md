# Cat12-News14-Classifier

《人工神经网络》课程的实验大作业，包括猫咪分类以及新闻标题分类任务

## 项目地址

本次实验我分别完成了01猫咪分类、02新闻标题分类以及04中英文翻译

前两个均使用pytorch实现，中英文翻译则是使用paddlepaddle平台

01、02：https://github.com/handsomelky/Cat12-News14-Classifier

04：https://aistudio.baidu.com/projectdetail/7399087

## 环境

本项目的python环境为3.8.17

需要安装Pytorch框架，除此之外可以通过运行以下指令一键安装其他库

``` shell
pip install -r requirements.txt
```

## 文件结构

本次实验中的代码均被放置在`code`文件夹中，每个任务有一个代码文件（包括了多个模型及训练测试过程）

数据集文件应该解压到`dataset`目录下

模型训练得到的最佳数据存储在`state`目录下，同时每个任务都有一个子目录，如`01-cat`，其中不同权重文件以模型名字来命名，如`model_cnn.pt`

同时有一个任务的模型有记录曲线变化，其tensorboard数据存储在`log`文件夹下

下面是数据集正确放置后的**文件结构**

- dataset
  - 01-猫咪分类
    - data
      - cat_12_train
      - train_list.txt
  - 02-新闻标题分类
    - data
      - dev.txt
      - test.txt
      - train.txt

## 训练

打开每个任务的代码文件，如果存在多个模型，则找到相应的选择模型的模块

任务一猫咪分类选择模型的部分如下

![image-20240113013451660](https://r1ck-blog.oss-cn-shenzhen.aliyuncs.com/image-20240113013451660.png)

更改model_name即可

任务二新闻标题分类选择模型的地方如下

![image-20240113013547178](https://r1ck-blog.oss-cn-shenzhen.aliyuncs.com/image-20240113013547178.png)

同样是更改model_name

选择好模型之后，**一键运行所有代码即可开始训练+测试**

## 测试

和训练过程一样，如果存在多个模型，需要先更改model_name

如果想跳过训练过程，直接使用之前训练好的最优参数导入模型，**可以分段运行代码，并跳过训练模型部分**

任务一**不要运行**下面这一部分

![image-20240113013859444](https://r1ck-blog.oss-cn-shenzhen.aliyuncs.com/image-20240113013859444.png)

任务二**不要运行**下面这一部分

![image-20240113013800618](https://r1ck-blog.oss-cn-shenzhen.aliyuncs.com/image-20240113013800618.png)





