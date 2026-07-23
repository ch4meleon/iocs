# IOCs: Lampion Banking Trojan Campaign — Brazil/Portugal

**Source:** https://www.darkreading.com/cyberattacks-data-breaches/brazilian-banking-trojan-spreading-portugal
**Date collected:** 2026-07-23

## Campaign Overview

Lampion (ChePro-derived Brazilian banking Trojan) actively targeting Portuguese organizations via phishing emails. Multistage infection chain: ZIP → HTML → VBS → VBS → DLL (RAT). Heavy obfuscation and junk padding used throughout. Sources: Acronis TRU (July 2026) and Unit 42 (May 2025) reports.

---

### ip_address

18.218.184.201
18.222.100.142
3.135.194.95
3.139.85.102
3.141.199.105
3.144.37.134
3.148.240.228
3.150.134.118
52.14.160.173
5.8.9.77
83.242.96.159
18.221.69.167
18.222.97.143
18.116.15.129
18.220.96.58
3.135.200.135
18.191.192.110
18.224.38.123
18.118.163.100
3.147.127.14
3.138.32.196
18.117.11.70
18.117.173.119
18.116.28.153
3.16.76.203
3.15.7.241
3.15.155.141
18.117.71.203
3.133.160.140
3.133.113.215
3.143.24.42
18.217.180.185
3.23.105.171
3.142.200.117
3.128.34.187
18.191.240.233
3.147.86.100

### domain

auto-contabilistica.com
autoridade-contabilistica.org
autoridade-financeira.com
fat-contabislitaca.com
inde-faturas.com
autoridade-tributaria.com

### url

hxxp://18.218.184.201/03_metal7342/trapezio.php
hxxp://18.222.100.142/17_moldura8210/regerem.php
hxxp://18.222.100.142/18_prateleira1967/revigore.php
hxxp://3.135.194.95/09_nsabdo/receado.php
hxxp://3.139.85.102/17_eudhfj/regerem.php
hxxp://3.139.85.102/18_vdsyuh/revigore.php
hxxp://3.139.85.102/20_fjegydk/destravares.php
hxxp://3.141.199.105/13_ytdshe/reimpresso.php
hxxp://3.141.199.105/15_rjhsymc/unificador.php
hxxp://3.141.199.105/16_kdsgyue/raquete.php
hxxp://3.144.37.134/01_sdneow/fruais.php
hxxp://3.144.37.134/02_sjdhie/reestruturado.php
hxxp://3.144.37.134/03_osneops/trapezio.php
hxxp://3.148.240.228/05_dnwodu/equivaler.php
hxxp://3.148.240.228/06_sndiwds/galgassem.php
hxxp://3.150.134.118/05_papel6197/equivaler.php
hxxp://3.150.134.118/06_couro8254/galgassem.php
hxxp://52.14.160.173/10_algodao9148/reunia.php
hxxps://fat-contabislitaca.com/js/1898.php
http://18.116.63.61/ifeellike.php
http://18.116.63.61/trogloditas.php
http://3.135.249.199/prayfor.php
http://18.217.122.187/proposito.php
http://18.226.150.56/persistir.php
http://3.142.40.36/grow.php
http://18.216.78.94/aceitalo.php
http://3.23.103.13/stick.php

### sha256

87efeada5fe39a94cefc6151fd84af223d0e0e2b070daec606274481ed87b87b
ab46f7c4d3f717bb1e61d2f236917976d2a85be6958ae099fee79ea6e9031e37
b1c101bd1ba134ffbea61f9fac2b7c8fbd13ca113a37944abdc131ef86da92ac
c6618bb692fb3f5d7959f8db1fedaaac5e8a36fb901397a008aa2b88874448fd
036c8f32012abdcb9a389ae9c284da89505e830bca74eb1aa9ea3794b067aab6
d25d32478ae67403484a309591b6409224d26ca3d094c5ccd8428ebef7efcfd1
643c0093baec45952a46b0210f7a6f8fb26883b396b66f1cb609c5b55e6dae1e
050e84d134a32ed7c4885a9d57ce37f8ae5f910960b67e2156941961bd5781ba
7ad89fb0a4a5449a381b8f540238193019673adc7cfb1c008dcd14a745891551
1bd347ce5deee3d783a038e2d2d224bc30cc074e0471a3897c5409ce99816dc9
1541c23f34eb05dfcbede3830741427681d719cee1dfd397a2c04110e0fa81b2
fe769fd85a7440751e1508614c8d9ef0de00bece803329bf3318ff863a146216
ee4c8e4cce55bd40afa1fb0bc0eee3d7c23d0ebe2db48c2092e854f6ca1472ce
4aeb84dd71588a35084109ff5525c7bff2f30e0ed58ce139621b17f2374bdb35
bba48cf24bb9e6bdcbc79c2241f101e3dd4127ab450e3dbbe1b79fa738f06483
29b63fcf8e5f08fd12166507b3a85746e3ec685ae0620a124e64125ecd9ccf9b
58fe2a7d4435c9c24c98d33aff1110add4bf95add31558f51289a028ddafcc6e
334dfbaefbf7e6301d2385f95d861eb6dae9018c48fb298a2cbf5f364fbcdb2d
1681c3b88ed315543ac1bf07d258d560cf2f85bfd26c10471d71700eaeb57fb3

## Pages visited

- L1: https://www.darkreading.com/cyberattacks-data-breaches/brazilian-banking-trojan-spreading-portugal (no IOCs — news summary only)
- L2: https://www.acronis.com/en/tru/posts/lampions-portugal-focused-phishing-campaign-delivers-multistage-malware/ (IOCs found)
- L2: https://unit42.paloaltonetworks.com/lampion-malware-clickfix-lures/ (IOCs found)
- L2: https://seguranca-informatica.pt/targeting-portugal-a-new-trojan-lampion-has-spread-using-template-emails-from-the-portuguese-government-finance-tax/ (blocked by Cloudflare)
