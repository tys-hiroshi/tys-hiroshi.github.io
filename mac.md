## App

- Chrome

- Bitwarden
- Xcode
- Android Studio
- Google Japanese input

「キー設定の選択」をmacOSとWindows OSで同じにします。

Windowsに慣れているなら「MS-IME」、Macに慣れているなら「ことえり」に統一する

- Karabiner-Elements

https://creative89.com/2017/05/27/how-to-use-windows-keyboard-on-mac/

PCキーボードの無変換キー to 英数キー
PCキーボードの変換キー to かなキー
left_control to left_command
capslock to left_control


- CopyClip
- simplenote
- memory diag
- skitch
- github desktop
- FileTransfer https://www.android.com/filetransfer/

https://qiita.com/suzutatsu/items/817f58cfb6e69f56d134

- postman


- homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
```

https://gitup.co/


## Setting

Scroll
open Lanchpad with shortcut (Ctrl+L)
Keyboard


https://qiita.com/ohkawa/items/c84fcb1347dfb3a73c6d

記号 | 読み方
-- | --
⌘ | command
⌥ | option / alt
⇧ | shift
⌃ | control


https://brew.sh/index_ja

```
zsh: command not found: brew

vi ~/.zshrc


export PATH="/usr/local/bin:/usr/local/sbin:$PATH"

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
➜  ~ brew --version
Homebrew 2.3.0
Homebrew/homebrew-core (git revision 69d13; last commit 2020-06-09)
```

### heroku install

```
brew tap heroku/brew && brew install heroku
```


https://docs.brew.sh


brew install wget

fink でmac にaptをInstallする方法

https://qiita.com/taka_baya/items/c84e306f05e2513e4a67
https://qiita.com/u4da3/items/4229702b4a8504290dd5


Terminalで実行中のコマンドを中止

apple key + dot(.)

## Windows からリモートする

http://tenten0213.hatenablog.com/entry/2016/11/29/211656

システム環境設定 - 共有 で 画面共有 にチェック

「コンピュータの設定」ボタンからポップアップで出てきた選択肢の両方にチェックを入れ、パスワードを入力


## macbook を閉じてもスリープさせない

OS X Server：スリープを防ぐ方法
OS X Server を使っている Mac 上でスリープモードになるのを防ぐ方法について説明します。

(管理者パスワードで) 次のターミナルコマンドを使うと、コンピュータがスリープになるのを防ぐことができます。

```
sudo pmset -a disablesleep 1
```

値を 1 に設定すると、すべてのスリープ機能は無効化されます。また、Apple メニューの「スリープ」項目が、淡色表示 (「グレイ表示」) されます。



「コンピュータの設定」ボタンからポップアップで出てきた選択肢の両方にチェックを入れ、パスワードを入力



## finder でファイルのPath をコピーする

https://aprico-media.com/posts/1578

ファイルを右クリックする。
その状態で「Optionキー」を押しましょう。すると、「○○をコピー」というメニューが「○○のパス名をコピー」に変わります。

この機能を選択することで、ファイル・フォルダまでのパスのコピーが出来ます。


https://support.apple.com/ja-jp/guide/terminal/apdc52250ee-4659-4751-9a3a-8b7988150530/mac

圧縮

tar -czvf

解凍

tar -xvf

## Macを使ってiPhoneのバックアップを作成する

https://support.apple.com/ja-jp/guide/iphone/iph3ecf67d29/ios


