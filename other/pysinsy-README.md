# Pysinsy

![Python package](https://github.com/r9y9/pysinsy/workflows/Python%20package/badge.svg)
[![License](http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat)](LICENSE.md)

https://github.com/r9y9/sinsy 的Python封装器。

请注意本软件包仍处于Alpha状态，API可能有所改动。一旦我完成了最初的设计，我将标记一个版本。

## 安装

本软件包基于sinsy的共享库构建，您必须从源码编译sinsy并安装到您的系统中。参见https://github.com/r9y9/sinsy 并安装。

sinsy安装完成后，您可以通过以下命令安装pysinsy：

```
python setup.py develop
```


## 快速演示

```py
import pysinsy

sinsy = pysinsy.sinsy.Sinsy()

# Set language to Japanese
assert sinsy.setLanguages("j", "/usr/local/lib/sinsy/dic")

assert sinsy.loadScoreFromMusicXML("./tests/song070_f00001_063.xml")

print("Mono labels:")
is_mono = True
labels = sinsy.createLabelData(is_mono, 1, 1).getData()
for l in labels[:5]:
    print(l)

print("\nFull-context labels:")
is_mono = False
labels = sinsy.createLabelData(is_mono, 1, 1).getData()
for l in labels[:5]:
    print(l)

sinsy.clearScore()
```

输出：

```
Mono labels:
0 10909090 sil
10909090 21818181 sil
21818181 32727272 sil
32727272 43636363 pau
43636363 47727272 g

Full-context labels:
0 10909090 s@xx^xx-sil+sil=sil_xx%xx^00_00~00-1!1[xx$xx]xx/A:xx-xx-xx@xx~xx/B:1_1_1@xx|xx/C:2+1+1@JPN&0/D:xx!xx#xx$xx%xx|xx&xx;xx-xx/E:xx]xx^0=2/4~110!1@109#48+xx]1$1|0[10&0]48=0^100~xx#xx_xx;xx$xx&xx%xx[xx|0]0-n^xx+xx~xx=xx@xx$xx!xx%xx#xx|xx|xx-xx&xx&xx+xx[xx;xx]xx;xx~xx~xx^xx^xx@xx[xx#xx=xx!xx~xx+xx!xx^xx/F:A4#9#0-2/4$110$1+40%18;xx/G:xx_xx/H:xx_xx/I:12_12/J:2~2@3
10909090 21818181 s@xx^sil-sil+sil=pau_xx%00^00_00~00-1!1[xx$xx]xx/A:xx-xx-xx@xx~xx/B:1_1_1@xx|xx/C:2+1+1@JPN&0/D:xx!xx#xx$xx%xx|xx&xx;xx-xx/E:xx]xx^0=2/4~110!1@109#48+xx]1$1|0[10&0]48=0^100~xx#xx_xx;xx$xx&xx%xx[xx|0]0-n^xx+xx~xx=xx@xx$xx!xx%xx#xx|xx|xx-xx&xx&xx+xx[xx;xx]xx;xx~xx~xx^xx^xx@xx[xx#xx=xx!xx~xx+xx!xx^xx/F:A4#9#0-2/4$110$1+40%18;xx/G:xx_xx/H:xx_xx/I:12_12/J:2~2@3
21818181 32727272 s@sil^sil-sil+pau=g_00%00^00_00~00-1!1[xx$xx]xx/A:xx-xx-xx@xx~xx/B:1_1_1@xx|xx/C:2+1+1@JPN&0/D:xx!xx#xx$xx%xx|xx&xx;xx-xx/E:xx]xx^0=2/4~110!1@109#48+xx]1$1|0[10&0]48=0^100~xx#xx_xx;xx$xx&xx%xx[xx|0]0-n^xx+xx~xx=xx@xx$xx!xx%xx#xx|xx|xx-xx&xx&xx+xx[xx;xx]xx;xx~xx~xx^xx^xx@xx[xx#xx=xx!xx~xx+xx!xx^xx/F:A4#9#0-2/4$110$1+40%18;xx/G:xx_xx/H:xx_xx/I:12_12/J:2~2@3
32727272 43636363 p@sil^sil-pau+g=e_00%00^00_00~00-1!1[xx$xx]xx/A:xx-xx-xx@xx~xx/B:1_1_1@xx|xx/C:2+1+1@JPN&0/D:xx!xx#xx$xx%xx|xx&xx;xx-xx/E:xx]xx^0=2/4~110!1@109#48+xx]1$1|0[10&0]48=0^100~xx#xx_xx;xx$xx&xx%xx[xx|0]0-n^xx+xx~xx=xx@xx$xx!xx%xx#xx|xx|xx-xx&xx&xx+xx[xx;xx]xx;xx~xx~xx^xx^xx@xx[xx#xx=xx!xx~xx+xx!xx^xx/F:A4#9#0-2/4$110$1+40%18;xx/G:xx_xx/H:xx_xx/I:12_12/J:2~2@3
43636363 47727272 c@sil^pau-g+e=N_00%00^00_00~00-1!2[xx$1]xx/A:xx-xx-xx@xx~xx/B:2_1_1@JPN|0/C:1+1+1@JPN&0/D:xx!xx#xx$xx%xx|xx&xx;xx-xx/E:A4]9^0=2/4~110!1@40#18+xx]1$4|0[10&0]48=0^100~1#12_0;38$0&168%0[100|0]0-n^xx+xx~xx=xx@xx$xx!2%xx#5|xx|24-xx&xx&xx+xx[xx;xx]xx;xx~xx~xx^xx^xx@xx[xx#xx=xx!xx~xx+p0!xx^xx/F:A4#9#0-2/4$110$1+13%6;xx/G:xx_xx/H:12_12/I:11_11/J:2~2@3
```











[返回](/nnsvs-zh-translate/)