# mypkg_2023
ロボットシステム学の練習用リポジトリです。

[![test](https://github.com/shirakawasojyu/mypkg_2023/actions/workflows/test.yml/badge.svg)](https://github.com/shirakawasojyu/mypkg_2023/actions/workflows/test.yml)

##パッケージのコピー方法について
1. ホームディレクトリに移動して以下のコマンドを実行してください。

###githubアカウントを持っている人
```
$ git clone git@github.com:shirakawasojyu/mypkg_2023.git
```

###githubアカウントを持っていない人
```
$ git clone https://github.com/shirakawasojyu/mypkg_2023.git
```

## ビルド方法について

1. このリポジトリをcloneしたら、
```
$ cd ~/mypkg_2023
```
でmypkg_2023へ移動してください。


2. 以下のコマンドを実行してください。パッケージの内容がビルドされます。
```
$ colcon build
```

3.次に設定などを読み込ませます。
```
$ source ~/.bashrc
```

4.以上でビルドは終了です。以下の機能から実行を行えるようになります。
 

## 機能について

* **talker.py**
数字を0.5秒ごとにカウントし、`talker`というトピック名でトピック通信を行うノードです。
実行の際には以下のコマンドを入力してください。

```
$ ros2 run mypkg talker
```

* **listener.py**
`listener`というトピック名でトピック通信を行うノードであり、前述の`talker.py`からメッセージを受信し、表示する機能があります。
実行の際には、端末を2つ用意し、片方の端末で`talker.py`, もう片方の端末で`listener.py`を実行してください。
実行コマンドは以下のようになります。

```
$ ros2 run mypkg listener
```
* **talk_listen.launch.py**
前述の`talker.py`と`listener.py`の2つのノードを同時に実行できるノードです。
実行する際には以下のコマンドを実行してください。
終了したいときは`Ctrl + C`を入力すると終了します。

```
$ ros2 launch mypkg talk_listen.launch.py
```
## ソフトウェア
・Python Ver3.7 ～ 3.10

## テスト環境
ubuntu22.04.2 LTS

## ライセンス
・このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布及び使用が認められます。
・©2023 ShirakawaSojyu


