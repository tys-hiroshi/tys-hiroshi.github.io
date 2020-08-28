【Powershell】テキストファイルを分割する

```
$i=0; cat .\test.txt -ReadCount 10000 | % { $_ > test$i.txt;$i++ }
```

http://souegg2.hatenablog.com/entry/2017/10/16/202230
