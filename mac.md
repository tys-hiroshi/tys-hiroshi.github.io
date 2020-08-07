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

## command code が使えないとき

Visual Studio Codeを起動
コマンドパレットを開く(cmd+shift+p)
"Shell Command: Install 'code' command in PATH"を選択

https://qiita.com/sayama0402/items/453595d0d8f54b645753

```
emacs ~/.zshrc
```

```
function code {
    if [[ $# = 0 ]]
    then
        open -a "Visual Studio Code"
    else
        local argPath="$1"
        [[ $1 = /* ]] && argPath="$1" || argPath="$PWD/${1#./}"
        open -a "Visual Studio Code" "$argPath"
    fi
}
```

```
source ~/.zshrc
```


dotfileを見えるようにする

```
defaults write com.apple.finder AppleShowAllFiles -boolean true
killall Finder
```

元に戻す

```
defaults delete com.apple.finder AppleShowAllFiles
killall Finder
```

finder to terminal

システム環境設定 > キーボード > ショートカット > サービス > フォルダに新規ターミナルタブ

https://qiita.com/yamagh/items/02608e97be22c85cefaa

## TextEdit

Defaultで貼り付けると装飾されてうざいので、Plain Text で貼り付ける

https://www.lifehacker.jp/2016/08/160813_textedit_plaintxt.html

```
defaults write com.apple.TextEdit RichText -int 0
```

## LifeTime


https://support.apple.com/ja-jp/HT201624


> iPhone、iPad、iPod、Mac 製品をお持ちのお客様は、製品の販売中止後 5 年間 (法で定められている場合はそれ以上) は Apple や Apple サービスプロバイダから修理サービスや部品を入手できます。Apple は、特定の技術的なオブソリート製品のサポートをすでに終了しています。
> ビンテージ製品とは、販売中止から 5 年以上 7 年未満の製品です。Mac、iPhone、iPad、iPod、Apple TV のビンテージ製品については、Apple Store 直営店を含む Apple のサービスプロバイダからハードウェアの修理サービスを引き続き受けることができますが、在庫状況や、法律の定めるところによります。


https://appleshinja.com/mac-lifetime
