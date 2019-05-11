# Mint Linux
## install
install 日本語 でmozcがデフォルトでインストールされる
HOME以下のフォルダー名が日本語になっているので
一度 設定->言語 English(US)に設定して再起動
再起動時にフォルダ名を英語にしますか(Update)　とダイアログがでるので Update
同様にlanguage->Japanese に戻して再起動　フォルダ名を英語にしたいので今回は No を選択する

	install English version
	日本語でインストールしないとmozcまわりがおかしなことになる（？
	Language Setting
	Language support - > Japanise [install]
	

windowが端にきたときリサイズされるのを止める
Window Tiling -> OFF

## keyboard
Input method -> Fcitx
Fcitx configuration

### 英語キーボードを使って右アルトで日本語　左アルトで英語に切り替わるようにする
Gloval config
Show Advance Option
Activate input method -> Ralt
Inactivate Input method -> Lalt


##  swap  ctrl  and  caps  
Keyboard- >Layouts->Options...
ctrl positions->Swap ctrl and caps lock
delete kayでempty
fasd sadfjlkj lkj lkj ;lkj l;k ;lk ｌｋｊｌｋｊ

### SandS  spaceh key を shiftとしても扱う
apt install xcape
xmodmap -e 'keycode 255=space'; xmodmap -e 'keycode 65=Shift_L';xcape -e '#65=space'
```
alias sands="killall xcape; xmodmap -e 'keycode 255=space'; xmodmap -e 'keycode 65=Shift_L';xcape -e '#65=space'"
```
スペースを押したときに入力モードの切り替えが働いてしまう
入力モードメソッドの設定->全体の設定->ホットキー-> 入力メソッドの切り替え
Ctrl+ShiftからAlt+Shiftにする

英語モードのときspaceが二重(それ以上)に入力されてしまう
xmodmapの多重起動の可能性がある?
再起動

### mozc
mozcのskinは設定ではなく右下のキーボードアイコンからスキンを選択する

## neovim
https://github.com/neovim/neovim/wiki/Installing-Neovim#ubuntu

## golang
https://golang.org/dl/
source .profile


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


## dropbox
Linux で 1 万件以上のフォルダを監視する
https://www.dropbox.com/ja/help/syncing-uploads/files-not-syncing
	Linux 版の Dropbox デスクトップ アプリは、デフォルト設定により 1 万件以上のフォルダを監視することはできません。制限数を超えた場合は監視
echo fs.inotify.max_user_watches=100000 | sudo tee -a /etc/sysctl.conf; sudo sysctl -p

## bash
.inputrc .bashrcではないことに注意
大文字小文字を区別せず補完する
set completion-ignore-case on
```
echo set completion-ignore-case on > .inputrc
```

# emoji
フォントはインストールで対応済み
辞書登録
https://github.com/peaceiris/emoji-ime-dictionary



# Arch Linux
sudo pacman -S python-pip
sudo pip install pynvim
sudo pacman -S python2-pip
sudo pip2 install pynvim


sudo pip install pynvim
