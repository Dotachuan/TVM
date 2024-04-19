# TVM进度规划以及困难记录

2024.4.12  
目前计划将TensorRT安装部署在1806服务器上，阅读了解TensorRT的使用指南

2024.4.19  
![b51cb5c40825f1c06c58ef96e6b322c](https://github.com/Dotachuan/TVM/assets/80832042/c76bc7c3-9dda-4df6-a1cd-a8230127e611)  
目前已确定毫米波雷达算法中的某些算子不被onnx支持，下一步或参照https://blog.csdn.net/zhaoyqcsdn/article/details/135512992 进行自定义算子或将目标模型改成CNN模型

tensorrt方面，参照https://blog.csdn.net/m0_38043555/article/details/114479282中的样例编写了将Onnx构建为tensorrt的代码以及用trt推理引擎进行推理的代码
