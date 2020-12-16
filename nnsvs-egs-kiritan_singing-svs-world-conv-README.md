# svs-world-conv

构建统计参数化歌声合成语音库的训练文件。一个语音库由三个可训练网络组成：

1. 时间差模型
2. 持续时间模型
3. 声学模型

对于波形的分析和合成，将采用WORLD vocoder。语音库系统的基本架构与以下论文中描述的类似：

Y. Hono et al, "Recent Development of the DNN-based Singing Voice Synthesis System — Sinsy," Proc. of APSIPA, 2017. ([PDF](http://www.apsipa.org/proceedings/2018/pdfs/0001003.pdf))

但请注意，细节处仍有很多不同（例如，混合密度网络暂时还未在我们的代码中采用）。请参阅代码中的完整设置。

## 步骤

请先下载东北切浦英歌声数据集：https://zunko.jp/kiridev/login.php，并在`run.sh`中设置 `wav_root`。

### 数据下载

```
CUDA_VISIBLE_DEVICES=0 ./run.sh --stage -1 --stop-stage -1
```

### 数据准备

```
CUDA_VISIBLE_DEVICES=0 ./run.sh --stage 0 --stop-stage 0
```

### 特征提取

```
CUDA_VISIBLE_DEVICES=0 ./run.sh --stage 1 --stop-stage 1
```

### 训练时间差/持续时间/声学模型

```
CUDA_VISIBLE_DEVICES=0 ./run.sh --stage 2 --stop-stage 4
```

### 合成


```
CUDA_VISIBLE_DEVICES=0 ./run.sh --stage 5 --stop-stage 6
```

您可以在`exp/kiritan/synthesis`目录下找到生成的样本

## 高级用法

### 预训练模型

若您想使用外部的预训练模型，请指定`--pretrained-expdir` ，例如：

```
CUDA_VISIBLE_DEVICES=0  run.sh --stage 2 --stop-stage 4 --pretrained-expdir /path/to/expdir
```

预计预训练模型的exp目录将包含三个子目录：

1. timelag
2. duration
3. acoustic

每个目录将包含一个预训练模型，分别为时间差/持续时间/声学模型





[返回](/nnsvs-zh-traanslate/nnsvs/)