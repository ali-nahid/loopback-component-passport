# loopback-component-passport

## Overview

**Support of Realms Added**

You can pass and your realm in options object. For eg :

`options = {
  userRealm: <name-of-your-realm>,
  profileToUser: mapper ...
}` 

The module provides integration between [LoopBack](http://loopback.io) and
[Passport](http://passportjs.org) to support third-party login and account
linking for LoopBack applications.

<img src="./ids_and_credentials.png" width="600px" />

> Please see the [official documentation](http://loopback.io/doc/en/lb3/Third-party-login-using-Passport.html) for more information.

## All local accounts requires verification

### All third party accounts will login with an email of `uniqueID@loopback.provider.com` example `123456@loopback.facebook.com`

which will allow the user to link the social media accounts that they want as well as the users could sign up with the same email account that is used for facebook/twitter/google/local if they wish to keep them separate.

Facebook profile information (such as email, gender, timezone, etc) may still be included if necessary. See
https://github.com/strongloop/loopback-example-passport/blob/master/README.md#4-facebook-profile-info.

All user required info including the email will be available, but the main email for the account will remain `uniqueID@loopback.facebook.com`.

## Module Long Term Support Policy

This module adopts the [
Module Long Term Support (LTS)](http://github.com/CloudNativeJS/ModuleLTS) policy,
 with the following End Of Life (EOL) dates:

| Version | Status          | Published | EOL      |
| ------- | --------------- | --------- | -------- |
| 3.x     | Maintenance LTS | Dec 2016  | Dec 2020 |

Learn more about our LTS plan in [docs](https://loopback.io/doc/en/contrib/Long-term-support.html).
