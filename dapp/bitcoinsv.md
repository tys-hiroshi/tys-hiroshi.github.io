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

## bip39, bip32 について

https://gist.github.com/t4sk/ac6f2d607c96156ca15f577290716fcc

https://qiita.com/masakielastic/items/21ba9f68ef6c4fd7692d

https://en.bitcoin.it/wiki/List_of_address_prefixes

https://bitcoin.stackexchange.com/questions/55383/how-to-convert-a-wif-private-key-to-a-bip32-extended-private-key

https://github.com/AustEcon/bsvbip32

https://github.com/bitcoin/bips/blob/8677fd57864430becd4e828f3ce625922c91b4fd/bip-0032.mediawiki


https://bitcoin.stackexchange.com/questions/76655/how-to-generate-public-and-private-key-pairs-from-the-12-seed-words-in-python

https://github.com/lyndsysimon/bip32utils


## bitsv でUploadは bcat.bico.media をつかっているのでこの仕様を

http://bcat.bico.media/
https://github.com/bico-media/bcat



wif_for_blob

https://github.com/richardkiss/pycoin/blob/de89fa4ffb5b7eb518c9ab2859c9d767f6b3e31d/pycoin/symbols/grs.py

b2a_base58

https://github.com/richardkiss/pycoin/blob/de89fa4ffb5b7eb518c9ab2859c9d767f6b3e31d/pycoin/encoding/b58.py


## bulk transaction

https://developers.whatsonchain.com/#bulk-transaction-details
