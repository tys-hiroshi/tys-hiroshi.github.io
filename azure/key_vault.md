Key Vaultを登録

アクセスポリシーにアプリ(StorageAPIv1)を新規追加する。

Azure AD からアプリを登録する
https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps

設定＞キー からキーを登録する
https://portal.azure.com/#blade/Microsoft_AAD_IAM/ApplicationBlade/appId/6f99efeb-4b1f-4709-b9bf-c7ac0115e8d2/objectId/f73fee63-a767-4d6c-b5ef-c28c656a4e7c


キーが使えなくなったら、Key Vaultのアクセスポリシーからアプリを削除してもう一度追加する。
※本当にできるかわからない

ADからアプリを消してキーを追加、KeyVaultのアクセスポリシーからアプリを削除、もう一度追加(Subscriptionの)
