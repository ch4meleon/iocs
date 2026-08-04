# IOCs: H96 Android TV Box Ad Fraud & Residential Proxy (Fuyao / BADBOX)

**Source:** https://hackread.com/h96-android-tv-boxes-ad-fraud-residential-proxies/
**Date collected:** 2026-08-03

domain:
- catmore88.com
- ipmoyu.com
- 911.re

## Notes

- `catmore88.com` and `ipmoyu.com` are command-and-control (C2) domains for BADBOX 2.0, reported in the HackRead article "BADBOX 2.0 Found Preinstalled on Android IoT Devices Worldwide" (L2), which is closely related to the H96/Fuyao ad-fraud and residential-proxy campaign described at the source URL.
- `911.re` is the domain of the 911.re residential proxy service (L3 article about its 2022 shutdown/breach). It is contextually related (residential proxy abuse) but NOT confirmed as Fuyao/BADBOX C2 infrastructure — included with uncertainty.
- Related malware artifacts (not standard IOC types, for context): `libanl.so` (native backdoor), `p.jar` / `q.jar` (Java dropper modules), `com.hs.app` (system-level loader app) for BADBOX 2.0; `DGBLuancher` / `Corejava classes.dex` (T95); `Android.Triada.231` (Triada trojan).
- The primary L1 article itself contained no explicit IOCs in its visible text. Original off-domain research reports (Bitsight, Point Wild, Human Security) were not crawled per the same-domain crawl rule and likely contain additional IOCs.

## Pages visited

- L1: https://hackread.com/h96-android-tv-boxes-ad-fraud-residential-proxies/ (no IOCs)
- L2: https://hackread.com/android-tv-boxes-backdoors-home-networks/ (no IOCs)
- L2: https://hackread.com/badbox-2-0-preinstalled-android-iot-devices-worldwide/
- L2: https://hackread.com/monero-mining-malware-infect-android-smart-tv-phones/ (no IOCs)
- L3: https://hackread.com/amazon-t95-tv-box-pre-installed-malware/ (no IOCs)
- L3: https://hackread.com/malware-targets-iot-devices-android-tv/ (no IOCs)
- L3: https://hackread.com/preinstalled-trojan-in-cheap-android-devices-steal-data-intercept-chats/ (no IOCs)
- L3: https://hackread.com/911-911-re-proxy-shuts-down-confirms-data-breach/
- L3: https://hackread.com/hundreds-of-android-devices-shipped-with-pre-installed-malware/ (no IOCs)
