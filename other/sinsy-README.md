# Sinsy

![C/C++ CI](https://github.com/r9y9/sinsy/workflows/C/C++%20CI/badge.svg)

sinsy的一个克隆仓库（fork）：http://sinsy.sourceforge.net/

## 为什么要这么做？

想要用git来克隆仓库（fork）。

为了保存提交历史，用以下命令初始化了仓库：

```
git svn clone https://svn.code.sf.net/p/sinsy/code-0/ --no-metadata --authors-file=authors.txt sinsy
```

后续的改进将根据需要在git仓库中进行。

原始README文件请参见[src/README](src/README)。

## 需求

- https://github.com/r9y9/hts_engine_API

## 安装

```
cd src
mkdir -p build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON  ..
make -j
sudo make install
```

完整的设置请参见https://github.com/r9y9/sinsy/blob/master/.github/workflows/ccpp.yaml.


## 更改

- 为适配最近的C++编译器进行了修复
- 对CMake进行支持
- 使用Github动作进行CI

## 参考文献

- Sinsy官方网站：http://www.sinsy.jp/
- Sinsy官方源代码：http://sinsy.sourceforge.net/
