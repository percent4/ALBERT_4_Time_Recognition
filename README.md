# ALBERT_4_Time_Recognition
使用ALBERT预训练模型，用于识别文本中的时间，同时验证模型的预测耗时是否有显著提升。

该项目旨在通过ALBERT+Bi-LSTM+CRF模型来提升模型训练和预测的时间，其中，模型预测耗时为38ms/次。

如何使用该模型？

1. 下载该项目，同时安装项目所依赖的Python模块: tensorflow, tornado;

2. 运行run.py，启动模型训练、预测的HTTP服务;

3. 在浏览器中输入: http://localhost:12306/model_train即可开始模型训练；或者直接运行train.py也可。模型训练的时间较长，需耐心等待，生成后的模型文件位于ckpt文件夹。

4. 模型预测为POST请求，可输入如下命令：

```python
curl -d "event=***" http://localhost:12306/subj_extract
```

模型预测的例子如下（使用软件为Postman）：

![](https://img-blog.csdnimg.cn/20191018231235365.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pjbGlhbjkx,size_16,color_FFFFFF,t_70)

关于该项目的文章，可以参考：https://blog.csdn.net/jclian91/article/details/102631837 。
