# 基于NeRFstudio框架实现物体三维重建

## 依赖

```
nerfstudio
COLPMAP
```

## 数据集

### 下载地址

```

```

### 处理

首先要对图片用 COLMAP 估计相机参数终端输入

```
ns-process-data images --data {DATA_PATH} --output-dir {PROCESSED_DATA_DIR}
```

其中 DATA_PATH 是下载的数据集解压后的地址，PROCESSED_DATA_DIR 是结果输出地址。

## 训练