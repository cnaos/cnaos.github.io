# cnaos's github pages

これまでにつくったもの

# BleScanner

Android用のBLEデバイスのスキャンツール

[https://github.com/cnaos/BleScanner](https://github.com/cnaos/BleScanner)


<img src="https://github.com/cnaos/picture/raw/master/BleScanner/device_list02.png" width="25%"/><img src="https://github.com/cnaos/picture/raw/master/BleScanner/device_detail.png" width="25%"/>

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
