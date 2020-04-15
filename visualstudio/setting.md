## ログで出力されるコードの行が正しくないとき

プロジェクトのプロパティを開く。
ビルドの構成を選択。
コードの最適化のチェックを外す。


## Visual Studio で.NET Framework のVersionを変更するとき

1. プロジェクトのプロパティを開く
2. アプリケーション のターゲット フレームワークのVersionを変更する
3. Web.configのhttpruntime targetframeworkを2のVersionに変更する
4. packages.config があるなら、パッケージマネージャー コンソールでUpdate-Package -Reinstall とする。

https://docs.microsoft.com/ja-jp/dotnet/framework/migration-guide/runtime/4.6.1-4.7.2



## vscode

https://qiita.com/dynamonda/items/5a8129cd6e9cc139d94a

> pip3で追加したモジュールはpylint でimport errorが表示される

VscodeのSettings.jsonを修正する。

File -> Preference -> Settings

Userのタブで settings.json と検索して、J内に以下を入力する。

```
{
    "python.pythonPath": "{$ which python3 のパス}"
}
```


### テストがDebugできないとき

出力 ＞ 出力元：テストを指定したときのログが以下の様になっているとき。

```
ログのレベルは、情報 (既定) に設定されています。
テスト データ ストアが 0.029 秒で開きました。
---------- 要求されたテストの実行についてテスト検出を開始しています ----------
Microsoft.VisualStudio.TestPlatform.ObjectModel.TestPlatformException: Testhost process exited with error: It was not possible to find any compatible framework version
The framework 'Microsoft.NETCore.App', version '2.2.0' was not found.
  - The following frameworks were found:
      3.1.3 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
You can resolve the problem by installing the specified framework and/or SDK.
The specified framework can be found at:
  - https://aka.ms/dotnet-core-applaunch?framework=Microsoft.NETCore.App&framework_version=2.2.0&arch=x86&rid=win10-x86
. Please check the diagnostic logs for more information.
   at Microsoft.VisualStudio.TestPlatform.CrossPlatEngine.Client.ProxyOperationManager.ThrowExceptionOnConnectionFailure(Int32 connTimeout)
   at Microsoft.VisualStudio.TestPlatform.CrossPlatEngine.Client.ProxyOperationManager.SetupChannel(IEnumerable`1 sources, String runSettings)
   at Microsoft.VisualStudio.TestPlatform.CrossPlatEngine.Client.ProxyDiscoveryManager.DiscoverTests(DiscoveryCriteria discoveryCriteria, ITestDiscoveryEventsHandler2 eventHandler)
========== テスト検出が中止されました: 535 ミリ秒 に 0 件のテストが見つかりました ==========
```

テストProjectの プロパティから ビルド ＞ 対象プラットフォームをx64にする。

https://stackoverflow.com/questions/59246822/after-updated-visual-studio-2019-to-16-4-0-i-cant-run-tests-with-target-framewo

