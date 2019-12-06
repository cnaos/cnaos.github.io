# cnaos's github pages

これまでにつくったもの

# 環境センサViewer

AndroidでOmronの環境センサ2JCIE-BL01の測定データの読み取り、測定データのグラフ表示、測定データのエクスポートができるアプリです。

環境センサ2JCIE-BL01を使ったデータ観測の例では、環境センサの動作モードをデータ保存なしのビーコンモード(IM/EP)に変更して観測する例が多いのですが、他のアプリとの同時利用も想定してデータ保存ありのモードでの運用ができるようにしました。


[環境センサViewer(Google Play)](https://play.google.com/store/apps/details?id=io.github.cnaos.wxbeacon2viewer)

## できること

* 環境センサの現在の測定データの読み取り
* 環境センサ内の過去の測定データの読み出し
* アプリ内に取り込んだ測定データのグラフ表示(最大二週間まで)
* アプリ内に取り込んだ測定データのTSVエクスポート
* 環境センサの測定間隔の変更&内部タイマー設定

<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/wxbeacon2viewer/screenshot/sc01.png" width="25%"/>
<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/wxbeacon2viewer/screenshot/sc02.png" width="25%"/>
<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/wxbeacon2viewer/screenshot/sc03.png" width="25%"/>
<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/wxbeacon2viewer/screenshot/sc04.png" width="25%"/>




# BleScanner

Android用のBLEデバイスのスキャンツール

[https://github.com/cnaos/BleScanner](https://github.com/cnaos/BleScanner)


<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/BleScanner/device_list02.png" width="25%"/>
<img style="margin:0.5em;" src="https://github.com/cnaos/picture/raw/master/BleScanner/device_detail.png" width="25%"/>

googleの[Android BluetoothLeGatt Sample](https://github.com/android/connectivity-samples/tree/master/BluetoothLeGatt)
と、
HIRAMINEさんの[BLE通信ソフトを作る( Android Studio 2.3.3 + RN4020 )](https://www.hiramine.com/programming/blecommunicator/index.html)
をベースに、kotlin coroutineのcallbackFlowでBLEデバイスのスキャンを行うサンプルアプリです。

通常のBLEデバイスのスキャンではデバイス名が不明な場合が多いので、
スキャン後にBLEのGATTプロファイル(汎用アトリビュートプロファイル)を使って詳細なデバイス名の取得を行っています。


## 利用ライブラリ

* Able
  * [https://github.com/JuulLabs-OSS/able](https://github.com/JuulLabs-OSS/able)
  * AndroidのBluetoothLEフレームワークをKotlinのcoroutineで扱えるようにするためのフレームワーク
* Peko
  * [https://github.com/deva666/Peko](https://github.com/deva666/Peko)
  * Android PermissionsをKotlin Coroutineまたは、LiveDataで扱えるようにするためのライブラリ
* android-identicons
  * [https://github.com/lelloman/android-identicons](https://github.com/lelloman/android-identicons)
  * Ideticonを生成するためのライブラリ


## できること

* Bluetooth LEデバイスのスキャン
* Bluetooth LEデバイスのGATTサービスの一覧の表示
* Bluetooth LEデバイスのGATTキャラクタリスティック（Characteristic）の表示




# Torrent Dump

torrentファイルの解析と整合性チェックツール

[https://bitbucket.org/cnaos/torrentdump/src/master/](https://bitbucket.org/cnaos/torrentdump/src/master/)

<img src="https://bytebucket.org/cnaos/torrentdump/raw/a197e6b0c5f4739254a7814f07e751faf07b493c/images/screenshot1.png" width="50%"/>

## ツールの概要

windows用のtorrentファイルのダンプツールです。
ファイルの整合性チェックもできます。

## 特徴

javaで同様のGUIツールを作っていましたが、javaの実行環境のアップデートが面倒だったのでC#で作り直しました。
GUIで解析対象のファイルをドラッグアンドドロップできるようにしたかったので、WPFを選択しました。

GUIアプリを作る上で、ユーザ入力などのイベント処理を簡単に記述するため、ReactiveExtensionsを導入しました。

GUIに表示する情報のマッピングを簡単にするために、
読み込んだTorrentファイルのツリー構造データをXMLのツリー構造データに変換して、
XPathで指定した特定のノードの値を画面表示用のモデルにマッピングするという手法をとっています。


# QuickQRGen_RxSwift_MacOS


[https://bitbucket.org/cnaos/quickqrgen_rxswift_macos/src/master/](https://bitbucket.org/cnaos/quickqrgen_rxswift_macos/src/master/
)

RxSwift, RxCocoa, QRCoder をつかったMacOS用のQRコードジェネレータです。
RxSwiftでテキストフィールドに入力した文字列を即座にQRコードに反映します。

<img src="https://bytebucket.org/cnaos/quickqrgen_rxswift_macos/raw/6e8c359943e668967dde2962a67a32fcfce2d4fd/images/screenshot1.png" width="50%"/>
