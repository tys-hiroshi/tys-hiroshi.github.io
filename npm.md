Configure npm global directory

```
$  mkdir ~/.npm-global
$  npm config set prefix '~/.npm-global'
$  echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.profile
$  source ~/.profile
$  npm completion >> ~/.bashrc
```
