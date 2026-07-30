# IOCs: Joyfill npm Packages – DEV#POPPER Node.js Malware

**Source:** https://thecyberexpress.com/joyfill-npm-packages-devpopper-nodejs-malware/ and https://socket.dev/blog/joyfill-npm-beta-releases-compromised
**Date collected:** 2026-07-29

ip_address:
- 166.88.134.62
- 23.27.13.43
- 23.27.202.27
- 198.105.127.210

domain:
- api.trongrid.io
- fullnode.mainnet.aptoslabs.com
- bsc-dataseed.binance.org
- bsc-rpc.publicnode.com
- ip-api.com

url:
- http://166.88.134.62:80
- https://166.88.134.62:443
- http://198.105.127.210:80
- https://198.105.127.210:443
- https://23.27.202.27:443
- http://23.27.202.27:27017
- https://23.27.13.43/$/boot
- /u/f
- /u/e
- /0x/js
- /verify-human/
- /verify-human/{campaign}
- /snv
- /d/python.zip
- /d/7zr.exe
- /d/python.7z
- /$/{id}
- /$/boot

sha256:
- adc4af90540d33cd1e98f44b51482ae9250fbeb97d6f8d7841c81b618cb2c6e6
- 8e8b90dedd456ded0c5748119836e1ca1066112bc569c1b41ca70eb931d1d4dc
- 5f6a92006ca2ea4b464d66fb41af777edce7296939a7c6ee491e2b3cbfe09848
- bcc93dc55bc7daedf4ca57254f0e7a7f1c40e09851eab98fe10cde801982db17
- 1352ad22c99983d91e600348b7cbf58235131b1ee34cea9f09623206d5b7dea7
- 67c6ef602cc850f10d935fee53fa40440df841adf081563bf4fc2631a71249ce
- c5742ea1875ecd2360022624149994909cd0546e221e4203dffd01f48de45469
- cb46f12d70824ea24ed1f8bcf45bf3f86680e02a9089aafc03b27f691be57be3
- f452f9cfa539f4a1fe25187a99a484391290d5dbaa422ba455edf6b04f81b7d1
- 78f0de8682e0e894a5784eb7e95db4da6088f528918ca3107dd1e76f80a561d8
- ae7565109fd01b88d82acf7f73ab20709cbc2c9f26fdea13e429ccc87a55d4fb
- 26351aed0397158d3a3b8cc8fd3047d4c015d264c9895f10f20f1521b974ed18
- 26e679eaf1e9baeb7c55eb48db482301171d4d26e1728544b23734a90dc70e1b
- 2cfede38fb121a71a2f3607474aa8cd588a99f51b37e5e6f0d8cb789fa275032
- 36ff00b45e67baa7e3674b0c80f48e88737264c61e5c6b3b091200972de8157c

email:
- (none identified as malware-related; editor@thecyberexpress.com and raj@thecyberexpress.com are benign site contacts)

## Additional technical indicators (blockchain/wallet addresses & payload markers)

### Tron addresses
- TMfKQEd7TJJa5xNZJZ2Lep838vrzrs7mAP
- TXfxHUet9pJVU1BgVkBAbrES4YUc1nGzcG
- TA48dct6rFW8BXsiLAtjFaVFoSuryMjD3v

### Aptos accounts
- 0xbe037400670fbf1c32364f762975908dc43eeb38759263e7dfcdabc76380811e
- 0x3f0e5781d0855fb460661ac63257376db1941b2bb522499e4757ecb3ebd5dce3
- 0x533b2dbcaeff19cd1f799234a27b578d713d8fcaa341b7501e4526106483e0b1

### BSC payload transactions
- 0x18a8420f727f2405f9d1805ad887b31029b584b2ff5a7ec0f57c72635183e99d
- 0x7ffb4efddd96e20aec90724be2ac9a71c138a9af697b9fb8224bbf80ea4f22be
- 0xb6c725890be6890fd2c735eedc47e24b85a350301f6c19a3864e43c35e470968

### XOR keys used by payload
- 2[gWfGj;<:-93Z^C
- m6:tTh^D)cBz?NM]
- ThZG+0jfXE6VAGOJ

### Persistence injection tags
- /*C250617A*/
- /*C250618A*/
- /*C250619A*/
- /*C250620A*/
- /*C260511A*/
- /*C260512A*/
- /*RS260605*/

### Affected npm packages (compromised)
- @joyfill/layouts@0.1.2-2773.beta.0
- @joyfill/components@4.0.0-rc24-2773-beta.4

### Safe versions (recommended)
- @joyfill/layouts@0.1.1
- @joyfill/components@4.0.0-rc24

## Pages visited

- L1: https://thecyberexpress.com/joyfill-npm-packages-devpopper-nodejs-malware/ (no specific IOCs on page – article references Socket.dev analysis)
- L2: https://socket.dev/blog/joyfill-npm-beta-releases-compromised (all IOCs above)
