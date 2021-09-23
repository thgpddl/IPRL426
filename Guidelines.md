# 代码篇
## 路径
使用相对路径

统一使用'/'
## 异常(try)和断言(assert)
善于使用try和assert判断项目中的常见的、可预见的Bug，并输出相关错误信息

文件路径是否存在：
```python
path="/home/work/log.txt"

# 使用try处理
try:
  f=open(path)
except:
  print("文件无法打开，请检查文件路径是合法在或者其他问题")
 
# 使用assert处理
assert os.path.exists(path),print("路径不合法")
```
检查输入数据是否为灰度图：
```python
inputs=img_data
 
# 使用assert处理
assert len(inputs.shape)==2,print("输入数据要求为2维灰度图，但提供的是非2维灰度图")
```
常见异常：
- 路径异常
- 输入数据格式异常(shape、dimension...)
- 



# 目录结构及命名
|描述|命名|必须|
|--|--|--|
|需求|requirements.txt|√|
|单帧推理脚本|inference.py||
|视频推理|inference_video.py||
