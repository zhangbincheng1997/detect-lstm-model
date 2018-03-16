# 深度学习 检测异常

## 实验环境
| 程序 | 版本 |
| --- | --- |
| 操作系统 | Ubuntu 16.04 |
| 内存容量 | 128 G |
| 硬盘容量 | 8 T |
| 显卡型号 | GTX 1080Ti * 4 |
| 开发框架 | Keras / Tensorflow |

## 检测异常 URL
3 个 Epoch

| 模型        |  准确率  |  时间/Epoch  |
| --------    |  -----:  |  :----:  |
| Bi-LSTM              |  99.15%  |  445ms  |
| Bi-LSTM + CNN        |  99.76%  |  491ms  |
| CNN + Bi-LSTM        |  99.79%  |  145ms  |
| CNN + Bi-LSTM + CNN  |  99.71%  |  145ms  |

## 检测异常 Request
5 个 Epoch

| 模型        |  准确率  |  时间/Epoch  |
| --------    |  -----:  |  :----:  |
| Bi-LSTM              |  82.48%  |  2057ms  |
| Bi-LSTM + CNN        |  98.78%  |  2230ms  |
| CNN + Bi-LSTM        |  98.86%  |  448ms  |
| CNN + Bi-LSTM + CNN  |  99.52%  |  466ms  |

## 网络结构

### Bi-LSTM
![alt text](docs/blstm.jpg "title")

### Bi-LSTM + CNN
![alt text](docs/blstm-cnn.jpg "title")

### CNN + Bi-LSTM
![alt text](docs/cnn-blstm.jpg "title")

### CNN + Bi-LSTM + CNN
![alt text](docs/cnn-blstm-cnn.jpg "title")

## 通用结构

### 输入层 Input
使用字向量，不使用词向量。

### 卷积层 CNN
![alt text](docs/normal-cnn.jpg "title")

### 输出层 Output
![alt text](docs/normal-output.jpg "title")
