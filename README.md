
[![test](https://github.com/ReiHide/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/ReiHide/mypkg/actions/workflows/test.yml)

# mypkg
千葉工業大学ロボットシステム工学講義内で使用したROS2のパッケージを管理するリポジトリ

## インストール方法
ROS2がるよう可能な環境で
~~~
git clone https://github.com/ReiHide/mypkg.git
~~~
と入力する

##ノード

###talker.py
listener.pyに1,2,3,...と数字を送るパブリッシャ
###listener.py
talker.pyから送られた内容を標準出力するサブスクライバー

##実行例
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
