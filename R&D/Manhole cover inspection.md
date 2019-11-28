

# 简介

井盖检测：检测场景中是否存在井盖

# 目前进展

项目地址：

模型开发中，现阶段正在处理井盖数据

## 效果图

## 数据集



## 模型框架

模型：YOLOv3   
框架：tensorflow,keras

## 测试结果



# 每周进展

按时间倒序排列

## 2019/11/21-2019/11/28

1.本次开发采用yolo3模型，tensorflow深度学习框架   
2.数据集来源：线下收集+网络收集   
3.初步采集+整理了大约80张图片,通过数据增广、裁剪大约扩展到800张图片,其中有井盖和无井盖之间的比大约为5：3   
4.   
 a.现如今的一些问题：(1)识别出现错误的概率很小，但是有些井盖不识别。(2)识别出的物体的置信率过低         
 b.可能解决的方案：增大数据集，源数据集只有80张，即使数据增广后也只有800张，还是太少。特征提取不明显。        
5.部分效果图如下：   
![井盖图片1](https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/jinggai1.png)
![井盖图片2](https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/jinggai2.png)
![井盖图片3](https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/jinggai3.png)
![井盖图片4](https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/jinggai4.png)
![井盖图片5](https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/jinggai5.png)
