
[![test](https://github.com/ReiHide/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/ReiHide/mypkg/actions/workflows/test.yml)

# mypkg
千葉工業大学ロボットシステム工学講義内で使用したROS2のパッケージを管理するリポジトリ

## インストール方法
ROS2が利用可能な環境で
~~~
git clone https://github.com/ReiHide/mypkg.git
~~~
と入力する

## ノード
#### talker.py
トピックcountupでlistener.pyにメッセージとして1,2,3,...と数字を送るパブリッシャ
#### listener.py
トピックcountupでtalker.pyから送られたメッセージを標準出力するサブスクライバー

## 実行例
#### 1つの端末を使用する方法
* 入力例
~~~
ros2 launch mypkg talk_listen.launch.py
~~~
* 出力例
~~~
[INFO] [launch]: All log files can be found below /home/reizen/.ros/log/2023-01-03-15-59-54-920064-DESKTOP-PIUCHI7-277
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [279]
[INFO] [listener-2]: process started with pid [281]
[listener-2] [INFO] [1672729196.127023200] [listener]: Listen: 0
[listener-2] [INFO] [1672729196.615459400] [listener]: Listen: 1
[listener-2] [INFO] [1672729197.115504000] [listener]: Listen: 2
[listener-2] [INFO] [1672729197.617092100] [listener]: Listen: 3
[listener-2] [INFO] [1672729198.116003800] [listener]: Listen: 4
[listener-2] [INFO] [1672729198.616882600] [listener]: Listen: 5
~~~
終了する場合は ctrl + C
#### 2つの端末を使用する方法
* 入力例

  〇端末1
~~~
ros2 run mypkg talker
~~~

  〇端末2
~~~
ros2 run mypkg listener
~~~
* 出力例
~~~
[INFO] [1672728450.283001100] [listener]: Listen: 141
[INFO] [1672728450.755937000] [listener]: Listen: 142
[INFO] [1672728451.255859200] [listener]: Listen: 143
[INFO] [1672728451.755849200] [listener]: Listen: 144
~~~
終了する場合は ctrl + C
## テスト環境
* Ubuntu20.04

## ROS2のバージョン
* Foxy Fitzroy

## Github Actionsでのテスト
担当講師がセットアップしたコンテナ
~~~
https://hub.docker.com/repository/docker/ryuichiueda/ubuntu22.04-ros2
~~~
を利用してテストを行っています。

## ライセンス
・BSDライセンスが適用されます。詳細は LINCENSE を参照してください。

© 2023 Hideya Reizen
