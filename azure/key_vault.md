Key Vaultを登録

1. Azure AD からアプリを登録する
https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps
2. 登録したアプリでキーを登録する (例：ホーム > 東横開発用 - アプリの登録 > StorageAPIv1 > 設定 > キー)
3. Key Vaultを登録する
https://portal.azure.com/#@toyokoazuregmail.onmicrosoft.com/resource/subscriptions/0babef06-13e8-45ef-800d-d14a9fa07a1c/resourceGroups/kazokunokiroku/providers/Microsoft.KeyVault/vaults/KazokuKeyVault/access_policies

4. アクセスポリシーにAzure ADで登録したアプリを新規追加する。
※subscription なんとかって書いてない方


https://gist.github.com/inosuke/6185003c2de804bc5075703ee1066ad8
