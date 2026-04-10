# 概要
Galaxy note10+(楽天モバイル)でCAを開放する方法と、戻す方法を記載する。

## 事前準備(Windows)
Windowsで、以下をinstallする

・Android USB Driver for Windowsのインストール<br>
https://developer.samsung.com/mobile/android-usb-driver.html


・DFS QToolsのインストール<br>
https://cdmatool.net/Downloads/Products

・URLが切れていたら<br>
https://drive.google.com/drive/folders/1cqpqKyNEF4Qk0REtVC2WMQC_t2yOeYOW?usp=drive_link

## 手順

１．Android(note10+)の電話アプリで　\*#0011#　を入力して、ca_disableであることを確認<br>
２．開発者モードでUSBデバッグにチェック<br>
　　→必要に応じて：Diagモード（\*#0808# > RNDIS + DM + MODEM )にする。<br>
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





## 手順2

回線を増やす方法

１．Android(note10+)の電話アプリで　\*#0011#　を入力して、ca_disableであることを確認<br>
２．開発者モードでUSBデバッグにチェック<br>
　　→必要に応じて：Diagモード（\*#0808# > RNDIS + DM + MODEM )にする。<br>
３．DFS QToolsを起動する、portタブで、androidに接続<br>
４．[Tools]→[Programing]→[BCC LTE]を開く<br>
５．３番で開いたportを設定<br>
６．[Read]で、androidの情報を取得<br>
７．8番と18番をtrue<br>
※note20+では26 18 8 11をtrueにした。<br>


## 手順3

docomoをアンインストール<br>



1.ツールをダウンロード<br>
　https://developer.android.com/studio/releases/platform-tools<br>
　リンク切れならこちら：https://drive.google.com/file/d/1Qjgae7S5nH03jHc0TLVQyvOwGMNvlmBk/view?usp=drive_link<br>
<br>
２．コマンドラインでアンインストールした場所へ移動<br>
<br>
３．adb.exe shellで接続<br>
　　→必要に応じて：Diagモード（\*#0808# > MTP )にする。<br>
４．docomoのパッケージを調べる<br>
　　→pm list packages | grep docomo<br>
５．削除<br>
　　→pm uninstall --user 0 <パッケージ名><br>
６．削除できないアプリ<br>
　　→android上でデバイス管理アプリとして設定されているので、解除してから消す必要がある。<br>
　　com.nttdocomo.android.wipe<br>
　　com.nttdocomo.android.remotelock<br>
７．Galaxyのカレンダー<br>
　　pm uninstall --user 0 com.samsung.android.calendar<br>
８．ドコモのユーザー管理<br>
　　pm uninstall --user 0 com.android.contacts<br>

参考URL<br>
https://note.com/nekofuton/n/nae2421530dc1

Galaxy [Galaxy s22 ultra.txt](https://github.com/user-attachments/files/26637649/Galaxy.s22.ultra.txt)


Galaxy s22 ultraを削除する際のコマンド例
pm uninstall --user 0 com.nttdocomo.android.wipe
pm uninstall --user 0 com.nttdocomo.android.devicehelp
pm uninstall --user 0 com.nttdocomo.android.anshinsecurity
pm uninstall --user 0 com.nttdocomo.android.apnsw
pm uninstall --user 0 jp.co.nttdocomo.carriermail
pm uninstall --user 0 com.nttdocomo.android.remotelock
pm uninstall --user 0 com.nttdocomo.android.msg
pm uninstall --user 0 jp.co.nttdocomo.anshinmode
pm uninstall --user 0 com.nttdocomo.android.schedulememo
pm uninstall --user 0 com.nttdocomo.android.mascot
pm uninstall --user 0 com.nttdocomo.android.homezozo
pm uninstall --user 0 jp.co.nttdocomo.lcsapp
pm uninstall --user 0 com.nttdocomo.android.mymagazine
pm uninstall --user 0 com.nttdocomo.android.databackup
pm uninstall --user 0 com.nttdocomo.android.idmanager
pm uninstall --user 0 com.nttdocomo.android.dmenu2
pm uninstall --user 0 com.nttdocomo.android.anmane2
pm uninstall --user 0 jp.co.nttdocomo.saigaiban
pm uninstall --user 0 com.nttdocomo.android.felicaremotelock
pm uninstall --user 0 com.nttdocomo.android.docomoset
pm uninstall --user 0 com.nttdocomo.android.pf.dcmippushaggregator
pm uninstall --user 0 com.nttdocomo.android.initialization
pm uninstall --user 0 com.nttdocomo.android.applicationmanager
pm uninstall --user 0 com.nttdocomo.android.store
pm uninstall --user 0 com.nttdocomo.android.applicationmanagersub

pm uninstall --user 0 com.android.contacts
pm uninstall --user 0 com.samsung.android.app.spage
pm uninstall --user 0 com.microsoft.skydrive
pm uninstall --user 0 com.google.android.apps.tachyon
pm uninstall --user 0 com.samsung.android.calendar
