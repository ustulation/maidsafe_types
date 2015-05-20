# maidsafe_types

|Crate|Travis|Appveyor|Coverage|
|:------:|:-------:|:-------:|:-------:|
|[![](http://meritbadge.herokuapp.com/maidsafe_types)](https://crates.io/crates/maidsafe_types)|[![Build Status](https://travis-ci.org/maidsafe/maidsafe_types.svg?branch=master)](https://travis-ci.org/maidsafe/maidsafe_types)|[![Build status](https://ci.appveyor.com/api/projects/status/bxjlrqhqdg3dc5y8/branch/master?svg=true)](https://ci.appveyor.com/project/dirvine/maidsafe-types-pgsk8/branch/master)|[![Coverage Status](https://coveralls.io/repos/maidsafe/maidsafe_types/badge.svg)](https://coveralls.io/r/maidsafe/maidsafe_types)|

| [ API Documentation](http://maidsafe.github.io/maidsafe_types/) | [MaidSafe System Documention](http://systemdocs.maidsafe.net/) | [MaidSafe web site](http://www.maidsafe.net) | [Safe Community site](https://forum.safenetwork.io) |


###Pre-requisite:
libsodium is a native dependency for [sodiumxoide](https://github.com/dnaq/sodiumoxide). Thus, install sodium by following the instructions [here](http://doc.libsodium.org/installation/README.html).

For windows, download and use the [prebuilt mingw library](https://download.libsodium.org/libsodium/releases/libsodium-1.0.2-mingw.tar.gz).
Extract and place the libsodium.a file in "bin\x86_64-pc-windows-gnu" for 64bit System or "bin\i686-pc-windows-gnu" for a 32bit system.

#Todo
- [ ] Anonymous public types to be included as part of the body of the public type
- [ ] Change tests to reflect the above task
- [ ] Remove name from types to enhance type invariance
- [ ] Add a member of signature type to Id types. The signature in pure keys is sign_using_own_private_key(public keys + type tag). And in dependent keys, is sign_using_owner_private_key(public keys + owner public key + type tag)
- [ ] add SafeCoin entry type which should have i) owners, ii) previous owners and iii) signatures created by previous owners to verify the transaction approved by them, and iv) Type tag
- [ ] Implement and test Sendable, Encodable, Decodable, PartialEq and fmt::Debug traits for SafeCoin Type
- [ ] Remove maid_signature and mpid_signature from PublicMaid and PublicAnMaid
- [ ] Provide Shona with modifications required in Types representations
- [ ] Write tests to confirm invariants of all types
