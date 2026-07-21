# IOCs: SleeperGem — RubyGems Supply Chain Attack

**Source:** https://thehackernews.com/2026/07/sleepergem-uses-three-malicious.html
**Date collected:** 2026-07-20

## domain

- git.disroot.org
- rubygems.org

## url

- https://git.disroot.org/git-ecosystem
- https://rubygems.org/gems/git_credential_manager
- https://rubygems.org/gems/Dendreo
- https://rubygems.org/gems/fastlane-plugin-run_tests_firebase_testlab

## Malicious RubyGems packages (note: not standard IOC types but critical artifacts)

- git_credential_manager (versions 2.8.0, 2.8.1, 2.8.2, 2.8.3)
- Dendreo (versions 1.1.3, 1.1.4)
- fastlane-plugin-run_tests_firebase_testlab (version 0.3.2)

## Affected dependent packages (added malicious gems as dependencies)

- slackHtmlToMarkdown
- seo_optimizer
- array_fast_methods

## Artifacts (file paths to hunt)

- $HOME/.local/share/gcm/git-credential-manager
- $HOME/.local/share/gcm/.env
- /usr/local/sbin/ping6

## Payload files

- deploy.sh

## Compromised RubyGems accounts

- LR-DEV (maintainer of git_credential_manager, Dendreo, slackHtmlToMarkdown, seo_optimizer, array_fast_methods)
- pinkroom (maintainer of fastlane-plugin-run_tests_firebase_testlab)

## Pages visited

- L1: https://thehackernews.com/2026/07/sleepergem-uses-three-malicious.html
- L2: https://www.stepsecurity.io/blog/sleepergem-compromised-rubygems-drop-persistent-backdoor
- L2: https://www.aikido.dev/blog/sleepergem-rubygems-supply-chain-attack

## Notes

- No IP addresses, SHA256/SHA1/MD5 hashes, or email addresses were found in the articles.
- The primary C2 infrastructure is the public Forgejo instance at git.disroot.org under the path `/git-ecosystem`.
- The malicious gems impersonate legitimate tools (git_credential_manager impersonates Microsoft's Git Credential Manager).
- No hashes for the dropped binaries were published as the binary payload analysis was not included in any of the three articles.
- Behavioral indicators: Outbound HTTPS to git.disroot.org with User-Agent "Git" and certificate verification disabled; Ruby process spawning child install script upon require.
