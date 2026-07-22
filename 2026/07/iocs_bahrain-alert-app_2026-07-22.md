# IOCs: Fake Bahrain Alert App Deploys Android Surveillance Malware

**Source:** https://www.darkreading.com/mobile-security/fake-bahrain-alert-apps-android-surveillance-malware (Level 1) and https://dreamgroup.com/blog/how-a-fake-bahrain-civil-defense-app-turns-a-phone-into-a-listening-post (Level 2 - Dream Research Labs original report)
**Date collected:** 2026-07-22

## Malware Names & Aliases
- BH Alert (fake app name)
- OctagonPanel (RAT)
- Ward (RAT framework)
- WardClient
- GuardService
- OctagonCipher

## ip_address
- 10.0.0.1/24 (VPN tunnel address assigned by FenrirVpnService - private/non-routable)
- 1.1.1.1 (DNS advertised by malware - Cloudflare public DNS)
- 8.8.8.8 (DNS advertised by malware - Google public DNS)

*Note: 1.1.1.1 and 8.8.8.8 are legitimate public DNS services that the malware configures the device to use. 10.0.0.1/24 is a private IP range used for the VPN blackhole tunnel.*

## domain
- alert-bh.com (delivery domain, Google Play impersonation)
- bh-security.com (delivery domain, Bahrain government impersonation)
- alertbh.com (delivery domain)
- bh-alert.com (payload hosting domain)
- playgoogle.alertbh.com (Google Play impersonation page)
- download.alert-bh.com (download subdomain)
- download.bh-security.com (download subdomain)
- download.alertbh.info (download subdomain)

## url
- https://download.alert-bh.com
- https://download.bh-security.com
- https://playgoogle.alertbh.com
- https://download.alertbh.info
- https://download.alert-bh.com/BH-Alert.apk (payload download)
- https://download.bh-security.com/BH-Alert.apk (payload download)
- https://download.bh-security.com/assets/js/app.js?v=3 (tracking script)

## Android package name (domain-format indicators)
- com.old.stem (outer RC4 shell - Ematterassist)
- com.kit.kitty (lure/permission coercion stage)
- com.kisa.octagonpanel (final RAT payload)
- biz.rely.melt (nested RC4 shell - Hvoicemanual)

## sha256
*(No file hashes were published in either the Dark Reading article or the Dream research blog)*

## sha1
*(No file hashes were published)*

## md5
*(No file hashes were published)*

## meta_pixel_id
- 1688111402450882 (Meta Pixel ID used for tracking installs as Lead events on Variant B delivery pages)

## file_path
- assets/payload.base (second-stage APK embedded in the installer)
- assets/js/app.js?v=3 (external tracking script on bh-security.com)

## encrypted_container
- ZfChs.ttf (disguised font file containing encrypted DEX payload - outer shell)
- ZGdSEl.jar (encrypted container for nested shell)

## config_value
- passphrase: octagon-default-key-change-me (AES-GCM encryption passphrase for C2 traffic)
- RC4 key (outer shell): ct
- RC4 key (nested shell): NYrGT
- build_id: DevLRT
- protocol_version: 2

## Pages visited

- L1: https://www.darkreading.com/mobile-security/fake-bahrain-alert-apps-android-surveillance-malware (no technical IOCs found - news summary only)
- L2: https://dreamgroup.com/blog/how-a-fake-bahrain-civil-defense-app-turns-a-phone-into-a-listening-post (primary IOC source - Dream Research Labs technical analysis)
