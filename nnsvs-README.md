# NN-SVS

[![License](http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat)](LICENSE)
![Python CI](https://github.com/r9y9/nnsvs/workflows/Python%20CI/badge.svg)

> 原作者：r9y9 [来源](https://github.com/r9y9/nnsvs)
>

基于神经网络的歌声合成库的研究。

## 示例

### 使用东北切浦英（kiritan_singing）数据库 （日语）进行的基于神经网络的歌声和成演示。

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/r9y9/Colaboratory/blob/master/Neural_network_based_singing_voice_synthesis_demo_using_kiritan_singing_database_(Japanese).ipynb)
- [![Nbviewer](https://github.com/jupyter/design/blob/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.jupyter.org/gist/r9y9/79705665ed5a94f0028839ca40992751)

## 音频样本

- 东北切浦英（Kiritan）样本: https://soundcloud.com/r9y9/sets/dnn-based-singing-voice

## 安装

- Python 3.6或者更新的版本
- [nnmnkwii](https://github.com/r9y9/nnmnkwii): 需要**开发版** (master分支)
- [pysinsy](https://github.com/r9y9/pysinsy) 需要**开发版** 。安装请留意一下版本库。
- Pytorch >= 1.x

请注意以上列出的依赖包需要手动安装。安装后请运行：

```
python setup.py develop
```

来完成剩余依赖关系的安装。

## 仓库结构

- 核心库: [nnsvs/](nnsvs/)
- 命令行程序: [nnsvs/bin/](nnsvs/bin) 及其配置 [nnsvs/bin/conf/](nnsvs/bin/conf/)
- 语音库: [egs/](egs/)

## Python 文档字符串(docstring) 风格

https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html

## 语音库

语音库训练文件是一组用于再生语音库的脚本与配置。所有用于再生语音库的步骤都是独立提供的。如果你想建立自己的语音库，请看一下[egs](egs)目录。

## 背景

2020年2月以来，一款基于DNN的歌声合成软件 [NEUTRINO](https://n3utrino.work/)开始在日本走红。由于基于强大的DNN算法，用户可以创造出富有表现力的、自然的歌声。使用现有的工具，即使不需要手动调校也可以达到令人满意的质量。

虽然NEUTRINO是极好的创作软件，但它并不开源。据我们所知，它只有少数的几个开源小工具。为了推进歌声合成的研究，我们致力于为研究者和开发者提供一个基于DNN的现代歌声和合成工具。

说了这么多，其实我只是好奇我能不能做出一个比NEUTRINO更好的歌声合成软件。拭目以待:)

## 开发历史

详见[HISTORY.md](HISTORY.md)

## 已知问题


## 参考文献

- Y. Hono 等, "Recent Development of the DNN-based Singing Voice Synthesis System — Sinsy," Proc. of APSIPA, 2017. ([PDF](http://www.apsipa.org/proceedings/2018/pdfs/0001003.pdf))
- sinsy的克隆仓库: https://github.com/r9y9/sinsy
- sinsy的Python封装器: https://github.com/r9y9/pysinsy
- NEUTRINO: https://n3utrino.work/







[返回](/nnsvs-zh-traanslate/nnsvs/)