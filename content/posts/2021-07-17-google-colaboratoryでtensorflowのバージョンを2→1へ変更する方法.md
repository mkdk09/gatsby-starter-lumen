---
template: post
title: Google ColaboratoryでTensorFlowのバージョンを2→1へ変更する方法
slug: TensorFlow
socialImage: /media/cpu.svg
draft: false
date: 2021-07-17T05:52:42.090Z
description: Google ColaboratoryでTensorFlowのバージョンを2→1へ変更する方法について書いていきたいと思います。
category: TensorFlow
tags:
  - TensorFlow
  - ""
---
Google ColaboratoryでTensorFlowのバージョンを2→1へ変更する方法について書いていきたいと思います。

ネット上にあるTensorFlowやKerasで書かれたコードを動かして見たいと思った時、私はGoogle Colaboratory上で実装してコードの実行結果などを確認しています。

しかし、Google Colaboratory上のTensorFlowのバージョンと、ネット上のコードのTensorFlowのバージョンが一致せずコードを動かせないということが多々あります。

Google Colaboratory上のTensorFlowのバージョンは現在は2.xですが、数年前に書かれたコードのTensorFlowのバージョンは1.xになっていることがほとんどです。

コードをバージョン2.xに対応したものに書き換えることができれば動かせるのですが、Google Colaboratory上ですとコードの編集が難しかったり、時間がかかったりで非常に面倒です。

そこで、Google Colaboratory上のTensorFlowのバージョンを2.xから1.xに変更する方法で対応します。

## 対処法1
最初の方法はpip install を使ってTensorFlowのバージョンを強引に1.xに下げてしまう方法です。
```
!pip install tensorflow==1.15
```
これでバージョンを確認すると、
```
import tensorflow as tf
print(tf.__version__)
```
`1.15.0` のようにバージョンの変更が行えます。

pip install をする前に
import tensorflow as tfを実行してしまった場合は、
pip uninstallでアンインストールを行なった後に、tensorflow==1.15をインストールすることでバージョン変更ができます。
```
!pip uninstall -y tensorflow
!pip install tensorflow==1.15
```

## 対処法2
もう一つの方法は使用するバージョンを明示的に切り替える方法です。
Google Colaboratory上にはバージョン2.xだけでなくバージョン1.xもインストール自体はされています。
そこで、バージョン1.xに切り替えるコマンドを使用することによって解決できます。
```
%tensorflow_version 1.x
```
このコードをセルに入力し実行することで、
```
import tensorflow as tf
print(tf.__version__)
```
`1.15.2`のようにバージョンの変更が行えます。

先ほどと同じように先にTensorFlowをインポートしてしまった場合は、ノートブックのランタイムを再起動することで対処できます。

また、バージョン1.xからバージョン2.xに変更したい時には、
```
%tensorflow_version 2.x
```
とすることでバージョン2.xに切り替えることができます。

## 参考文献
[Google Collaboratory で tensorflowのバージョンを変更する方法 | PRGLOG](https://prglog.info/home/?p=22)

[【2021年最新版】Google ColaboratoryのTensorFlowバージョンを変更する(1.X←→2.X)](https://www.servernote.net/article.cgi?id=google-colab-change-tensorflow-version)

[The %tensorflow_version magic - Colaboratory](https://colab.research.google.com/notebooks/tensorflow_version.ipynb)