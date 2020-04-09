## Create env

```
conda create -n py37 python=3.7 anaconda
```


def get_tx(addr = ''):
    try:
        start_index_str = request.args.get('start_index')
        if start_index_str == "":
            start_index = 0
            else: 
                start_index = 
        cnt_str = request.args.get('cnt')
        if cnt_str == "":
            cnt = 5
        else:
            cnt = int(cnt_str)
        print("addr: %s; start_index:%s;cnt: %s" % (addr, start_index, cnt))
        # search mongodb transaction records from start_index to cnt.
        trans_list = []
        transaction_list = mongo.db.transaction.find()
