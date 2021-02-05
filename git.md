### Add submodule

```
git submodule add -b develop https://github.com/tys-hiroshi/StorageLib.git StorageAPI/Libraries/StorageLib
```

### Remove submodule

```
git submodule deinit StorageAPI/Libraries/StorageLib
git rm StorageAPI/Libraries/StorageLib 
```


### git clone private repository

https://help.github.com/ja/github/authenticating-to-github/connecting-to-github-with-ssh

You need to do blow.

- 既存の SSH キーの確認

- 新しい SSH キーを生成して ssh-agent に追加する

- GitHub アカウントへの新しい SSH キーの追加

When u can above, u can clone private repository.

$ git clone git@github.com:tys-hiroshi/{repositoryname}.git


### count code

```
$ git ls-files '*.js' '*.ts' '*.json' | xargs -n1 git --no-pager blame -w | wc -l

$ git ls-files '*.ts' | xargs -n1 git --no-pager blame -w | wc -l
```

