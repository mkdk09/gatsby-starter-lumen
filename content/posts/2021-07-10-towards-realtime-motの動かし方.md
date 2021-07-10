---
template: post
title: Towards-Realtime-MOTの動かし方
slug: PyTorch
socialImage: /media/cpu.svg
draft: false
date: 2021-07-10T12:35:26.441Z
description: Towards-Realtime-MOTの動かし方(環境構築から実行まで)についてを書いていきたいと思います。
category: PyTorch
tags:
  - PyTorch
  - ""
---
[Towards-Realtime-MOT](https://github.com/Zhongdao/Towards-Realtime-MOT)の動かし方(環境構築から実行まで)についてを書いていきたいと思います。

## Towards-Realtime-MOTについて
Towards-Realtime-MOTとは、同時に多数の人物をトラッキングする（Multi-Object Tracking）モデルです。  
PyTorchベースで実装されています。

## 環境構築
基本的に[こちら](https://colab.research.google.com/drive/1PANKX9WETfYfa2pol7k4OwH22PESnWjh#scrollTo=C4aP95dtcvLC)のGoogleColab通りに構築していきます。

PyTorchはすでにインストールされている前提で進めます。

### プロジェクトのインストール
```https://github.com/Zhongdao/Towards-Realtime-MOT```

### ライブラリのインストール
こちらもGoogleColab通りにインストールします。

```
!pip install motmetrics
!pip install cython_bbox
!pip install lap
```

上記に加えて、以下のライブラリもインストールします。

```pip install numba==0.48```

## 学習済みモデルのダウンロード

## デモ
```cd Towards-Realtime-MOT```

## 参考文献
[Zhongdao/Towards-Realtime-MOT: Joint Detection and Embedding for fast multi-object tracking](https://github.com/Zhongdao/Towards-Realtime-MOT)(Towards-Realtime-MOT)

[Towards real-time MOT test - Colaboratory](https://colab.research.google.com/drive/1PANKX9WETfYfa2pol7k4OwH22PESnWjh#scrollTo=C4aP95dtcvLC)(Google Colaboratory上での実行例)
