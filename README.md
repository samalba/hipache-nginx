Hipache-Nginx (experimental)
============================

This projects aims to replace the work done in [Hipache](https://github.com/dotcloud/hipache)
by nginx using the [Lua module](https://github.com/chaoslawful/lua-nginx-module).

The projects only consists of a some configuration files for now but it will
soon evolve in a ready-to-use scalable proxy solution.

1. Nginx requires the LUA module: [installation instructions](http://wiki.nginx.org/HttpLuaModule#Installation)
2. You have to install the [lua-redis client](https://github.com/agentzh/lua-resty-redis).
