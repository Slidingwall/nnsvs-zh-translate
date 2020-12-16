# 如何使用utau2db

如何使用

## 步骤

1.  用MIDI或MusicXML创建一个UST。
2.  在UTAU中编辑UST。不做「っ」的原音设定似乎会很不方便。
3.  运行utau2db。
4.  检查生成的标签。
5.  与MusicXML生成的LAB进行比较。

### UTAU的步骤

1.  用插件「おま☆かせ2020」制作连续音。（先行发生请使用100）
2.  如果您需要的话，可以进行调校。
3.  全选，执行本体机能「パラメータ自動調整」（将STP等写入UST）。
4.  如果您需要的话，编辑STP和重叠。
5.  导出UST的歌声。

### ust2db的步骤

1.  运行`python ust2db.py`。
2.  指定UST所在的文件夹。
3.  生成LAB。仔细阅读错误的输出。
4.  setParam使用的ini也会输出，这样就会看到LAB了。

### 检查标签

1.  用oto2lab的lab_invalid_time工具进行检查。
2.  用oto2lab的generate_label_from_musicxml工具生成LAB进行对比。
3.  用oto2lab的lab_set_start_sil工具统一开头的休止符。

### NNSVS的步骤

1. 用oto2lab的ust_bpm_and_range工具检测音域。

2. 在nnsvs的config.py写入频率范围（根据音域推算）。

3. 祝你好运

   

   

   

   

   [返回](/nnsvs-zh-translate/)
