## .NET Framework のソースコード

https://referencesource.microsoft.com/

## ASP.NETのセッション管理

https://qiita.com/84zume/items/dce5c9b496665183f1a9

> StateServer	「ASP.NET状態サービス」というWindowsサービスのプロセスで管理します。IISとは別のプロセスで管理するため、IISを再起動したとしても、セッション状態は維持されます。また特定のIISプロセスで管理されていないため、負荷分散の構成（クラスター構成）をとっているような複数台のサーバで共通したセッション管理を行うことができます。

> SQLServer	SQL Serverのデータベースでセッション状態を管理します。StateServerと同様のメリットがあります。

## Web.config

sessionState Element (ASP.NET Settings Schema)

https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-2.0/h6bb9cz9(v=vs.80)?redirectedfrom=MSDN


MultipleActiveResultSets
https://docs.microsoft.com/ja-jp/dotnet/api/system.data.sqlclient.sqlconnectionstringbuilder.multipleactiveresultsets?view=dotnet-plat-ext-5.0

Integrated Security

IntegratedSecurity プロパティの値。値が指定されていない場合は false。

https://docs.microsoft.com/ja-jp/dotnet/api/system.data.sqlclient.sqlconnectionstringbuilder.integratedsecurity?view=dotnet-plat-ext-5.0


Database と initial catalog の違いはない。(どらちかでよい)


IIS 上で親 Application の Web.config を子 Application の Web.config に継承させない方法

"親Application"のWeb.config に継承させたくないSectionを以下で囲む

```
<location path="." inheritInChildApplications="false">
</location>
```

http://emu717171.hatenablog.com/entry/2014/08/10/040204


Persist Security Info=False の使用
→ Persist Security Info=False とするべき

https://docs.microsoft.com/ja-jp/dotnet/framework/data/adonet/protecting-connection-information#use-persist-security-infofalse
