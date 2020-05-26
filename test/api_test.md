## テスト観点

### Http Status Code

- 正常なリクエストの場合、HTTP Status Code: 200 を返す
- リクエストパラメータが間違っている場合、HTTP Status Code: 400 を返す
- 認証エラーの場合、HTTP Status Code: 401 を返す
- 許可されていないMethodでリクエストした場合、HTTP Status Code: 405 を返す
- 例外が発生した場合、HTTP Status Code: 500 を返す


### リクエストパラメータ

パラメータが存在しない場合、どのような挙動をするか

#### 数値

- 下限と上限が存在する

#### 文字

- 最大文字数


### 応答時間


#### OWASP ASVS

https://www.jpcert.or.jp/securecoding/OWASP_ASVS_20160623.pdf
