## .NET Framework のソースコード

https://referencesource.microsoft.com/

## ASP.NETのセッション管理

https://qiita.com/84zume/items/dce5c9b496665183f1a9

> StateServer	「ASP.NET状態サービス」というWindowsサービスのプロセスで管理します。IISとは別のプロセスで管理するため、IISを再起動したとしても、セッション状態は維持されます。また特定のIISプロセスで管理されていないため、負荷分散の構成（クラスター構成）をとっているような複数台のサーバで共通したセッション管理を行うことができます。

> SQLServer	SQL Serverのデータベースでセッション状態を管理します。StateServerと同様のメリットがあります。


sessionState Element (ASP.NET Settings Schema)

https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-2.0/h6bb9cz9(v=vs.80)?redirectedfrom=MSDN

