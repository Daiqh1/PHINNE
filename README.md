# VHINFGE

## 环境配置

本项目使用anaconda+python3.7
运行项目所需的几个Python包,在requirements.txt<br>
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
* Dataset Ⅳ:1380_221<br>

其中每个数据集中都含有病毒宿主相互作用，病毒病毒相似性，宿主宿主相似性

**2.Embedding文件夹：**
也有四个文件夹，分别对应四个数据集，每个文件夹包含每一折训练数据生成的node2vec embeddings文件

**3.Novel_VHI文件夹：**
也有四个文件夹，分别对应四个数据集，写入新的VHIs

***
***Python文件***
* load_datasets.py-->读取输入数据，包括交互和相似性
* get_Embedding_FV.py--> 读取 node2vec 生成的嵌入并获取每个病毒和宿主的 FV（CV 随机种子 = 22）
* training_functions.py-->用于几个训练和处理函数，例如 edgeList、Cosine_similarity、..
* pathScores_functions.py-->计算并返回路径结构的所有路径分数
* snf_code.py-->相似性网络融合函数
* GIP.py--> 计算并返回gussian相似度
* VHIs_Main_ada.py-->3路径

## 运行
```
python VHIs_Main_ada.py --data 728_129
```
```
python VHIs_Main_ada.py --data 32_119
```
```
python VHIs_Main_ada.py --data 312_747
```
```
python VHIs_Main_ada.py  --data 1380_221
```
