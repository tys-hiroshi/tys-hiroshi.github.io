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

```
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository -y ppa:ethereum/ethereum

$ sudo apt-get update
$ sudo apt-get install ethereum-swarm
$ swarm version
Swarm
Version: 0.4.3-stable
Git Commit: 66e016c6dc71abadf4a18ecf8688cf66079f6212
Go Version: go1.11.5
OS: linux

```

create new account

```
$ geth account new
INFO [02-01|20:10:18.853] Maximum peer count                       ETH=50 LES=0 total=50
INFO [02-01|20:10:18.853] Smartcard socket not found, disabling    err="stat /run/pcscd/pcscd.comm: no such file or directory"
Your new account is locked with a password. Please give a password. Do not forget this password.
Password: 
Repeat password: 

Your new key was generated

Public address of the key:   0x564d05E22AC8b678fBe8e91C341e5BEBA65051e1
Path of the secret key file: /home/th4/.ethereum/keystore/UTC--2020-02-01T11-10-22.622224149Z--564d05e22ac8b678fbe8e91c341e5beba65051e1

- You can share your public address with anyone. Others need it to interact with you.
- You must NEVER share the secret key with anyone! The key controls access to your funds!
- You must BACKUP your key file! Without the key, it's impossible to access account funds!
- You must REMEMBER your password! Without the password, it's impossible to decrypt the key!


$ swarm --bzzaccount 0x564d05E22AC8b678fBe8e91C341e5BEBA65051e1
INFO [02-01|20:12:02.943] Maximum peer count                       ETH=50 LES=0 total=50
Unlocking swarm account 0x564d05E22AC8b678fBe8e91C341e5BEBA65051e1 [1/3]
Passphrase: 
INFO [02-01|20:12:09.352] Starting peer-to-peer node               instance=swarm/v0.4.3-66e016c6/linux-amd64/go1.11.5
INFO [02-01|20:12:09.523] New local node record                    seq=1 id=caec887dc8e49c34 ip=127.0.0.1 udp=30399 tcp=30399
INFO [02-01|20:12:09.523] Updated bzz local addr                   oaddr=7ee05a590af441ce1efd95bf2087192a792df41852f3c42960626ba3deb725e8 uaddr=enode://27eebe365880cd5c2c3faca420e5aa0726334815fa2ceb12c20b0fdb974a5c2d8a833688559e7089d332604be20440efcb4b20116778578b47d64ce9b22f7278@127.0.0.1:30399
INFO [02-01|20:12:09.523] Starting bzz service 
INFO [02-01|20:12:09.523] Starting hive                            baseaddr=7ee05a59
INFO [02-01|20:12:09.523] Detected an existing store. trying to load peers 
INFO [02-01|20:12:09.523] hive 7ee05a59: no persisted peers found 
INFO [02-01|20:12:09.523] Swarm network started                    bzzaddr=7ee05a590af441ce1efd95bf2087192a792df41852f3c42960626ba3deb725e8
INFO [02-01|20:12:09.525] Started P2P networking                   self=enode://27eebe365880cd5c2c3faca420e5aa0726334815fa2ceb12c20b0fdb974a5c2d8a833688559e7089d332604be20440efcb4b20116778578b47d64ce9b22f7278@127.0.0.1:30399
INFO [02-01|20:12:09.525] Started Pss 
INFO [02-01|20:12:09.525] Loaded EC keys                           pubkey=0x04f013f5bc6068eb1060600f7793335dafd0af0dd37656f3f36b6d5a06a210637d0b4aa271532f3096f705532918a7d0c522c7cfcf0f8a987b00ef76476ac7fea6 secp256=0x02f013f5bc6068eb1060600f7793335dafd0af0dd37656f3f36b6d5a06a210637d
INFO [02-01|20:12:09.525] Streamer started 
INFO [02-01|20:12:09.525] Starting Swarm HTTP proxy                port=8500
INFO [02-01|20:12:09.529] IPC endpoint opened                      url=/home/th4/.ethereum/bzzd.ipc
INFO [02-01|20:12:09.532] Mapped network port                      proto=tcp extport=30399 intport=30399 interface=NAT-PMP(192.168.179.1)
INFO [02-01|20:12:09.534] Mapped network port                      proto=udp extport=30399 intport=30399 interface=NAT-PMP(192.168.179.1)
INFO [02-01|20:12:09.702] New local node record                    seq=2 id=caec887dc8e49c34 ip=10.136.23.195 udp=30399 tcp=30399

$ swarm up ./testfile.md 
1b7912a83f21244d79602fe62e9c5ef7065b729520b3a707dd377b1eb6ff402f

```
