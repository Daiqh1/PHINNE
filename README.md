# VHINSGE

## 环境配置

本项目使用anaconda+python3.7
运行项目所需的几个Python包<br>

* gensim<br>
* numpy<br>
* scikit-learn<br>
* imlearn<br>
* pandas<br>

这些Python包可以使用pip或conda以以下示例进行安装：<br>
```
pip install -r requirements.txt
```
```
conda install --yes --file requirements.txt
```

***
## 文件说明
***共有三个文件***<br>

**1.Input文件夹：**
包括四个数据集的文件夹，包括：<br>
* Dataset Ⅰ:728_129
* Dataset Ⅱ:32_119
* Dataset Ⅲ:312_747
* Dataset Ⅳ:1393_229<br>
其中每个数据集中都含有病毒宿主相互作用，病毒病毒相似性，宿主宿主相似性

**2.Embedding文件夹：**
也有四个文件夹，分别对应四个数据集，每个文件夹包含每一折训练数据生成的node2vec embeddings文件

**3.Novel_VHI文件夹：**
也有四个文件夹，分别对应四个数据集，写入新的VHIs

***
***Python文件***
* load_datasets.py
* get_Embedding_FV.py
* training_functions.py
* pathScores_functions.py
* snf_code.py
* GIP.py
* VHIs_Main_nn4.py
* VHIs_Main_nn.py

## 运行
```
python VHIs_Main_nn4.py --data 728_129
```
```
python VHIs_Main_nn4.py --data 32_119
```
```
python VHIs_Main_nn4.py --data 312_119
```
```
python VHIs_Main_nn.py  --data 1393_229
```
