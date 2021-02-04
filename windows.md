https://forest.watch.impress.co.jp/docs/serial/yajiuma/1071179.html


### 仮想デスクトップを切り替え

［Windows］＋［Ctrl］＋左右キー

［Windows］＋［Ctrl］＋［D］キー：仮想デスクトップを作成する

［Windows］＋［Ctrl］＋［F4］キー：現在の仮想デスクトップを閉じる

### 邪魔なウィンドウを隠す［Windows］＋［Home］キー

［Windows］＋［D］キー：ウィンドウをすべて非表示にしてデスクトップを表示する（もう一度押せば元の状態へ戻せる）

Windows + Shift + S

### 動画を撮る

Windows +G


### Command

#### proxy を使用しない

```
Microsoft Windows [Version 10.0.18363.720]
(c) 2019 Microsoft Corporation. All rights reserved.

C:\WINDOWS\system32>netsh winhttp show proxy

Current WinHTTP proxy settings:

    Direct access (no proxy server).


C:\WINDOWS\system32>netsh winhttp reset proxy

Current WinHTTP proxy settings:

    Direct access (no proxy server).
```

### WinMergeでDiff ペインが表示されないとき

ファイル比較ウインドウが表示されている状態で、
[表示]メニュー → [ロケーションペイン]にチェックを入れてみるとどうでしょうか？

これでうまくいかない場合は、WinMerge終了後、
レジストリエディタregeditで

HKEY_CURRENT_USER\SOFTWARE\Thingamahoochie\WinMerge

のWinMergeをリネームすると初期状態になりますので
ロケーションペインが表示されるようになると思います。


https://answers.microsoft.com/en-us/windows/forum/windows_10-start-win_taskbar/how-to-increase-the-number-of-recent-files/2ec5e80a-c8f1-4e25-bd5e-4c98169a520e

## how to increase the number of application history

```
Click your Start Button, type regedit and hit Enter to open the Registry Editor

Navigate to:
HKEY_CURRENT_USER\Software\Microsoft\ Windows\CurrentVersion\Explorer\Advanced

On the right-side, look for an entry named JumpListItems_Maximum.

If there is no such entry, you need to create one by right-clicking on the empty area, clicking New, clicking DWORD (32-bit) Value, and name it as JumpListItems_Maximum

Double click that DWORD and set its value to 20 or 30
```


### context menu

https://laboradian.com/add-item-to-context-menu/

私はここで答えを見つけました:
https://forum.videolan.org/viewtopic.php?t=82274

関連する指示:

> 私はここで答えを見つけました:
> https://forum.videolan.org/viewtopic.php?t=82274
> 
> 関連する指示:
> 
> 
> Regeditを開きます。 HKEY_CLASSES_ROOT \ Directory \ shellを見つけます。
> このキーの下で、フォルダーのコンテキストメニューから削除する各VLCキーを見つけます。
> (オプション)それぞれを右クリックして、エクスポートを選択します(念のため)。キーの名前に「-dir」を加えて、エクスポートされたregファイルを保存します。完全なレジストリパスではなくキー名のみを取得するには、名前が強調表示されているときに名前を変更する代わりに、最初に名前変更を選択してから、(エクスポートする前に)コピーを選択します。 [キー名のコピー]は、選択したキーだけではなく、フルパスを提供します。
> キーを削除します。

https://ja.ojit.com/so/contextmenu/322838
