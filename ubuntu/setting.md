# Ubuntu setting

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
