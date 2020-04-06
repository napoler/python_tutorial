---
description: 中文自然语言处理 (NLP) 标注工具
---

# 文本标注工具

{% embed url="https://github.com/t-web/ChineseAnnotator" %}





中文自然语言处理 \(NLP\) 标注工具，与 有志之士 共同 促进 中文 自然语言处理 的 发展。

### 一、关于

* 这个项目最原始的代码是从 YEDA fork 过来的，访问 [YEDA](https://github.com/jiesutd/YEDDA) 项目，了解更多信息
* 这 **不是** 一个 web 应用，而是一个基于 Python tkinter 的轻量级桌面端应用
* 本项目仅支持 Python 3.x，**不考虑** 兼容 Python 2.x
* 本项目目前仅支持实体标注，未来将加入更多功能

### 二、使用指南

#### 安装 Python 3.x

#### 下载本项目

`git clone https://github.com/SophonPlus/ChineseAnnotator.git` 或直接下载 [压缩包](https://github.com/SophonPlus/ChineseAnnotator/archive/master.zip) 并解压

#### 开始标注

[![alt text](https://github.com/SophonPlus/ChineseAnnotator/raw/master/EnglishInterface.png)](https://github.com/SophonPlus/ChineseAnnotator/blob/master/EnglishInterface.png) [![alt text](https://github.com/SophonPlus/ChineseAnnotator/raw/master/ChineseInterface.png)](https://github.com/SophonPlus/ChineseAnnotator/blob/master/ChineseInterface.png)

* 执行 `python YEDDA_Annotator.py`，启动标注程序
* 在标注程序界面的右侧，设置快捷键，如 `a: Action; b: Loc; c: Cont`
* 点击 `ReMap` 按钮，保存快捷键设置
* 点击 `Open` 按钮，选择文件 \(后缀必须为 .txt 或 .ann\)
* 选中文本，然后使用设置好的快捷键进行标注，标注格式形如 `[@the text span＃Location*]`
* 通过 `RMOn` 和 `RMOff` 按钮，可以开启或关闭智能推荐
* 智能推荐会根据已经手动标注的数据，自动标注未标注的数据。其格式为 `[$the text span＃Location*]`，并用绿色展示出来（注意：手动标注以 `[@` 打头，而推荐标注则以 `[$` 打头）
* 标注结果与原始文件保存在同一个目录中，文件名为 _**"原文件名 + .ann"**_

#### 管理标注工作

[![alt text](https://github.com/SophonPlus/ChineseAnnotator/raw/master/AdminInterface.png)](https://github.com/SophonPlus/ChineseAnnotator/blob/master/AdminInterface.png)

* 执行 `python YEDDA_Admin.py`，启动管理程序
* 点击 `多人标注分析`，然后选择多个 `*.ann` 文件，会给出不同标注结果的 F 值矩阵 [![alt text](https://github.com/SophonPlus/ChineseAnnotator/raw/master/resultMatrix.png)](https://github.com/SophonPlus/ChineseAnnotator/blob/master/resultMatrix.png)
* 点击 `配对比较`，然后选择 2 个 `*.ann` 文件，会生成相应的对比报告 \(报告为 `.tex` 格式，可以进一步编译为 `.pdf` 文件\)。示例 pdf 报告如下：

[![alt text](https://github.com/SophonPlus/ChineseAnnotator/raw/master/detailReport.png)](https://github.com/SophonPlus/ChineseAnnotator/blob/master/detailReport.png)

#### 其他（重要）功能

1. 按 `ctrl + z` 撤销最近 1 次的修改
2. 选择已经标注的实体，或将光标置于已标注的实体范围内，按其他实体类别的快捷键 \(如 `x`\) 更新实体类别 \(与 `x` 对应的实体\)，按 `q`，删除实体标注
3. 选择已标注的文本，如 `[@美国＃Location*]`, 再按 `q`, 删除实体标注，即恢复到未标注的状态 \(如"美国"\)
4. 确认/删除推荐标注的实体：将光标置于推荐标注的实体范围内，按 `y` \(确认\)，按 `q` \(退出\)
5. 点击 `export` 按钮，会将 _**".ann"**_ 文件导出为同名的 _**".anns"**_ 文件（存放在同一目录下）。导出文件为序列标注的格式。

* 源代码中，参数 `self.seged` 用于控制导出的行为。如果句子由空格间隔的单词构成（英文或已分词的中文），则该值应设置为 `True`，否则应设置为 `False`（如未分词的中文）
* 另一个参数 `self.tagScheme` 控制导出的格式，_**".anns"**_ 文件将使用 `BMES` 格式，如何该值为 `"BMES"`，否则导出格式为 `"BIO"`

