# 简介
人脸检测及识别
# 目前进展

# 每周进展
按时间倒序排列
## 2019/10/08-2019/10/12

1.207服务器安装cuda9.0，与cuda9.2并存，更改 /etc/profile，source使之生效；

2.安装tensorflow-gpu==1.12，cuda9.0与tensorflow-gpu==1.12版本匹配，cuda9.2没有可用的tensorflow-gpu版本；

3.mtcnn人脸检测mxnet版换成tensorflow版，640*480图片一张人脸，min_face_size = 40，人脸检测所需时间40ms左右；

4.门禁人脸检测方法由mxnet版换成tensorflow版，**/dfb/face/door2/test/door_server_12004.py**。现由客户端传图片、服务器处理图片、识别结果传回客户端，总时长约85ms。
## 2019/9/23-2019/9/26
