# 2026.11.16 制造万物 · Assignment 1 · 3D 扫描记录

[中文](README.md) | [English](README.en.md)

[文件清单](source-inventory.csv)

[双语网页文件](scan-20261116-bilingual-review.html) · [原文 TXT](source/record-original.txt)

## 背景与作业要求

本次为《制造万物》课程第一次作业，主题为 Digital Bodies: Scan, Mix & Modify。以下记录我在 2026 年 11 月 16 日进行扫描、初步拼合和模型导出的过程。

- 至少将一个 3D 扫描结果与另一个三维模型组合。
- 清理和修复网格，为 3D 打印做好准备；本次不要求实际打印。
- 记录扫描、编辑、相关数字文件，以及过程中的问题和心得。

## 1. 设备连接与软件版本

revo scan连接的时候，遇到了连接不上的问题，尝试了usb和typec接入电脑之后，发现是app的版本问题。我在fablab实验室使用的是pop2的机型，但是下载的是不适配的Revo scan6。重新下载了revo scan5之后，成功连接上了。

![扫描仪扫描 (16)](images/setup.jpg)

![连接电脑阶段 (3)](images/device-view.jpg)

![连接电脑阶段 (4)](images/cables.jpg)

![连接电脑阶段 (11)](images/connection.jpg)

![连接电脑阶段 (8)](images/software-download.jpg)

![连接电脑阶段 (7)](images/version.jpg)

## 2. 扫描仪的不稳定表现

很可惜的是，扫描仪似乎从今天中午开始出现了一些问题，在扫描的时候，非常的不稳定，而且最终的效果不尽人意。它今天无法稳定地扫描光滑的表面，扫描出来的表面像泥泞的地面，细节全部丢失了，而且还出现了表面断层、位移的问题。在云图阶段，扫描到的点的数量明显不够，一键处理之后的效果也是很恶心的。

![扫描仪扫描 (12)](images/scan-setup-2.jpg)

![扫描仪扫描 (13)](images/scan-setup-3.jpg)

## 3. 石膏像与鼠标的扫描结果

我尝试扫描了实验室里的小石膏模型，但是人的面部的精细度极差，几乎看不出来是人脸了。然后我选择了我的鼠标作为扫描的对象，它本来是一个光滑的曲面表面，但是扫描出来的结果像一只癞蛤蟆。我先正着放置在圆盘上扫描了鼠标的上部，然后把鼠标的底面朝上，扫描了它的底部。其中都存在细节错误和丢失的问题。我原本的计划是把正面和底部的两次扫描结果进行拼合，最终得到一整个完整的模型，但是由于模型的细节和精准度上存在问题，最后并没有得到较满意的结果。

![失去的面部细节](images/face.jpg)

![失败的石膏模型 (1)](images/plaster-side.jpg)

![失败的石膏模型 (2)](images/plaster-front.jpg)

![错位的石膏模型](images/offset.jpg)

![不平整的鼠标模型](images/mouse-cloud.jpg)

![不平整的鼠标模型 (1)](images/mouse.jpg)

![不平整的鼠标模型 (3)](images/mouse-other.jpg)

## 4. 鼠标模型对齐尝试

对齐的过程我尝试选择相同的节点，但是模型精度较低，而且存在一定的错位的情况，对齐效果并没有我想象中的好。

![拼合模型 (1)](images/alignment.jpg)

![拼合模型 (2)](images/alignment-alt.jpg)

## 5. 手机端 Revo Scan 连接

同时我也尝试使用了手机端的revo scan，但是在连接上存在问题，推测是接触不良，总之一直无法稳定连接。不过考虑到扫描仪的故障，也就没有继续尝试了。

![扫描仪扫描 (9)](images/mobile-revo.jpg)

## 6. 改用 RealityScan 与更换对象

最终我选择了尝试使用手机端的reality scan进行拍照+生成3d模型的尝试。手机端的reality scan的说明指出：这个app比较使用于食品、毛绒或是自然表面的扫描，而并不太适用于光滑平坦的表面。这里我推测的原因是通过照片分析3d数据并不能做到像扫描仪那样通过结构光和激光精准的定位，所以得到的模型表面也比较粗糙。但是这个app的优势在于他的贴图非常精美，可以精确的把照片里的物品的材质和细节通过贴图的方式展示上去，所以最后的产物至少从视觉上来说是美观的。但是实际的模型仍然需要后续的打磨。这也是我为什么最后更换了我扫描的对象，选择了毛绒玩具，他的表面更加不平坦。

![手机扫描鼠标 (2)](images/phone-mouse.jpg)

