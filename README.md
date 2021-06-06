# Supermininghash
https://github.com/P7-33/Supermininghash.wiki.git
Support mining
Skip to content
Sign up
Supermininghash
/
SUPERHASHMININING
Code
Issues
106
Pull requests
2
Security
Insights
v37.6
 master
 v37.6
  6  readme.md 
@@ -36,46 +36,47 @@
* Support Windows & Linux.
* Support backup mining pool configuration.
* Support SSL connection to mining pools.
* Dev Fee: 
  * ethash etchash 1%
  * cuckatoo & cuckatoo32 & cuckoo_ae 2%
  * progpow_sero 2%
  * kawpow 2%
  * beamv3 2%
  * octopus 3%
  * ergo 2%
## Requirements
- **NVIDIA Driver version: >= 384**.
- Nvidia GPU Specific Requirements:
| Algorithm        |  Coin   | Compute Capability | Memory (Win7 & Linux) | Memory (Win10) |
| :--------------- | :-----: | :----------------: | :-------------------: | :------------: |
| ethash           |   ETH   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          5GB          |      6GB      |
| cuckatoo         | GRIN31  | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          8GB          |      10GB      |
| cuckatoo32 | GRIN32 | 6.0, 6.1, 7.0, 7.5 | 8GB | 10GB |
| cuckoo_ae        |   AE    | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          5GB          |      6GB       |
| progpow_sero     |  SERO   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          3GB          |      4GB      |
| kawpow           |   RVN   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          3GB          |      4GB      |
| beamv3 | BEAM | 6.0, 6.1, 7.0, 7.5 | 3GB | 3GB |
| octopus | CFX | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 | 5GB | 6GB |
| ergo | ERGO | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 | 3GB | 3GB |
- \* Compute Capability reference link: [wikipedia](<https://en.wikipedia.org/wiki/CUDA#GPUs_supported>)
## Sample Usages
#### ETH
- **ethermine:** nbminer -a ethash -o ethproxy+tcp://asia1.ethermine.org:4444 -u 0x12343bdgf.worker
- **sparkpool:** nbminer -a ethash -o ethproxy+tcp://cn.sparkpool.com:3333 -u 0x12343bdgf.worker
- **f2pool:** nbminer -a ethash -o ethproxy+tcp://eth.f2pool.com:8008 -u 0x12343bdgf.worker
- **beepool:** nbminer -a ethash -o ethproxy+tcp://eth-pool.beepool.org:9530 -u 0x12343bdgf.worker
- **nanopool:** nbminer -a ethash -o ethproxy+tcp://eth-asia1.nanopool.org:9999 -u 0x12343bdgf.worker
- **herominers:** nbminer -a ethash -o ethproxy+tcp://ethereum.herominers.com:10201 -u 0x12343bdgf.worker
- **nicehash:** nbminer -a ethash -o nicehash+tcp://daggerhashimoto.eu.nicehash.com:3353 -u btc_address.worker
- **miningpoolhub**: nbminer -a ethash -o nicehash+tcp://asia.ethash-hub.miningpoolhub.com:20535 -u username.worker

#### ETH+ZIL:

@@ -274,6 +275,11 @@ GET http://api_host:port/api/v1/status

## Change Log

#### v37.6(2021-06-03)

- `fix`: `ethash` `--enable-dag-cache` cause crash on AMD GPUs when switch DAG file.
- `fix`: `ergo` support on `AMD Vega` GPUs.

#### v37.5(2021-05-21)

​    changes from 37.3
  6  readme_zh.md 
@@ -69,6 +69,7 @@ NVIDIA、AMD显卡的`ETH`, `RVN`,  `GRIN`, `BEAM`, `CFX`, `ZIL`, `ERGO`, `AE`,
- **beepool:** nbminer -a ethash -o ethproxy+tcp://eth-pool.beepool.org:9530 -u 0x12343bdgf.worker
- **nanopool:** nbminer -a ethash -o ethproxy+tcp://eth-asia1.nanopool.org:9999 -u wallet.worker
- **nicehash:** nbminer -a ethash -o nicehash+tcp://daggerhashimoto.eu.nicehash.com:3353 -u btc_address.worker
- **miningpoolhub**: nbminer -a ethash -o nicehash+tcp://asia.ethash-hub.miningpoolhub.com:20535 -u username.worker

#### ETH+ZIL:

@@ -266,6 +267,11 @@ GET http://api_host:port/api/v1/status

## 修改记录

#### v37.6(2021-06-03)

- `修复`: `ethash` `--enable-dag-cache` 在A卡上切换epoch时可能导致崩溃的情况
- `修复`: `ergo` 在`Vega`显卡的支持

#### v37.5(2021-05-21)

​    changes from 37.3
0 comments on commit 17d36ae
Please sign in to comment.
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About

