# Reminder_data_from_ambiguous_information

曖昧な情報でリマインド用のデータを作ります。日本語のみ対応です

## 概要

リマインダを作る際に、"色々聞かれて入力が面倒くさい !"、"そのぐらい察してくれよ ! " と思ったことはないですか?そんな時、これを使えば、日本語の曖昧な表現を年月日に変更してくれます。

例えば、

- 来週の火曜日は誕生日 → ('2021', '11', '02', '7', '0', '誕生日')
- 12 月 15 日 8 時から誕生日 → ('2021', '12', '15', '8', '0', '誕生日')
  といった感じです

## 依存するライブラリ

pendulum で時間の計算をしていので、pendulum を入れてください

```
conda install pendulum
or
pip install pendulum
```

## 使い方

このリポジトリの"remind_make.py"を好きなフォルダに落として、python から呼び出しで、下記を実行すると、out に結果のタプルが入ります。

```
import remind_make
out = remind_make.main("12月15日8時から誕生日",pendulum.now())
```

## 注意

無い情報の補填は、完全に自分用です! 気に入らなければ適当にモディファイくださいまし
※時間が入ってなければ、勝手に朝の 7 時としたり、、、など
