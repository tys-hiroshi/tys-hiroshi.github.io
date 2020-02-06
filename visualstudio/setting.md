## ログで出力されるコードの行が正しくないとき

プロジェクトのプロパティを開く。
ビルドの構成を選択。
コードの最適化のチェックを外す。


## Visual Studio で.NET Framework のVersionを変更するとき

1. プロジェクトのプロパティを開く
2. アプリーケーション のターゲット フレームワークのVersionを変更する
3. Web.configのhttpruntime targetframeworkを2のVersionに変更する
4. packages.config があるなら、Update-Package -Reinstall とする。
