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


### ListView は古いからRecyclerView を

https://qiita.com/fu_neko/items/722e0ab5f0f1255f87bf

### データの保存, 共有

https://qiita.com/s_emoto/items/aeacf06111b9469176b1

Room を使用してローカル データベースにデータを保存する

https://developer.android.com/training/data-storage/room?hl=ja

https://github.com/arifnadeem7/mvvmcoroutinesandflow

package を作るとき、java > com.hblockth.dapp で 右クリック して、New > package

### 例えば水没するなどしてAndroidが操作できないときに USBにつないでストレージのデータを取得できるか？

### Shortcut Key

https://qiita.com/takke/items/5cbc629f7f65d6a49906
定義箇所へ移動（Go to declaration）	Ctrl + B	
戻る	Ctrl + Alt + ←	
進む	Ctrl + Alt + →

Cannot access database on the main thread since it may potentially lock the UI for a long period of time.

https://qiita.com/toastkidjp/items/49ad3035a6df525ce040
