# Ubuntu setting

## VMの命名規則

Ubuntu[フランス人女性名][Version]
Versionは18.04なら1804とする。

フランス人女性名

https://www.kyoto-su.ac.jp/department/lf/gakushu/kyozai/prenom/prenom_table.html


# Need Apps

- clipit
- visual studio code
- gitkraken
- SoundConverter
- bitwarden
- smartgit
- mpv media player
- meld
- firefox
- chrome
- rhythmbox
- mongodb

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


## 自動起動

```
gnome-session
```

## ClipIt

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
