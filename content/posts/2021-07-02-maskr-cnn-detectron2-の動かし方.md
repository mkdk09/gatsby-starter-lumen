---
template: post
title: MaskR-CNN(Detectron2)の動かし方
slug: MaskR-CNN
socialImage: /media/cpu.svg
draft: false
date: 2021-07-02T14:12:00.000Z
description: |-
  MaskR-CNN(Detectron2)の動かし方(環境構築から実行まで)
  についてを書いていきたいと思います。
category: MaskR-CNN
tags:
  - MaskR-CNN
  - ""
---
MaskR-CNN(Detectron2)の動かし方(環境構築から実行まで)
についてを書いていきたいと思います。

## 環境構築

`pip install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html`

`pip install pyyaml==5.1`

`pip install opencv-python`

`python -m pip install -e detectron2`

`cd detectron2/demo`

## 参考文献
[Previous PyTorch Versions | PyTorch](https://pytorch.org/get-started/previous-versions/)(PyTorchの過去のバージョンをダウンロード)

[detectron2/INSTALL.md at master · facebookresearch/detectron2](https://github.com/facebookresearch/detectron2/blob/master/INSTALL.md)(Detectron2をインストール)