# 简介

人群计数：检测出某个场景的人数，通过效果图展示

# 目前进展

项目地址：http://10.10.50.228:3000/AI/API/src/master/code/python/aisuite/human_counter

模型开发已经完成，测试查准率阶段也已经完成，考虑加入热力图中   

## 效果图

#### 车站一   
<img src="https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/station1.png" width="60%">


#### 车站二   
<img src="https://github.com/guomxin/city-video-analysis/blob/master/R%26D/images/station2.png" width="60%">


## 数据集

测试集一: ../mnt/disk03/cityVideoAI/人群聚集/公交站台   (2000张)    

测试集二: ../mnt/disk03/cityVideoAI/人群聚集/mall_dataset   (100张)   

## 模型框架
模型：YOLOv3   
框架：tensorflow keras

## 测试结果

数据集一：../mnt/disk03/cityVideoAI/人群聚集/公交站台 

|      总人数      |    347    |
| :--------------: | :-------: |
| **识别出的人数** |  **295**  |
|    **查全率**    | **85.0%** |

数据集二：../mnt/disk03/cityVideoAI/人群聚集/mall_dataset

|      总人数      |   62315   |
| :--------------: | :-------: |
| **识别出的人数** | **46308** |
|    **查全率**    | **74.3%** |

# 每周进展

### 2019/10/29-2019/11/04  

对于人群密度过高，重叠较为严重的情况，可以考虑通过soft nms 替换nms   
热力图的思路:   
  1.获取bounding box 的中心坐标   
  2.将所有中心坐标处理，放入List   
  3.通过matplotlib画热力图   

### 2019/10/21-2019/10/28

检查了100张左右的图片，查准率为100% 并未出现识别出是人而不是人的情况  

### 2019/10/13-2019/10/20

| 总人数           | 347       |
| ---------------- | --------- |
| **识别出的人数** | **295**   |
| **查全率**       | **85.0%** |

数据集路径 /mnt/disk03/cityVideoAI/公交站台

该数据集选自公交站台数据。一共测试150张图片，相比于mall_dataset，该数据集每张图像的人数较少，离镜头更近。不过有些在公交车上的人也会被识别出来.

总结：1.当图像中的人数越少时，查全率越高。2.人数越多，遮挡越严重，不易于识别。

### 2019/10/08-2019/10/12

测试结果：

|      总人数      |   62315   |
| :--------------: | :-------: |
| **识别出的人数** | **46308** |
|    **查全率**    | **74.3%** |

数据集路径 /mnt/disk03/cityVideoAI/mall_dataset

该数据集选自mall_dataset。是一个商场人群数据集，一共有2000张图像。总人数为62315人，其中模型一共识别出46308人。该数据集采集时镜头较远，有不少人在图像最上方，很难检测出来，还有些人遮挡严重，只能识别成一个。  
