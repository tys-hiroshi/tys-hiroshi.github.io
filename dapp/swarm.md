## Geth Install

https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Ubuntu

```
~$ geth account new
INFO [12-07|14:23:10.099] Maximum peer count                       ETH=50 LES=0 total=50
INFO [12-07|14:23:10.099] Smartcard socket not found, disabling    err="stat /run/pcscd/pcscd.comm: no such file or directory"
Your new account is locked with a password. Please give a password. Do not forget this password.
Password: 
Repeat password: 

Your new key was generated

Public address of the key:   0x14Bf8b2d11F64a05485C1A79ff300932c59390D4
Path of the secret key file: /home/th4/.ethereum/keystore/UTC--2019-12-07T05-23-12.981108744Z--14bf8b2d11f64a05485c1a79ff300932c59390d4

- You can share your public address with anyone. Others need it to interact with you.
- You must NEVER share the secret key with anyone! The key controls access to your funds!
- You must BACKUP your key file! Without the key, it's impossible to access account funds!
- You must REMEMBER your password! Without the password, it's impossible to decrypt the key!
```


http://kojiryo.com/1116/

https://github.com/ethersphere


https://github.com/ethersphere/swarm-guide/blob/master/contents/installation.rst

$ sudo apt-get install software-properties-common
$ sudo add-apt-repository -y ppa:ethereum/ethereum

$ sudo apt-get update
$ sudo apt-get install ethereum-swarm
