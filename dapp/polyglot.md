```
upload_b
↓
b_send_from_file(self, file, media_type=None, encoding=None, file_name=None)
↓

1.b_create_rawtx_from_file → b_create_rawtx_from_binary → create_pushdata, create_transaction


from bitsv import op_return
op_return.create_pushdata

filter_utxos_for_bcat → get_unspents 

self.create_transaction(outputs=[], message=lst_of_pushdata, combine=False, custom_pushdata=True, unspents=utxos[-1:]) ? → bitsv/wallet.py の create_transaction

https://github.com/AustEcon/bitsv/blob/31f585ae9784ec8d7be415f80570a2dbecda1ca2/bitsv/transaction.py

create_p2pkh_transaction(private_key, unspents, outputs, custom_pushdata=False)



2.send_rawtx
```
