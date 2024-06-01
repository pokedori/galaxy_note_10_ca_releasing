# 概要
Galaxy note10+(楽天モバイル)でCAを開放する方法と、戻す方法を記載する。

## 事前準備(Windows)
Windowsで、以下をinstallする

・Android USB Driver for Windowsのインストール<br>
https://developer.samsung.com/mobile/android-usb-driver.html


・DFS QToolsのインストール<br>
https://cdmatool.net/Downloads/Products


## 手順

１．Android(note10+)の電話アプリで　*#0011#　を入力して、ca_disableであることを確認<br>
２．開発者モードでUSBデバッグにチェック<br>
　　→必要に応じて：Diagモード（*#0808# > RNDIS + DM + MODEM )にする。
３．DFS QToolsを起動する、portタブで、androidに接続<br>
４．[Tools]→[File Explorer]を開く<br>
５．３番で開いたportを設定<br>
６．[Read]で、androidの情報を取得<br>
７．ca_disableを削除<br>
　　/nv/item_files/modem/lte/common/ca_disable

## ca_disableを戻す

以下にバックアップを残すので、それをエクスポートすること<br>
https://github.com/pokedori/galaxy_note_10_ca_releasing/blob/main/20240418_112619_Qualcomm%20Universal%5B8089C141%5D.zip

## 周波数を広げる前のバックアップ
https://github.com/pokedori/galaxy_note_10_ca_releasing/blob/main/Galaxy%20note20%20ultra%20band%E5%A4%89%E6%9B%B4%E5%89%8D%E3%81%AE%E3%83%90%E3%83%83%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97.zip

## 参考

https://oiio.jp/entries/5394<br>
https://pocyomkin1220.com/galaxy-carrier-aggregation/<br>
https://hchch.net/galaxy-lte-band-enable/
