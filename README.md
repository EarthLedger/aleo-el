## Aleo Testnet3 Multiple GPU Prover

Extrat ubuntu.tgz:
```
tar -xvzf ./ubuntu.tgz
cd ./ubuntu
```

First create your Aleo accout:
```
./snarkos account new

Private Key  APrivateKey1zkpGiX2h2okjvLJuAGS6XuDrWyn2BgShfAxFr12zzuLg5ue
   View Key  AViewKey1meERjGDnS4bNckaPrrrnwEbm9NmAFsFndzjHTv3MrxDg
    Address  aleo19wnavj9j9g62uptngsd8tekm85a4wzjew4hzeae8zau0fkw4mqzs8kjj8h

```
copy your key to a safe place, and copy Private Key, here is APrivateKey1zkpGiX2h2okjvLJuAGS6XuDrWyn2BgShfAxFr12zzuLg5ue  
open address.sh, paste to the end, for example:
```
./snarkos start --nodisplay --prover APrivateKey1zkpGiX2h2okjvLJuAGS6XuDrWyn2BgShfAxFr12zzuLg5ue
```

then start prover:
```
./run.sh
```

you can check your log output with below command:
```
tail -f log
```

