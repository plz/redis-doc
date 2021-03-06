Introduction to Redis
===

Redis is an open source, BSD licensed, advanced **key-value cache** and **store**.  It is often referred to as a **data structure server** since
keys can contain [strings](/topics/data-types-intro#strings), [hashes](/topics/data-types-intro#hashes), [lists](/topics/data-types-intro#lists), [sets](/topics/data-types-intro#sets), [sorted sets](/topics/data-types-intro#sorted-sets), [bitmaps](/topics/data-types-intro#bitmaps) and [hyperloglogs](/topics/data-types-intro#hyperloglogs).

You can run **atomic operations**
on these types, like [appending to a string](/commands/append);
[incrementing the value in a hash](/commands/hincrby); [pushing an element to a
list](/commands/lpush); [computing set intersection](/commands/sinter),
[union](/commands/sunion) and [difference](/commands/sdiff);
or [getting the member with highest ranking in a sorted
set](/commands/zrangebyscore).

In order to achieve its outstanding performance, Redis works with an
**in-memory dataset**. Depending on your use case, you can persist it either
by [dumping the dataset to disk](/topics/persistence#snapshotting)
every once in a while, or by [appending each command to a
log](/topics/persistence#append-only-file). Persistence can be optionally
disabled, if you just need a feature-rich, networked, in-memory cache.

Redis also supports trivial-to-setup [master-slave asynchronous replication](/topics/replication), with very fast non-blocking first synchronization, auto-reconnection with partial resynchronization on net split.

Other features include:

* [Transactions](/topics/transactions)
* [Pub/Sub](/topics/pubsub)
* [Lua scripting](/commands/eval)
* [Keys with a limited time-to-live](/commands/expire)
* [LRU eviction of keys](/topics/lru-cache)
* [Automatic failover](/topics/sentinel)

You can use Redis from [most programming languages](/clients) out there. 

Redis is written in **ANSI C** and works in most POSIX systems like Linux,
\*BSD, OS X without external dependencies. Linux and OSX are the two operating systems where Redis is developed and more tested, and we **recommend using Linux for deploying**. Redis may work in Solaris-derived systems like SmartOS, but the support is *best effort*. There
is no official support for Windows builds, but Microsoft develops and
maintains a [Win-64 port of Redis](https://github.com/MSOpenTech/redis).
