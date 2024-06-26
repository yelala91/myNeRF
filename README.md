# 基于NeRFstudio框架实现物体三维重建

## 依赖

```
nerfstudio
COLPMAP
```

## 数据集

### 下载地址

```
https://pan.baidu.com/s/1REOBbroZxQlKou9Az2pfZA?pwd=d26f
```
提取码：d26f
### 处理

首先要对图片用 COLMAP 估计相机参数

```
ns-process-data images --data {DATA_PATH} --output-dir {PROCESSED_DATA_DIR}
```

其中 DATA_PATH 是下载的数据集解压后的地址，PROCESSED_DATA_DIR 是结果输出地址。

## 训练

```
ns-train nerfacto --vis viewer+tensorboard --data {PROCESSED_DATA_DIR}
```
其中 PROCESSED_DATA_DIR 是上一步输出的地址，```--vis viewer+tensorboard``` 用于可视化和输出tensorboard 记录。

## 测试

```
ns-eval --load-config={PATH_TO_CONFIG} --output-path=output.json
```

其中 PATH_TO_CONFIG 是训练完成后输出文档中的 ```.yml``` 文件。