## Pypi

https://qiita.com/icoxfog417/items/edba14600323df6bf5e0



setup.py の description は一行でないと long_descriptionの表示が乱れてしまう。


## pypi にinstall したいPackageがないとき (pip insatll {packagename})

github にあるなら、clone して setup.py を実行

```
python setup.py develop
```
