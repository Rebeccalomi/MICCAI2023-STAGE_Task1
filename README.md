# MICCAI2023-STAGE_Task1

# Introduction

[https://aistudio.baidu.com/aistudio/competition/detail/968/0/introduction](https://aistudio.baidu.com/aistudio/competition/detail/968/0/introduction)

任务一：平均偏差值预测
本任务是根据黄斑OCT图像和青光眼分期信息预测24-2模式的视野报告中的平均偏差(Mean Deviation, MD)值，它反映了青光眼患者因神经节细胞死亡导致的平均视力下降，正常人的MD值在0dB左右。在临床诊断中，MD值是H-P-A和Mills视觉分类的关键参数。因此，在本次围绕利用结构图像预测功能信息的挑战赛中，我们将该值的预测作为第一项任务。由于眼底结构和视觉功能之间的映射关系尚不明确，这项任务仍然具有挑战性，本次任务中提供了青光眼分期信息作辅助。

Task 1: Prediction of Mean Deviation
This task aims to predict the mean deviation (MD) in the 24-2 mode perimetry report based on macular OCT images and glaucoma stage information. MD reflects the average decrease in visual acuity caused by ganglion cell death in glaucoma patients, with a typical MD value of around 0dB in normal individuals. The MD value is a key parameter in both H-P-A and Mills visual classification methods for clinical diagnosis. Therefore, predicting this key value serves as the first task in our challenge, which focus on predicting functional information based on structural images. However, this task remains challenging because the mapping relationship between fundus structure and visual function is unclear. Glaucoma staging information is provided to assist in this task.

# Method
将一组OCT图片同时输入baseline网络，同时输出为单通道预测值和青光眼分级结果，经过sigmoid激活函数将其放缩到[0,1]，训练过程使用数据集中的青光眼辅助信息将其进行数据的放缩得到预测值，预测过程使用青光眼分级结果将其进行数据的放缩得到预测值。

Input a group of OCT images into the baseline network, and output the single channel predictive value and glaucoma grading results at the same time. Scale them to [0,1] through the sigmoid Activation function. During the training process, use the glaucoma auxiliary information in the dataset to scale the data to get the predictive value. During the prediction process, use the glaucoma grading results to scale the data to get the predictive value.

# Usage
将下载数据集放入根目录`data`文件夹（需创建）
运行`Main.ipynb`

Please download the dataset and put it under `.data/` folder (needs to be created)
Run `Main.ipynb`

