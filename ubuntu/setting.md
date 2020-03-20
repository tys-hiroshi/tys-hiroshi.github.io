# Ubuntu setting



# app

## play mp4

```
sudo apt update
sudo apt-get install soundconverter
sudo apt install -y ubuntu-restricted-extras
sudo apt-get install ffmpeg
```

## git 

https://qiita.com/cyborg__ninja/items/6efd349370bf5f8bffb2

2段階認証

https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line

## add favorite custom app

https://askubuntu.com/questions/1026528/adding-custom-programs-to-favourites-of-ubuntu-dock

## 自動起動

gnome-session


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
