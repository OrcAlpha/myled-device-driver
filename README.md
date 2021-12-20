# **myled-device-driver**
千葉工業大学
未来ロボティクス学科2年後期
 
ロボットシステム学課題
 
講義動画：ロボットシステム学第7回～第8回(<https://www.youtube.com/watch?v=xQW8-FNuboo>)を見ながら作成
## コードについて
千葉工業大学　未来ロボティクス学科准教授　上田隆一先生のコード(<https://github.com/ryuichiueda/robosys_device_drivers.git>)の一部を改変したものです。

## オリジナルの変更点
* /dev/myled0　をcatしたときの出力文字を変更。
 
* LED点灯のパターンを追加。

## デモ映像

## 動作確認環境
OS ...Ubuntu 20.04 LTS
 
ハード...Raspberry Pi4

## 利用方法
* ハードのセッティング
 
　LEDのアノードをGPIO25ピンに繋ぎ、カソードをGNDに接続する。LEDには200Ω程度の抵抗を挟むことが理想である。
* コンパイル
 
```$ make```
* インストール

```$ sudo insmod myled.ko```
* 権限の設定
 
 ```$ sudo chmod 666 /dev/myled0``` 
* LEDの点灯
 
 ```$ echo (0~9,-) > /dev/myled0```
* アンインストール

```$ sudo rmmod myled```
 
```$ make clean```

## ライセンス
GPL3.0

## 参考
READMEの書き方(<https://laraweb.net/surrounding/7477/>)
