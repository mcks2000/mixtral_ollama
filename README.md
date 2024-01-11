# Mixtral 8x7b and LlamaIndex

这是如何使用 Mixtral 8x7b 和 LlamaIndex 启动并运行完全本地化模型的快速演示；更多详情请查看随附的 [文章]()

## 安装依赖

### 第 1 步：创建虚拟环境
注：本资源库中的脚本使用 python 3.10.9 运行
```
conda create -n mixtral_ollama python=3.10.9
conda activate mixtral_ollama
cd mixtral_ollama
```

### 第 2 步：安装依赖项

```
pip install -r requirements.txt


## 代码讲解
## 1_smoketest.py

下载 [Ollama](https://ollama.ai/)并运行 `ollama run mixtral` 后，运行此程序以确保一切连接正常。

## 2_index_data.py

这将索引 `data` 文件夹中的数据。运行次数不限，只会索引新数据。

## 3_verify_index.py

这展示了无需重新加载文件的工作索引。

## app.py

一个非常简单的 Flask 应用程序，演示如何在网络应用程序中使用索引。请注意，"flask run "不起作用；您必须运行 "python app.py"。
