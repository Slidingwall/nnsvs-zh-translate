![alt text](assets/logo_wide.png)

# nnmnkwii ([nanamin kawaii])
[![][docs-stable-img]][docs-stable-url]
[![][docs-latest-img]][docs-latest-url]
[![PyPI](https://img.shields.io/pypi/v/nnmnkwii.svg)](https://pypi.python.org/pypi/nnmnkwii)
[![Build Status](https://travis-ci.org/r9y9/nnmnkwii.svg?branch=master)](https://travis-ci.org/r9y9/nnmnkwii)
[![Build status](https://ci.appveyor.com/api/projects/status/ch8cmtpw8ic1sd86?svg=true)](https://ci.appveyor.com/project/r9y9/nnmnkwii)
[![codecov](https://codecov.io/gh/r9y9/nnmnkwii/branch/master/graph/badge.svg)](https://codecov.io/gh/r9y9/nnmnkwii)
[![DOI](https://zenodo.org/badge/96328821.svg)](https://zenodo.org/badge/latestdoi/96328821)

用于构建简单、快速的语音合成系统原型的库。

支持python2.7和3.6.

## 文档

- [**STABLE**][docs-stable-url] &mdash; **文档的最近标记版本**
- [**LATEST**][docs-latest-url] &mdash; *文档的开发版本*

## 安装

最新白可从pypi上下载。如果您已经安装了``numpy`` 你可以通过以下方法来安装nnmnkwii ：

    pip install nnmnkwii

如果您想安装最新的开发版本，请运行：

    pip install git+https://github.com/r9y9/nnmnkwii

或是：

    git clone https://github.com/r9y9/nnmnkwii
    cd nnmnkwii
    python setup.py develop # or install

这应该可以解决依赖包并安装``nnmnkwii`` 。

目前，`nnmnkwii.autograd` 包依赖 [PyTorch](http://pytorch.org/)。
若您需要autograd功能，请同时安装PyTorch。

## 鸣谢

本库灵感源自以下开源项目：

- Merlin: https://github.com/CSTR-Edinburgh/merlin
- Librosa: https://github.com/librosa/librosa

[docs-latest-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-latest-url]: https://r9y9.github.io/nnmnkwii/latest

[docs-stable-img]: https://img.shields.io/badge/docs-stable-blue.svg
[docs-stable-url]: https://r9y9.github.io/nnmnkwii/stable

Logo由Gloomy Ghost([@740291272](https://github.com/740291272)) ([#40](https://github.com/r9y9/nnmnkwii/issues/40))设计。
