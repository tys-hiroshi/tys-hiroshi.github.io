http://online106.hatenablog.jp/entry/2020/02/13/205523

```
https://api.bitindex.network/api/v2/addrs/balance?address=アドレス

これいままで使ってきたけど無料ではなくなったみたい。
システムに組み込むなら支払うべきだが、こちらはまだテストの前のテストレベルほかのサービスを使う。

https://whatsonchain.com/address/アドレス

こんな感じ。whatsonchainはアドレスもtxもなんでもフリーワードで検索できる。

https://blockchair.com/bitcoin-sv/address/アドレス

これもあり。こちらはさらにいろいろなブロックチェーンの検索が出来る。こりゃすごい。

MatterCloudさんいままでありがとう
```

Bitcoin sv testnet address:

https://faucet.bitcoincloud.net/

https://test.whatsonchain.com/

address:

```
mnoTQaiqDBjUG6WWAUwhFycirbrKYUMgmU
```

https://test.whatsonchain.com/address/mnoTQaiqDBjUG6WWAUwhFycirbrKYUMgmU


generate privatekey from mnemonic

https://github.com/trezor/python-mnemonic/

exist bip32 module

https://github.com/AustEcon/bsvbip32/

```
var Mnemonic = require('bsv-mnemonic');
var code = new Mnemonic(bsv_mnemonic);

var xpriv1 = code.toHDPrivateKey("", network='testnet'); // no passphrase
//var xpriv2 = code.toHDPrivateKey('my passphrase'); // using a passphrase

console.log(xpriv1)
console.log(xpriv1.privateKey)
privatekey_wif = xpriv1.privateKey.toWIF()
```


bsv-mnemonic

```

var xpriv1 = code.toHDPrivateKey("", network='testnet');

|

Mnemonic.prototype.toHDPrivateKey = function(passphrase, network) {
  var seed = this.toSeed(passphrase);
  return bitcore.HDPrivateKey.fromSeed(seed, network);
};

bsv - hdprivatekey.js

HDPrivateKey.fromSeed = function (hexa, network) {

|

```
