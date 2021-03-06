CHANGELOG
=========


Version 1.2.0 (released in 2012-09-04)
--------------------------------------

- [(c921687)](https://github.com/versatica/OverSIP/commit/c9216872ccd43c3977b8816551f33d9d0c178899) Added `on_target()` and `abort_routing()` methods for `Proxy` class.

- [(7e54d1c)](https://github.com/versatica/OverSIP/commit/7e54d1c89351e0517bc12d543e577dff46f251a4) Don't raise an exception if the received STUN request contains an invalid IP family (vulnerability!).

- [(f7eefd6)](https://github.com/versatica/OverSIP/commit/f7eefd6d8e02d30e61fd219f4426e6e63ea7f2a8) If request.from or request.to (`NameAddr` instances) are modified before routing the request, changes are applied for the outgoing request and reverted when sending responses upstream.

- [(0f9d3ec)](https://github.com/versatica/OverSIP/commit/0f9d3ec9da96c51197535bcd5f0c65e5749ec855) If request.contact `NameAddr` fields are modified then changes are applied in the forwarded request.

- [(df1389e)](https://github.com/versatica/OverSIP/commit/df1389eda22806dc48f6595cc3e6460c58391411) Added `SystemCallbacks` module for 3rd party modules to set custom callbacks when OverSIP is started, reloaded (HUP signal) or stopped.

- [(9d310d6)](https://github.com/versatica/OverSIP/commit/9d310d6678ee79c47d17b5aab010a49b8683c3da) Added `OverSIP::SIP::Uri#aor()`method which returns "sip:user@domain" for a SIP/SIPS URI (no port or params) and "tel:number" for a TEL URI (no params).

- [(56e099b)](https://github.com/versatica/OverSIP/commit/56e099bb0500e6cda221750ade7848fda614b522) Added a new method `OverSIP::SystemEvents.on_initialize()` useful for 3rd party modules configuration by the user.

- [(aac4bad)](https://github.com/versatica/OverSIP/commit/aac4badafd924cdbd3344a6636fa9588d0b84c79) `OverSIP::SIP::Modules::RegistrarWithoutPath` renamed to `OverSIP::SIP::Modules::OutboundMangling`.

- [(ce48977)](https://github.com/versatica/OverSIP/commit/ce48977ca786def6d9c9f8af8d743da7c105dcf6) `OverSIP::SIP::Modules::Core` moved to `OverSIP::SIP::Core`.

- [(98e5308)](https://github.com/versatica/OverSIP/commit/98e530869e57150778327b29e5a977b2f6985f8d)` OverSIP::SIP::Modules` moved to `OverSIP::Modules`.


Version 1.1.2 (released in 2012-08-28)
--------------------------------------

- [(d91d2e4)](https://github.com/versatica/OverSIP/commit/d91d2e4899a777dd7dd101e83fe36a1bca744398) Require EventMachine-LE >= 1.1.3 which includes the `:use_tls` option for selecting TLSv1 or SSLv23 (fixes [#12](https://github.com/versatica/OverSIP/issues/12)).
