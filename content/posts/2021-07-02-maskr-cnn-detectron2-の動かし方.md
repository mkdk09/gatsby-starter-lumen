---
template: post
title: Mask R-CNN(Detectron2)の動かし方
slug: MaskR-CNN
socialImage: /media/cpu.svg
draft: false
date: 2021-07-09T13:10:41.885Z
description: |-
  MaskR-CNN(Detectron2)の動かし方(環境構築から実行まで)
  についてを書いていきたいと思います。
category: MaskR-CNN
tags:
  - MaskR-CNN
  - ""
---
Mask R-CNN([Detectron2](https://github.com/facebookresearch/detectron2))の動かし方(環境構築から実行まで)についてを書いていきたいと思います。

## Detectron2について
Detetron2とは、Facebook AI Research が開発したコンピュータビジョンのライブラリです。  
主にPyTorchベースの物体検出のライブラリを提供しています。

## Mask R-CNNについて
Mask R-CNNとは、物体検出(Object Detection)と物体のセグメンテーション(Object Segmentation)を同時に行うマルチタスクの手法です。

## 環境構築

### PyTorchのインストール
PyTorchベースの手法なのでPytorchをインストールします。  
バージョンには気をつけてください。

`pip install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html`

Pytorchの過去のバージョンは[こちら](https://pytorch.org/get-started/previous-versions/)から調べました。

### pyyamlのインストール
主にモデルの構造やパラメータなどはyamlファイルで設定されているのでpyyamlをインストールします。

`pip install pyyaml==5.1`

### OpenCVのインストール
映像や画像を扱うのでOpenCVもインストールします。  
ここではビルドなどをする必要がなくpipからインストールで大丈夫です。

`pip install opencv-python`

### Detectron2のインストール
ここでDetectron2本体のインストールを行います。
`python -m pip install -e detectron2`

## デモ
`cd detectron2/demo`

## 参考文献
[Previous PyTorch Versions | PyTorch](https://pytorch.org/get-started/previous-versions/)(PyTorchの過去のバージョンをダウンロード)

[detectron2/INSTALL.md at master · facebookresearch/detectron2](https://github.com/facebookresearch/detectron2/blob/master/INSTALL.md)(Detectron2をインストール)