![手机扫描鼠标 (4)](images/phone-mouse-alt.jpg)

![手机扫描操作 (1)](images/phone-start.jpg)

![手机扫描操作 (2)](images/capture.jpg)

## 7. 拍摄、补光与点云检查

使用reality scan的时候，首先是选择了object mode，也是把物体放在平面上，通过连续手动或者自动拍照的方式，拍摄全方位的照片。这里要注意的是，拍摄的照片需要具有连续性且清晰完整，否则之后会出现大量的unconnected的内容。我在初次拍摄了72张照片之后生成的云点图观察到，暗部存在很多空缺。我尝试做了一些补光和重新拍摄，补上了一部分的暗部内容，但是实际上最后我认为还是应该在初期就准备好完整的光源，确保物体的每个面都能被较好读取。我在补充的暗部的内容的位置，由于做了补光，所以在明暗交接处有不自然的部分。这是我这次认为做得还不够好的地方。

![手机扫描操作 (3)](images/phone-generation.jpg)

![手机扫描操作 (4)](images/cloud.jpg)

![手机扫描操作 (6)](images/phone-cloudprogress.jpg)

![手机扫描操作 (7)](images/unconnected.jpg)

## 8. 模型生成、导出与白模对照

最后，在经过四五次的云点图检查之后，我生成了模型。在生成的选择上我选择了water-tight mesh，这样得到的模型会是一个完整的模型（缺少细节的部分由算法智能填补），为了得到较好的结果我也选择了较高质量和8k质量的贴图。得到的结果在材质上有着很不错的视觉效果，而白模确实存在一些粗糙的表面和细节，后续我将会继续修改优化。

![手机扫描操作 (5)](images/settings.jpg)

![手机扫描操作 (8)](images/phone-completed.jpg)

![微信图片_20261116232548_837_63](images/result.jpg)

![白模](images/white.jpg)

## 9. 在 Blender 中整理模型和添加底座

> **当前状态：半成品，还需要继续调整。** Blender 里的清理和缩放还没做完——扫描时垫的那块底板没有删掉，模型与底座的接合处也留着重叠面，尺寸和位置都还需要再调。这一版只是阶段性成果，之后会重新整理并导出。

我把扫描得到的模型导入 Blender，自己手动做了一些简单的整理：尝试清理多余的部分、调整模型的大小，并让表面尽量平滑一些。处理之后，模型看起来比刚导出时整齐了一些，不过表面还是比较粗糙，有些细节也没能保留下来。

然后我给模型加了一个简单的长方形底座，调整它们的位置，把扫描模型和底座组合在一起，做成一个小展示件。最后保存了 Blender 工程，并导出了 STL 文件。

下面是模型处理前后的对比和组合后的预览图。

| 原始扫描 | 清理和缩放后 |
| --- | --- |
| ![原始扫描网格](images/model-raw.jpg) | ![清理后的网格](images/model-clean.jpg) |

| 独立简化底座 | 组合展示件 |
| --- | --- |
| ![独立长方体底座](images/model-base.jpg) | ![组合件斜视图](images/model-final-iso.jpg) |

| 正面 | 背面 | 顶面 |
| --- | --- | --- |
| ![正面](images/model-final-front.jpg) | ![背面](images/model-final-back.jpg) | ![顶面](images/model-final-top.jpg) |

## 文件下载

> 下表模型文件均为当前半成品版本，清理和缩放完成后会更新。

| 文件 | 内容 |
| --- | --- |
| [最终组合 STL（ZIP）](downloads/display-piece.zip) | 模型与底座组合后的 STL 文件 |
| [清理后的主体 STL（ZIP）](downloads/clean-model.zip) | 保留缩放后的主体 |
| [独立简化底座 STL](models/processed/02_plinth_base.stl) | 单独提供的简单长方体底座 |
| [RealityScan 原始成果（ZIP）](downloads/realityscan-original.zip) | Rei.obj、Rei.mtl 和两张原始 8K 贴图；解压后保持同一文件夹 |
| [POP2 扫描 03（ZIP）](downloads/pop2-scan-03.zip) / [扫描 04（ZIP）](downloads/pop2-scan-04.zip) | 两个原始 PLY 扫描成果 |
| [Blender 组合工程（ZIP）](downloads/blender-project.zip) | 保存的 Blender 工程；最终导出模型见上方 STL 下载 |
| [原始 Word 记录](source/scan-diary-original.docx) | 本文中文原文 |
| [原始素材清单](source-inventory.csv) | 扫描素材的原始文件清单 |

原始照片、视频和 Revo Scan 工程保存在本地。上表提供扫描成果和模型文件下载。
