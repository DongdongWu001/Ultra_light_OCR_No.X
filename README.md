# AI-Studio-Ultra_light_OCR_No.X

## 项目描述
我组参赛的代码实现以paddleOCR2.1版本为基础，进行参数优化以及量化训练。代码结构和训练操作见本次比赛baseline

## 项目结构
```
-|data
-|work
-README.MD
-OCRlight.ipynb
```
## 模型训练
模型选择：mobilenet_v3
模型训练参考比赛baseline. 为获得较好的模型精度并控制模型大小，在模型训练过程中，在rec_chinese_lite_train_v2.0.yml文件的默认配置上，修改骨干网络：
Bcakbone:
name:MobileNetv3
scale:1.0
model_name:large

## 模型量化
模型优化操作参考：PaddleOCR_slim

训练好的模型精度较高，但是模型大小超出比赛规定范围。经调研，可用量化模型在精度损失较少的前提下降低模型大小。
![image](https://user-images.githubusercontent.com/35124524/125040757-93a4d180-e0ca-11eb-9e79-f89f7ca8c3e9.png)


## 使用方式
A：在AI Studio上[运行本项目](https://aistudio.baidu.com/aistudio/usercenter)
B：
