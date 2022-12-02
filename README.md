## Aleo Testnet3 Multiple GPU Prover

Make sure you have install Nvidia driver and cuda toolkit
for install cuda toolkit please flow : (here is cudatoolkit 11.8 for ubuntu 20.04)
https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=20.04&target_type=runfile_local

after download run file, execute below command:
```
sudo sh cuda_11.8.0_520.61.05_linux.run
```
flow prompt, make sure unselect driver, only install toolkit

after install cuda toolkit, run below to check:
```
nvcc --version
nvidia-smi
```
make sure all info output correct.

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

