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

|  模型  |  准确率  |  精确率  |  召回率  |  F1 Score  |  时间/Epoch  |
|  -----  |  :-----:  |  :----:  |  :----:  |  :----:  |  :----:  |
| Bi-LSTM              |  99.51%  |  99.54%  |  99.81%  |  99.67%  |  1242ms  |
| Bi-LSTM + CNN        |  99.78%  |  99.73%  |  99.97%  |  99.86%  |  1185ms  |
| CNN + Bi-LSTM        |  99.60%  |  99.75%  |  99.72%  |  99.73%  |  326ms  |
| CNN + Bi-LSTM + CNN  |  99.54%  |  99.75%  |  99.64%  |  99.69%  |  318ms  |

## 检测异常 Request
5 个 Epoch

|  模型  |  准确率  |  精确率  |  召回率  |  F1 Score  |  时间/Epoch  |
|  -----  |  :-----:  |  :----:  |  :----:  |  :----:  |  :----:  |
| Bi-LSTM              |  82.30%  |  80.81%  |  99.93%  |  89.23%  |  4434ms  |
| Bi-LSTM + CNN        |  99.11%  |  99.06%  |  99.68%  |  99.36%  |  4406ms  |
| CNN + Bi-LSTM        |  99.10%  |  98.92%  |  99.79%  |  99.35%  |  1101ms  |
| CNN + Bi-LSTM + CNN  |  99.45%  |  99.24%  |  99.96%  |  99.60%  |  1124ms  |

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
