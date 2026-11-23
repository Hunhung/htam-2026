# 2026.11.22 洞洞板配件3d打印记录 制造万物

[中文](README.md) | [English](README.en.md)

[文件清单](source-inventory.csv)

[双语网页（在线浏览）](https://hunhung.github.io/htam-2026/assignments/assignment-02/print-20261122-bilingual-review.html) · [原文 TXT](source/record-original.txt)

## 背景与作业要求

本次为《制造万物》课程第二次作业，为实验室洞洞板设计并 3D 打印一个针对具体物件的配件。以下记录我选择钳子、测量、绘制草图、建模、打印和安装测试的过程。

- 以实际物件为对象，测量后设计配件。

- 参考老师提供的洞洞板安装几何，考虑 FDM 打印方式。

- 打印后安装到洞洞板上，检查配合和取放情况。

## 1. 设计对象与尺寸测量

我选择了钳子作为我的设计对象。事实上这里我在这里发现了四种不同的钳子，它们只有钳头不同。我希望给他们设计一个可以把枢轴托住的洞洞板配件，同时为了稳固和安全，在上方（钳头的位置）加上一个围栏，保证在钳子可以方便的拿取的时候也可以保证实验室的安全。我测量了钳头的长度和最宽的部分，同时测量了从枢轴的最下部到钳头顶端的长度，以及钳子的厚度。这些数据支撑我设计出来一个尺寸合适的挂钩+围栏。

![选择实验室里的钳子](images/object-choice-1.jpg)

![不同钳型与测量工具](images/object-choice-2.jpg)

![尺寸测量记录 1](images/measure-1.jpg)

![尺寸测量记录 2](images/measure-2.jpg)

![尺寸测量记录 3](images/measure-3.jpg)

![尺寸测量记录 4](images/measure-4.jpg)

![尺寸测量记录 5](images/measure-5.jpg)

## 2. 草图与结构构想

在经过我的分析过后，我画了一个大致的草图。这个设计非常简单，就是在很常见的挂钩的基础上增加了顶部的围栏，但我认为这个设计可以很有效地提供一些安全的保障。配件由两部分组成：挂钩+围栏（这个在后续建模、打印的阶段会继续介绍）。

![挂钩与顶部围栏草图](images/sketch-1.jpg)

![钳子与托架的位置关系](images/sketch-2.jpg)

## 3. Fusion 建模与整体方案

我这次尝试使用了Fusion来建模。我最擅长的建模软件是SketchUp，但是我这次希望尝试一些新的工具，不过Fusion的快捷键和鼠标操作和SU有一些出入，所以对我还有一定的挑战性哈哈哈。原本我把他们建成了一个整体的，但是后续在打印的时候我发现一个是很难找到一个完美的方向进行打印，以达到强度较好的效果，另一个问题则是支撑也较多，打印的时候效果也不理想。

![Fusion 中的整体模型](images/fusion-model.jpg)

![在 Fusion 中调整几何](images/fusion-adjustment.jpg)

## 4. 第一次打印与问题

第一次打印到一半的时候，树状支撑已经出现了问题，于是我暂停了进程。不知道是不是材料的原因，打印出来的模型拉丝了而且强度不高。同时我也发现我第一次建的模型尺寸太小了，因此我重新对我的模型文件进行了调整。

![第一版的切片与支撑](images/slice-first.jpg)

![检查第一版的支撑与悬空位置](images/slice-check.jpg)

![第一次打印过程 2](images/first-print-2.jpg)

![第一次打印产物 1](images/failed-part-1.jpg)

![第一次打印产物 3](images/failed-part-3.jpg)

![第一次打印产物 5](images/failed-part-5.jpg)

<details>

<summary>其余第一次打印照片（7 张）</summary>



![第一次打印过程 1](images/first-print-1.jpg)

![第一次打印过程 3](images/first-print-3.jpg)

![第一次打印过程 4](images/first-print-4.jpg)

![第一次打印过程 5](images/first-print-5.jpg)

![第一次打印产物 2](images/failed-part-2.jpg)

![第一次打印产物 4](images/failed-part-4.jpg)

![第一次打印产物补充记录](images/failed-part-extra.jpg)

</details>

## 5. 拆分组件与榫卯连接

我重新计算了模型需要的尺寸，把我的模型变大了。同时我也重新思考分析了整个挂钩的受力，最终决定把模型拆成两个组件：挂钩和围栏。原本我的挂钩是竖直打印出来，这样的成品强度会相对较低，所以我将挂钩平放。在挂钩和围栏的连接处，我设置了一个简单的榫卯结构，并且考虑实际打印地误差和可能地磨损，在 X 方向留出了单边 0.15 mm、Y 方向留出了单边 0.20 mm 的间隙，让成品可以轻松地安装，也比较稳固。

![围栏与挂柱的销孔配合](images/joint.jpg)

## 6. 切片与第二次打印

打印的时候，首先是把成品的建模文件分别导出stl文件，然后放在一个Bambu切片的文件里面，调整好摆放的方向，选择对应的打印机型号（第一次我忘记了选择对应型号，所以还重新切片了一次），因为H2D是双喷头的设置，所以还可以根据自己的需要选择左侧或者右侧的喷头。选择好之后切片、查看支撑、导出单盘切片文件（.gcode.3mf格式的文件）就可以准备打印了。打印的时候可以查看需要的时间和耗材克重，只需要耐心等待就可以了~

![选择对应的打印机型号](images/printer-selection.jpg)

![两个零件分别摆放后的切片记录](images/slice-two-parts.jpg)

![第二次打印的设备记录](images/second-print.jpg)

## 7. 成品与安装测试

最终的成品在从打印机里取出来的时候，是将打印的底座垫子取出，轻轻弯折垫子让3d打印产品从底部剥落，然后就可以轻松取下完好的产物。我将它放在了洞洞板上测试，整体比较合适，不过在榫卯结构的位置，或许再多测试不同的空隙大小、打磨方式和耗材之后可以得到更好的更适合的产物，这个必定是需要经过多轮实测的。

![挂钩单独安装在洞洞板上](images/finished-1.jpg)

![挂钩与围栏组装后的空载状态](images/finished-4.jpg)

![装入钳子后的正面状态](images/finished-2.jpg)

![装入钳子后的另一角度](images/finished-3.jpg)

## 文件下载

| 文件 | 内容 |
| --- | --- |
| [最终版围栏 STL](models/01-fence.stl) | 围栏独立零件 |
| [最终版挂柱钩子 STL](models/02-post-hook.stl) | 挂柱、立板与钩子独立零件 |
| [第一版整体模型 STL](models/first-version.stl) | 用于对比第一次方案 |
| [尺寸图 PDF 审查版](downloads/cad-review-a.pdf) | 装配、零件三视图和连接剖面，共 4 页 |
| [二维 DXF 审查版](downloads/cad-review-a.dxf) | 可继续编辑的二维线稿 |
| [原始 Word 记录](source/print-diary-original.docx) | 保留作者提交的原始文档 |
| [原始中文 TXT](source/record-original.txt) | 原始中文全文 |
| [间隙数值更正后的 TXT](source/record-corrected.txt) | 更正已确认的孔销间隙数值 |
| [原始素材对应清单](source-inventory.csv) | 32 张照片与原文件的对应关系 |

尺寸图为先前制作的审查版，依据最终打印 STL 生成，尚未作为 Fusion 原生关联工程图确认。最新版 Fusion 原生模型与对应的最终切片文件将在版本核对后补充。
