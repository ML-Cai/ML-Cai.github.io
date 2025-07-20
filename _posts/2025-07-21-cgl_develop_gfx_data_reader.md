---
title: Cross Gate resource format and GraphicDataViewer tool
date: 2025-07-21 00:30:00 +0800
author: <menglcai>
categories: [CrossGate-Legacy]
tags: [CrossGate-Legacy]

image:
  path: /assets/lib/20250721_GraphicsDataViewer_preview.png

---

## GraphicsDataViewer tool

CGL proejct had submit a simple graphics data viewer: https://github.com/ML-Cai/CrossGate-Legacy/tree/dev/bin/GraphicsDataViewer

The GraphicsDataViewer is a simple Gradio-based web application for previewing graphics data from the classic game Cross Gate using palettes and data provided by the cgl backend module.

According to the `GraphicInfo*_*.bin`, `Graphic*_*.bin`, `Palet*_*.bin` formats from cgsword ([link](https://cgsword.com/filesystem_graphicmap.htm)), I have submitted resource-related classes to [CrossGate-Legacy](https://github.com/ML-Cai/CrossGate-Legacy/tree/dev/include/cgl/resources)


## Resource format : "GraphicInfo*_*.bin" and "Graphic*_*.bin"
--------------------

Data format are referenced from cgsword ([link](https://cgsword.com/filesystem_graphicmap.htm)). The data format described by cgsword is detailed, and I just followed its style to design my own implementation.

However, from CrossGate PUK2 (樂園之卵) and newer versions, the graphic data is updated with a private palette, and it is not yet supported in the current implementation.

![preview](/assets/lib/20250721_cgsword_GraphicInfo_fmt.png)

![preview](/assets/lib/20250721_cgsword_GraphicData_fmt.png)

![preview](/assets/lib/20250721_cgsword_run_length_fmt.png)

## Resource format : "Palet*_*.bin"
--------------------

Data format are referenced from cgsword ([link](https://cgsword.com/filesystem_graphicmap.htm))

![preview](/assets/lib/20250721_cgsword_palet_fmt.png)


