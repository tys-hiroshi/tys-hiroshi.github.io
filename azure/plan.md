S3からS1にしたときに「App Service プラン ProdRecommendPlan は、プランのサイズに対して推奨されているアプリ数を超えています。 詳細情報」と表示されていた。

「詳細情報」のURLは以下。

https://azure.github.io/AppService/2019/05/21/App-Service-Plan-Density-Check.html



https://medium.com/@zaab_it/azure-app-service-plan-tiers-f07d5e22297a から引用

App ServiceプランがSmall / Medium層

App Service Plan size translation:
1 = Small = 1 Core + 1.75 GB RAM
2 = Medium = 2 Core + 3.5 GB RAM
3 = Large = 4 Core + 7GB RAM

S1: Standard + Small ()
S1
ACU 合計 100
1.75 GB メモリ
A シリーズ コンピューティングと同等
9650.60 JPY/月 (推定)

S2
ACU 合計 200
3.5 GB メモリ
A シリーズ コンピューティングと同等
19308.50 JPY/月 (推定)

S3
ACU 合計 400
7 GB メモリ
A シリーズ コンピューティングと同等
38602.40 JPY/月 (推定)


https://azure.microsoft.com/ja-jp/pricing/details/app-service/windows/

Standard サービス プラン
Standard サービス プランは、実稼働ワークロードの実行を対象として設計されています。価格は、実行するインスタンスのサイズと数によって決まります。組み込みのネットワーク負荷分散サポートが、トラフィックを自動的に各インスタンスに分散させます。Standard プランには、トラフィックのニーズに合わせて実行中の仮想マシンのインスタンス数を自動的に調整する、自動スケール機能が含まれています。Linux ランタイム環境で使用される Standard サービス プランは、Web App for Containers をサポートします。

インスタンス	コア数	RAM	STORAGE	料金
S1	1	1.75 GB	50 GB	¥13.216/時間
S2	2	3.50 GB	50 GB	¥26.432/時間
S3	4	7 GB	50 GB	¥52.864/時間


