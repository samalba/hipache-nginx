Hipache-Nginx (experimental)
============================

This projects aims to replace the work done in [Hipache](https://github.com/dotcloud/hipache)
by nginx using the [Lua module](https://github.com/chaoslawful/lua-nginx-module).

The projects only consists of a some configuration files for now but it will
soon evolve in a ready-to-use scalable proxy solution.

1. Nginx requires the LUA module: [installation instructions](http://wiki.nginx.org/HttpLuaModule#Installation)
2. You have to install the [lua-redis client](https://github.com/agentzh/lua-resty-redis).


Health-checks
-------------

All dead backends won't be marked as dead in the Redis, they will be only
announced to be dead. This is on purpose since it's possible to have a delay
between the dead detection and the announcement with the current
implementation.

This is not a blocker to run this in production, you will need
to monitor the "dead" channel with the [Hipache-hchecker](https://github.com/samalba/hipache-hchecker/).
