# TVM进度规划以及困难记录

2024.4.12  
目前计划将TensorRT安装部署在1806服务器上，阅读了解TensorRT的使用指南

2024.4.19  
![b51cb5c40825f1c06c58ef96e6b322c](https://github.com/Dotachuan/TVM/assets/80832042/c76bc7c3-9dda-4df6-a1cd-a8230127e611)  
目前已确定毫米波雷达算法中的某些算子不被onnx支持，下一步或参照https://blog.csdn.net/zhaoyqcsdn/article/details/135512992 进行自定义算子或将目标模型改成CNN模型

tensorrt方面，参照https://blog.csdn.net/m0_38043555/article/details/114479282 中的样例编写了将Onnx构建为tensorrt的代码以及用trt推理引擎进行推理的代码

2024.4.24  
之前docker内torch.cuda.is_available()常常会在几天后突然变成False，一直未找出问题所在，偶然重启容器后发现其又变成True，找到了解决方法，即容器运行一段时间后重启容器。  

在 https://onnx.ai/onnx/operators/index.html onnx支持算子文档中搜索，发现模型中的“stack”算子不在onnx支持范围内，且“flatten_parameters”也不在onnx的支持范围  

获得了毫米波雷达算法的计算图

2024.5.25
![image](https://github.com/Dotachuan/TVM/assets/80832042/5defb819-10ed-4b88-9734-1133b81f237f)
由于直接运用conda无法安装一些所需要的包，因此改变conda设置，将源换成清华源。

