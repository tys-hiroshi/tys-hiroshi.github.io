## アプリケーションの設定

### DataTime.Now がUTCになっているとき

ホーム > 【App Service】 - 構成

のアプリケーション設定 でWEBSITE_TIME_ZONE : Tokyo Standard Time とすることでDataTime.NowがJSTになる。

### Azure 上のApp Serviceでappsettings.json を切り替えたいとき

ASPNETCORE_ENVIRONMENT でDevelopment,Staging,Production にすることでappsettings.{ASPNETCORE_ENVIRONMENT}.json が切り替えられる
