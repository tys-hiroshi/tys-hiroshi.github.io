# Ubuntu setting

## VMの命名規則

Ubuntu[フランス人女性名][Version]
Versionは18.04なら1804とする。

フランス人女性名

https://www.kyoto-su.ac.jp/department/lf/gakushu/kyozai/prenom/prenom_table.html


# Need Apps

- clipit -> Gpaste
- visual studio code
- SoundConverter
- bitwarden
- smartgit
- mpv media player
- meld
- firefox
- chrome
- rhythmbox
- mongodb

~~gitkraken~~

## Path

.bashrc

```
export PATH="$PATH:[directory path]"
```


## Default to python3

path is which command path

```
alias python='/usr/bin/python3'
```

## aliasは専用の設定ファイルが用意されている

create .bash_aliases

```
alias cat='cat -n'
alias emacs='emacs -nw'
alias python='/usr/bin/python3'
alias pip='/usr/bin/pip3'
```

```
source ~/.bashrc
```


http://chie8842.hatenablog.com/entry/2017/03/23/152615



# app

## play mp4

```
sudo apt update
sudo apt-get install soundconverter
sudo apt install -y ubuntu-restricted-extras
sudo apt-get install ffmpeg
```

## convert mp4 to mp3

https://qiita.com/fujisystem/items/0b3abb5cb1a5671c4d4c

```
sudo apt -y install ffmpeg ffmpeg-devel
find . -type f -name "*.mp4" -print0 | perl -pe 's/\.mp4\0/\0/g' | xargs -0 -I% ffmpeg -i %.mp4 -acodec libmp3lame -ab 256k %.mp3
ffmpeg -i hoge.mp4 -acodec libmp3lame -ab 256k foo.mp3
```



## git 

https://qiita.com/cyborg__ninja/items/6efd349370bf5f8bffb2

2段階認証

https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line

## add favorite custom app

https://askubuntu.com/questions/1026528/adding-custom-programs-to-favourites-of-ubuntu-dock

~/.local/share/applications に登録したいAppについて以下のファイルで保存する。

[appname].desktop

```
[Desktop Entry]
Type=Application
Encoding=UTF-8
Name=SmartGit
Comment=SmartGit
Exec=[app path]
Icon=[app icon path]
Terminal=false
```

```
chmod 773 [appname].desktop
cp [appname].desktop ~/Desktop
```

デスクトップにコピーされたファイルを実行して、Add Favoriteにする。


http://91stardust-atelier.hatenablog.com/entry/2016/11/17/015854

Ubuntu 2004 でデスクトップからdesktopファイルが起動しない

https://www.it-swarm-ja.tech/ja/.desktop/ubuntu-2004-lts%E3%81%A7%E3%83%87%E3%82%B9%E3%82%AF%E3%83%88%E3%83%83%E3%83%97%E3%81%8B%E3%82%89desktop%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%8C%E8%B5%B7%E5%8B%95%E3%81%97%E3%81%AA%E3%81%84/997984570/


## 自動起動

```
gnome-session
```

## Gpaste

ソフトウェアUpdate から検索してInstallし、

sudo apt install gnome-shell-extensions-gpaste

した後にRestart OS。

## ClipIt(expired)

sudo apt install clipit

https://github.com/CristianHenzel/ClipIt

```
Action	Key combination
History	Ctrl + Alt + h
Actions	Ctrl + Alt + a
Menu	Ctrl + Alt + p
Search	Ctrl + Alt + f
Offline mode	Ctrl + Alt + o
```

## static item

ref. https://askubuntu.com/questions/876078/how-to-create-static-items-in-clipit

> Right click the Clipit icon in the toolbar and select Manage History. A pop-up will appear titled Manage History.
> 
> Then choose the copied item from the list in the pop-up that you want to make static and click the Edit button at the bottom. Another pop-up will appear titled Editing Clipboard.
> 
> At the bottom left there will be a check box to make the item static, then click the OK button and that's it.



## Browser

- chrome
- firefox
- brave

https://brave-browser.readthedocs.io/en/latest/installing-brave.html#linux


## mount windows share folder


1.windows features

2.windows network sharing setting

3.windows folder share

4.ubuntu below commend

```
sudo mkdir -p /mnt/windows
sudo mount.cifs //[PC name or IP]/[Folder name] /mnt/windows -o username=[windows username],password=[windows password for username (it's not pin)]
```

### dpkg install

```
sudo dpkg -i [deb file]
sudo apt -f install
```
### dpkg uninstall

```
sudo dpkg -r [app name]
```

```
sudo update-grub
sudo reboot
```

https://yamanxworld.blogspot.com/2015/02/windows-server-2012-r2-hyper-v-and.html


## snap


snap は canonical が開発している新しいパッケージシステムです。独自のファイルシステムを利用して、バイナリの動作に必要なライブラリを全てパッケージングして配布することができます。snap を利用することで、 yum や apt のような Linux ディストリビューションのパッケージシステムを利用した時に、任意のバージョンをユーザーが自由に使うことができない問題を解決しました。

```
sudo snap install ruby --classic
```

## Virtualbox

hyper-vを有効にするとVirtual Box 上のUbuntuの挙動がおかしくなった(容量が少なかったからかわからないが、Gpartedで拡張した)
HyperVを無効にしても状況が改善されないので、一度再起動して、Virtual Boxをアンインストール。
その後、再起動しVirtual Boxを（Defaultの設定のまま）インストールした。
その後、仮想環境を使ったが、今の所特に問題はなさそう。

### Virtual box のウィンドウリサイズ

Virtual box のウィンドウリサイズに応じて自動的に仮想マシンをリサイズする - Qiita
https://qiita.com/lion0506/items/36b9ce19724a32fbd1ac

### Storageのサイズを変更する方法

```
"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" modifyhd [vdiのパス] --resize [MB]
```

```
sudo apt-get update
sudo apt-get install gparted
sudo gparted
```

### Windows FolderをMountする

1. Windows上の任意の場所に共有フォルダを作成。(共有設定でRead/Writeを有効にする)

2. VirtualBoxマネージャー→設定→共有フォルダ→共有フォルダを追加
3. フォルダのパス→その他→作成した共有フォルダを指定、自動マウントにチェック。
4. /mnt/windows にマウントされている

※ Guest Additions CD が多分事前にインストールする必要がある

## app

https://sicklylife.jp/ubuntu/2004/settings.html


http://releases.ubuntu.com/20.04/?_ga=2.139916275.1176122378.1586859505-491720526.1585113064


【Ubuntu】キーリングの解除のダイアログを出したくない

https://www.softel.co.jp/blogs/tech/archives/4635


### Keyboard layout

https://golang.hateblo.jp/entry/ubuntu-keyboard-layout

```
$ sudo dpkg-reconfigure keyboard-configuration
```

