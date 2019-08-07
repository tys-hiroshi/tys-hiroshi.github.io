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
