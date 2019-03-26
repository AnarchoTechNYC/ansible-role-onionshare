# Anarcho-Tech NYC: OnionShare [![Build Status](https://travis-ci.org/AnarchoTechNYC/ansible-role-onionshare.svg?branch=master)](https://travis-ci.org/AnarchoTechNYC/ansible-role-onionshare)

This role builds and configures an [OnionShare](https://onionshare.org/) receiver. Notably, this role has been tested with [Raspbian](https://www.raspbian.org/) on [Raspberry Pi](https://www.raspberrypi.org/) hardware. This role's purpose is to make it simple to prepare a host that is not security-critical to anonymously receive files. For security-critical applications, please use [SecureDrop](https://securedrop.org/) instead.

## Role variables

* `onionshare_username`: The user that will be running OnionShare. For public shares, this user's disk space should be restricted [using disk quotas](https://github.com/AnarchoTechNYC/ansible-role-common/blob/master/README.md#configuring-disk-quotas).
* `onionshare_data_dir`: Path to OnionShare's `data_dir`, the filesystem location in which received files will be saved.
* `onionshare_private_key`: The private key for the Tor Onion service managed by OnionShare, as prepared by OnionShare. This should be a Base64-encoded X25519 private key. See [Generating authentication credentials for version 3 Onion services](https://github.com/AnarchoTechNYC/meta/wiki/Connecting-to-an-authenticated-Onion-service#generating-authentication-credentials-for-version-3-onion-services) on [the Anarcho-Tech NYC meta wiki](https://github.com/AnarchoTechNYC/meta/wiki).
* `onionshare_public_mode`: Whether or not to enable [OnionShare's Public mode](https://github.com/micahflee/onionshare/wiki/Public-Mode).
