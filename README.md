# galaxy_note_10_ca_releasing
Galaxy note10+(楽天モバイル)でCAを開放

# 概要
Galaxy note10+(楽天モバイル)でCAを開放する方法と、戻す方法を記載する。

# 事前準備(Windows)
Windowsで、以下をinstallする

Android USB Driver for Windowsのインストール
https://developer.samsung.com/mobile/android-usb-driver.html

DFS QToolsのインストール
https://cdmatool.net/Downloads/Products


# 手順

１．Android(note10+)の電話アプリで　*#0011#　を入力して、ca_disableであることを確認
２．開発者モードでUSBデバッグにチェック
３．Diagモード（*#0808# > RNDIS + DM + MODEM )にする。
４．DFS QToolsを起動する、portタブで、androidに接続
５．[Tools]→[File Explorer]を開く
６．[Read]で、androidの情報を取得する
７．ca_disableを削除
　　/nv/item_files/modem/lte/common/ca_disable

# ca_disableを戻す
以下にバックアップを残すので、それをエクスポートすること



# 参考
https://oiio.jp/entries/5394
https://pocyomkin1220.com/galaxy-carrier-aggregation/
