# mypkg_2023
ロボットシステム学の練習用リポジトリです。

[![test](https://github.com/shirakawasojyu/mypkg_2023/actions/workflows/test.yml/badge.svg)](https://github.com/shirakawasojyu/mypkg_2023/actions/workflows/test.yml)

## 機能について

* **talker.py**

数字を0.5秒ごとにカウントし、`/countup`というトピックを通じてトピック通信を行うノードです。  
実行の際には以下のコマンドを入力してください。  
実行後画面には出力されません。後述の`listener.py`を参照してください。  
終了したいときは`Ctrl + C`で終了できます。

```
$ ros2 run mypkg talker
```

* **listener.py**

`/countup`というトピックからメッセージを貰うトピック通信を行うノードであり、前述の`talker.py`からメッセージを受信し、表示する機能があります。  
端末を2つ用意し、片方の端末で`talker.py`, もう片方の端末で`listener.py`を実行するとtalker.pyからのメッセージが表示されます。  
実行コマンドは以下のようになります。  
終了したいときは`Ctrl + C`で終了できます。

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

### 実行例
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/shirakawa/.ros/log/2023-12-23-16-55-51-405332-shirakawa-sojyu-1121
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [1122]
[INFO] [listener-2]: process started with pid [1124]
[listener-2] [INFO] [1703318152.251958001] [listener]: Listen: 0
[listener-2] [INFO] [1703318152.719450423] [listener]: Listen: 1
[listener-2] [INFO] [1703318153.218974133] [listener]: Listen: 2
[listener-2] [INFO] [1703318153.719072942] [listener]: Listen: 3
[listener-2] [INFO] [1703318154.219194220] [listener]: Listen: 4
[listener-2] [INFO] [1703318154.719067560] [listener]: Listen: 5
```
## ソフトウェア
* Python   
  * テスト済み：Ver3.7 ～ 3.10

## テスト環境
 * Ubuntu22.04.2 LTS

## ライセンス
* このパッケージは、下記のスライド、コードを参照し、本人の許可を得て自身の著作としたものです。  
  * https://github.com/ryuichiueda/mypkg  
  * https://github.com/ryuichiueda/my_slides/blob/master/robosys_2022/lesson8.md  
  * https://github.com/ryuichiueda/my_slides/blob/master/robosys_2022/lesson9.md  

* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布及び使用が認められます。  
* ©2023 ShirakawaSojyu


