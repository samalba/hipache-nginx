Hipache-Nginx (experimental)
============================

This projects is an experimental port of [Hipache](https://github.com/dotcloud/hipache)
to nginx using the [Lua module](https://github.com/chaoslawful/lua-nginx-module).

The project only consists of configuration files for now but it will
evolve into a ready-to-use scalable proxy solution.

1. Nginx requires the LUA module: [installation instructions](http://wiki.nginx.org/HttpLuaModule#Installation)
2. You have to install the [lua-redis client](https://github.com/agentzh/lua-resty-redis).


Health-checks
-------------

Dead backends won't be marked as dead in Redis, they will only
be *announced* as dead. This is on purpose since it's possible to have a delay
between the dead detection and the announcement with the current
implementation.

This is not a blocker for production deployment, you will need
to monitor the "dead" channel with the [Hipache-hchecker](https://github.com/samalba/hipache-hchecker/).
