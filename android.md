No target device found.

https://qiita.com/AoiLaurent/items/319f7dc0996bdc03c849


Emulator: emulator: ERROR: OpenGLES emulation failed to initialize. Please consider the following troubleshooting steps:

https://kg-update.net/running_avd3/

Driverを更新する。



```
cd apps/android-studio-ide-192.6392135-linux/android-studio/bin/
./studio.sh
```

```
sudo apt install qemu-kvm
sudo adduser $USER kvm
```

したあとは再起動してください。

Layout Editor の表示

app > res > layout > activity_main.xml 

https://qiita.com/k-ysd/items/f428072e9b5db9285cf3


## Button の位置が変わらない

https://qiita.com/sasayabaku/items/3697f3cd34a66df6678c

```
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintRight_toRightOf="parent"
app:layout_constraintLeft_toLeftOf="parent"
```


### fuel を使う

https://github.com/kittinunf/fuel

https://qiita.com/naotsune/items/8a45fb5436b50d3fef56


https://qiita.com/naoi/items/8df1409ad48ad8f3c632  ← なんか古い？
