## 数据集

数据集中共有标签6个，图片1195张。组成如下：

| 标签 | 训练集 / 验证集 | 总计 |
| ---- | ------------- | ---- |
| cat | 133 / 6 | 139 |
| cow | 155 / 7 | 162 |
| dog | 154 / 7 | 161 |
| bear | 794 / 10 | 804 |
| goat | 70 / 6 | 76 |
| human | 131 / 6 | 137 |


## 训练参数

### 图像增强

* 随机镜像：开
* 随机旋转：关
* 随机模糊：开
* 缩放方式：contain
* 缩放尺寸：224 * 224
* 平均值：123.5
* 标准差：58.395

### 模型信息

* 部署平台：nncase
* 模型网络：yolov2
* 主干网络：mobilenet_0.75

### 训练参数

* 训练次数：150
* 批量大小：32
* 学习率：0.001
* 标注框限制：8
* 数据均衡：关
* 允许负样本：开


## 训练结果

在验证集上第150次训练迭代有最佳准确率：0.654。
![image](https://github.com/user-attachments/assets/efc49203-af0e-4688-a9e8-fdcd2bdf20f3)


### 验证集结果抽样展示

* 正确结果

![image](https://github.com/user-attachments/assets/eaf3997c-ee4a-422b-80e9-7d6364908e45)
![image](https://github.com/user-attachments/assets/21c88ac9-24a0-4a07-a99c-77eb79e7c828)
![image](https://github.com/user-attachments/assets/6d375edf-8404-48fd-8f80-1b6bfcfc0ea3)
![image](https://github.com/user-attachments/assets/bdd65ba1-653b-41f2-8265-41d3d5dd4447)



* 错误结果

![image](https://github.com/user-attachments/assets/93f39411-53c7-4c55-a106-09bd4305cf78)
![image](https://github.com/user-attachments/assets/f31dcce2-121d-4aa9-9937-de81589aac77)
![image](https://github.com/user-attachments/assets/fe7f89ea-a063-4c96-b7b1-d9d2e054dc83)
![image](https://github.com/user-attachments/assets/9c6d58a9-971b-4b5e-9d92-9b716100a411)



> *白色框为用户标注框*
> *绿色框为模型正确预测框*
> *红色框为模型错误预测框*
> *只有白色框说明模型未检测到目标*

