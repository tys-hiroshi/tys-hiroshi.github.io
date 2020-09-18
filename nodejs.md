# Node.js

nのインストール
$ npm install -g n

check stable version 

$ n --stable

$ node -v

バージョンの切り替え

$ n

install stable version

$ sudo n stable



npmのアップデート
npmのほうはシンプルです。以下のコマンドでアップデートできます。

$ npm update -g npm



https://www.cypress.io/

$ npm install cypress

$ sudo apt-get install libgtk2.0-0 libgtk-3-0 libgbm-dev libnotify-dev libgconf-2-4 libnss3 libxss1 libasound2 libxtst6 xauth xvfb

https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements



```
$ sudo apt install -y nodejs npm

$ sudo npm install n -g

$ sudo n stable

$ sudo apt purge -y nodejs npm
$ exec $SHELL -l

$ node -v

```

Configure npm global directory

```
$  mkdir ~/.npm-global
$  npm config set prefix '~/.npm-global'
$  echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.profile
$  source ~/.profile
$  npm completion >> ~/.bashrc
```

## package uninstall

```
npm uninstall openzeppelin-solidity
```

## update packages

```
npm install -g npm-check-updates
```

## stable な node.jsをつかう

```
npm install -g n
which n
> /home/th4/.npm-global/bin/n
sudo /home/th4/.npm-global/bin/n stable
```

