# 继YOLOv8后，YOLOv5和v7的快速入门
# YOLOv5：
# 1、准备
1. 我采用的是Anaconda+Pycharm的配置，和yolov8文章中的环境一模一样
2. 下载yolov5：https://github.com/ultralytics/yolov5
3.  修改数据集中的data.yaml（具体在yolov8笔记有提到）
4.  把数据集中的data.yaml放在data中
5.  安装依赖，pycharm仓库主路径下terminal输入：

```python
pip install -r requirements.txt
```
6. 测试：直接运行detect.py，不报错，给出保存路径即成功
# 2、训练
1. 和yolov8不同的是，yolov5的训练是通过修改train.py文件并运行
2. 打开train.py，下滑至约434行处开始改参数 <br>
![在这里插入图片描述](https://img-blog.csdnimg.cn/d5eedae7d37144548febb95aa29f4a4a.png)
<br>方框中即为要改的参数，要填路径的填上路径即可
![在这里插入图片描述](https://img-blog.csdnimg.cn/edecf145411d466c9aa7aa795c0314b6.png)
3.运行train.py

<br>训练完成：<br>
![在这里插入图片描述](https://img-blog.csdnimg.cn/3ce746cafa754d2c8228e31e66cb1ad3.png)
# YOLOv7
# 1、准备
1. 我采用的是Anaconda+Pycharm的配置，和yolov8文章中的环境一模一样
2. 下载yolov7：https://github.com/WongKinYiu/yolov7
3. 下载权重yolov7.pt，并放在仓库主路径上（权重下载后就是压缩包.zip的形式，不必解压）
4. 修改数据集中的data.yaml（具体在yolov8笔记有提到）
5. 把数据集中的data.yaml放在data中
![在这里插入图片描述](https://img-blog.csdnimg.cn/2e6b45962cc84b6ca9aed4d3731e3e61.png)

6. 安装依赖，pycharm仓库主路径下terminal输入：

```python
pip install -r requirements.txt
```
# 2、训练
和yolov8差不多，就是多了一个权重yaml文件，具体也不再赘述

```python
python train.py --weights yolov7.pt --cfg cfg/training/yolov7.yaml --data data/data.yaml --device 0 --batch-size 8 --epoch 100
```
（如果报错在哪哪哪找不到dataset，那就把dataset放在哪哪哪就好）
