## install
install English version
日本語でインストールしないとmozcまわりがおかしなことになる（？
Language Setting
Language support - > Japanise [install]
Input method -> Fcitx
Fcitx configuration
Gloval config
Show Advance Option
Activate input method -> Ralt
Inactivate Input method -> Lalt
Keyboard- >Layouts->Options...
ctrl positions->Swap ctrl and caps lock
delete kayでempty

Window Tiling -> OFF

## mint de wacom 
wacom https://linuxwacom.github.io/
Kernel Driverのインストールと再起動で動作する
セキュアブートが入ってるとドライバーが入らないことに注意
sslのエラーメッセージがでるが問題なし？
はじめに、３つたりないというエラーが出るが最初の１つをインストールすればいい

wacom https://linuxwacom.github.io/
Kernel Driver をインストールして再起動で動く
sslのエラーがでても問題ない
3つ必要なinstallがでるがはじめの１つをいれればok
linux-karnelをupdateしたときは,make cleanをしてdriverをいれなおす
(再起動後一度cinammonがしぬ？

## 設定
mozcのskinは設定ではなく右下のキーボードアイコンからスキンを選択する

## dropbox
Linux で 1 万件以上のフォルダを監視する
https://www.dropbox.com/ja/help/syncing-uploads/files-not-syncing
	Linux 版の Dropbox デスクトップ アプリは、デフォルト設定により 1 万件以上のフォルダを監視することはできません。制限数を超えた場合は監視
echo fs.inotify.max_user_watches=100000 | sudo tee -a /etc/sysctl.conf; sudo sysctl -p

## bash
.inputrc .bashrcではないことに注意
大文字小文字を区別せず補完する
set completion-ignore-case on

## keyboard
### SandS
apt install xcape
xmodmap -e 'keycode 255=space'; xmodmap -e 'keycode 65=Shift_L';xcape -e '#65=space'
