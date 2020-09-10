# Redis Interview Questions

### Content

- Redis Fundamentals
  - [Introduction to Redis](#Introduction to Redis)
    - [x] [Q: What is Redis?](#Q: What is Redis?)
    - [x] [Q: What is the meaning of Redis?](#Q: What is the meaning of Redis?)
    - [x] [Q: In which language Redis is written?](#Q: In which language Redis is written?)
    - [x] [Q: What are the main features of Redis?](#Q: What are the main features of Redis?)
    - [x] [Q: What are the advantages of using Redis?](#Q: What are the advantages of using Redis?)
    - [x] [Q: What are the limitations of Redis?](#Q: What are the limitations of Redis?)
    - [x] [Q: How is Redis different from other databases?](#Q: How is Redis different from other databases?)
    - [x] [Q: What is the difference between Redis and RDBMS?](#Q: What is the difference between Redis and RDBMS?)
    - [x] [Q: What is the difference between Memcached and Redis?](#Q: What is the difference between Memcached and Redis?)
    - [x] [Q: What is the usage of Redis?](#Q: What is the usage of Redis?)
  - [Basics](#Basics) (Database, commands/key/value, Querying, Memory and persistence)
    - [x] [Q: How to interect with Redis?](#Q: How to interect with Redis?)
    - [x] [Q: Which are the most popular commands of the Redis database?](#Q: Which are the most popular commands of the Redis database?)
    - [x] [Q: List out the operation keys of Redis?](#Q: List out the operation keys of Redis?)
    - [x] [Q: Mention what are the things you have to take care while using Redis?](#Q: Mention what are the things you have to take care while using Redis?)
    - [x] [Q: Does Redis give speed and durability both?](#Q: Does Redis give speed and durability both?)
    - [x] [Q: How can you improve the durability in Redis?](#Q: How can you improve the durability in Redis?)
  - [Data Structures](#Data Structures) (Strings, Hashes, Lists, Sets, Sorted Sets)
    - [x] [Q: Which are the different data types used in Redis?](#Q: Which are the different data types used in Redis?)
  - [Leveraging Data Structures](#Leveraging Data Structures) (Multi key queries, references and indexes, transactions, keys anti-pattern)
  - [Beyond Data Structure](#Beyond Data Structure) (Expiration, Publication and subscription, monitor, sort)
  - [Administration](#Administration) (Configuration, Authentication, Replication, Backups, Cluster)
    - [x] [Q: Explain the Replication feature of Redis?](#Q: Explain the Replication feature of Redis?)
- Redis Cluster Schema
-  Distributed locks with Redis
- [Redis Cache Problems](#Redis Cache Problems) (Penetration 穿透, Breakdown 击穿, Avalanche 雪崩, Preheating 预热, Degrading 降级，Hotspot Key 热点key)
  - [x] [Q: What is Cache Penetration? How to solve it?](#Q: What is Cache Penetration? How to solve it?)
  - [x] [Q: What is Cache Breakdown? How to solve it?](#Q: What is Cache Breakdown? How to solve it?)
  - [x] [Q: What is Cache Avalanche? How to solve it?](#Q: What is Cache Avalanche? How to solve it?)
  - [x] [Q: What is Cache Concurrent?](#Q: What is Cache Concurrent?)
  - [x] [Q: What is Cache Preheating?](#Q: What is Cache Preheating?)
  - [x] [Q: Redis Hotspot Key Discovery and Common Solutions?](#Q: Redis Hotspot Key Discovery and Common Solutions?)

## Introduction to Redis

### Q: What is Redis?

Redis is an advanced key-value data store and cache. It has is also referred to as a data structure server as such the keys not only contains strings, but also hashes, sets, lists, and sorted sets. Companies using Redis includes StackOverflow, Twitter, Github, etc.

### Q: What is the meaning of Redis?

Redis stands for REmote DIctionary Server.

### Q: In which language Redis is written?

Redis is written in ANSI C and mostly used for cache solution and session management. It creates unique keys for store values.

### Q: What are the main features of Redis?

Following are the main features of Redis:

- Redis is very simple to install setup and manage.
- Redis is very fast. It can execute 100000 queries per second.
- Redis is fast because data is being persistent in memory as well as stored on the disk.
- Redis is very fast because it loads the whole dataset in primary memory.
- Redis operations working on different data types are atomic so these operations can be accomplished safely i.e. to set or increase a key, add or remove elements from a set or increase a counter.
- It supports various types of data structure such as strings, hashes, sets, lists, sorted sets etc.
- Redis supports a variety of languages i.e. C, C++, C#, Ruby, Python, Twisted Python, PHP, Erlang, Tcl, Perl, Lua, Java, Scala etc.
- If your favorite language is not supported yet, you can write your own client library, as the Protocol is pretty simple.
- Redis supports simple master to slave replication.
- Redis is portable.

### Q: What are the advantages of using Redis?

Advantage of using Redis are

- It provides high speed
- It supports a server-side locking
- It has got lots of client library.
- It has got command level Atomic Operation (tx operation)

### Q: What are the limitations of Redis?

- It is single threaded
- It has got limited client support for consistent hashing
- It has significant overhead for persistence
- It is not deployed widely

### Q: How is Redis different from other databases?

Redis is a NoSQL, Opensource, in-memory data-structure store. It follows the principle of key-value store.

It is extremely fast, persistent, portable and supports many languages such as C, C++, C#, Clojure, Common Lisp, D, Dart, Erlang, Go, Haskell, Haxe, Io, Java, JavaScript (Node.js), Julia, Lua, Objective-C, Perl, PHP, Pure Data, Python, R, Racket, Ruby, Rust, Scala, Smalltalk and Tcl.

### Q: What is the difference between Redis and RDBMS?

There are a lot of differences between Redis and RDBMS:

- Redis is a NoSQL database while RDBMS is an SQL database.
- Redis follows the key-value structure while RDBMS follows the table structure.
- Redis extremely fast while RDBMS is comparatively slow.
- Redis stores all the dataset in primary memory while RDBMS stores its dataset in secondary memory.
- Redis is generally used to store small and frequently used files while RDBMS is used to store big files.
- Redis provides only official support for Linux, BSD, Mac OS X, Solaris. It doesn?t provide official support for Windows currently while RDBMS provides support for both.

### Q: What is the difference between Memcached and Redis?

| Redis                                                        | Memcached                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Redis also does cache information but has got additional features like persistence and replication | Memcached only cache information.                            |
| Redis does not support the functionality of LRU (least recently used) eviction of values | Memcached supports the functionality of LRU (least recently used) eviction of values |
| In Redis you can set a time out on everything when memory is full, it will look at three random keys and deletes the one which is closest to expiry | In Memcached when they overflow memory, the one you have not used recently (LRU- least recently used) will get deleted |
| Redis does not support CAS ( Check and Set). It is useful for maintaining cache consistency | Memcached supports CAS (Check and Set)                       |
| Redis has got stronger data structures; it can handle strings, binary safe strings, list of binary safe strings, sorted lists, etc. | In Memcached, you have to serialize the objects or arrays in order to save them and to read them back you have to un-serialize them. |
| Redis had a maximum of 2GB key length                        | Memcached had a maximum of 250 bytes length                  |
| Redis is single threaded                                     | Memcached is a multi-threaded                                |



### Q: What is the usage of Redis?

Redis is a special key-value store database that can function as a NoSQL database or as a memory-cache store to improve performance when serving data that is stored in system memory.

## Basics

### Q: How to interect with Redis?

After the installation of the server you can run the Redis Client provided by redis installation or you can open the command prompt and use the following command:

```shell
redis-cli
```

By using any of them, you can interect with Redis.

### Q: Which are the most popular commands of the Redis database?

**Accessing Redis**

to connect to Redis

```
$ redis-cli
```

**Server Statistics**

The statistics command is "INFO" and will give you an output as following:

```
$ redis-cli INFO
redis_version:2.2.12
redis_git_sha1:00000000
redis_git_dirty:0
arch_bits:64
multiplexing_api:epoll
process_id:8353
uptime_in_seconds:2592232
uptime_in_days:30
...
```

**Dropping Databases**

To drop the currently selected database run

```
FLUSHDB
```

to drop all databases at once run

```
FLUSHALL
```

### Checking for Keys

If you want to know if an instance has a key or keys matching some pattern use "KEYS" instead of "GET" to get an overview.

```
redis 127.0.0.1:6379> KEYS test*
1) "testkey2"
2) "testkey3"
3) "testkey"
```

```
setnx
```

```
expire
```



### Q: List out the operation keys of Redis?

Operation keys of Redis include

- TYPE key
- TTL key
- KEYS pattern
- EXPIRE key seconds
- EXPIREAT key timestamp
- EXISTS key
- DEL key

### Q: Mention what are the things you have to take care while using Redis?

While using Redis one must take care of

- Select a consistent method to name and prefix your keys. Manage your namespace
- Create a “Registry” of key prefixes that maps each of your internal documents for that application which “own” them
- For every class you put through into your Redis infrastructure: design, implement and test the mechanisms for garbage collection or data migration to archival storage
- Design, implement and test a sharding library before you have invested much into your application deployment and make sure that you keep a registry of “shards “replicated on each server
- Separate all your K/V store and related operations into your own library/API or service

Other Answers

- Consistent method selection in order to name and prefix the keys. Namespace management.
- Make key prefixes registry which can map every documents to their owner applications.
- Designing, implementing and testing the Garbage collection mechanism for each class we keep into the redis architecture.
- Maintain a sharding library before investing so much into the application.

### Q: Does Redis give speed and durability both?

No, Redis purposely compromises the durability to enhance the speed. In Redis, in the event of system failure or crash, Redis writes to disk but may fall behind and lose the data which is not stored.

### Q: How can you improve the durability in Redis?

To improve the durability of Redis **“append only file”** can be configured by using fsync data on disk.

- Fsync () every time a new command is added to the append log file: It is safe but very slow
- Fysnc() one time every second: It is fast, but you may lose 1 second of data if system fails
- Never fsync(): It is an unsafe method, and your data is in hand of Operating System

## Data Structures

### Q: Which are the different data types used in Redis?

There are mainly 5 types of data types supported by Redis:

- Strings
- Hashes
- Lists
- Sets
- Sorted Sets

## Leveraging Data Structures

## Beyond Data Structure

## Administration

### Q: Explain the Replication feature of Redis? 

Redis supports simple master to slave replication. When a relationship is established, data from the master is transferred to the slave. Once this is done, all changes to the master replicate to the slave.

Other Answers

Replication is important in order to archive high level of availability in big data systems. The data needs to be replicated at n number of places. This follows the master-slave approach where the master copy is maintained by master-slave and replicated to n other nodes.



## Redis Cache Problems

### Q: What is Cache Penetration? How to solve it?

**Cache Penetration**

Cache penetration is a scenario where **the data to be searched doesn't exist at DB and the returned empty result set is not cached** as well and hence **every search for the key will hit the DB eventually**. If a hacker tries to initiate some attack by launching lots of searches with such key, the underlying DB layer will be hit too often and may eventually be brought down.

**Solutions**

In such cases, there are a few mitigation plans.

1. If there is no data for the key in DB, just return an empty result and cache it for a short period of time(Don't set a long expiration time)
2. Using Bloom filter. [Bloom filter](https://en.wikipedia.org/wiki/Bloom_filter) is similar to hbase set which can be used to check whether a key exists in the data set. If the key exists, go to the cache layer or DB layer, if it doesn't exists in the data set, then just return.

If the searched key has high repeat rate, then can adopt the first solution. Otherwise if the searched key has low repeat rate and the searched keys are too many, can adopt the second solution to filter most of them first.

### Q: What is Cache Breakdown? How to solve it?

**Cache Breakdown**

Cache breakdown is a scenario where the cached data expires and **at the same time there are lots of search on the expired data** which suddenly cause the searches to hit DB directly and increase the load to the DB layer dramatically.

**Solutions**

This would happen in high concurrency environment. 

1. Normally in this case, there needs to be **a lock on the searched key** so that other threads need to wait when some thread is trying to search the key and update the cache. After the cache is updated and lock is released, other threads will be able to read the newly cached data.
2. Another feasible method is to **asynchronously update the cached data through a worker thread** so that the hot data will never expire.

### Q: What is Cache Avalanche? How to solve it?

**Cache Avalanche**

Cache avalanche is a scenario where **lots of cached data expire at the same time** or **the cache service is down and all of a sudden**, so **all searches of these data will hit DB and cause high load to the DB layer** and impact the performance.

**Solutions**

To mitigate the problem, some methods can be adopted.

1. **Using clusters** to ensure that some cache server instance is in service at any point of time. If Redis is used, can have redis clusters.
2. Some other approaches like **hystrix circuit breaker and rate limit** can be configured so that the underlying system can still serve traffic and avoid high load.
3. Can **adjust the expiration time for different keys** (use prime numbers as expiration time) so that they will not expire at the same time.

All the mitigation methods need to be implemented based on real use cases and system design requirements.

### Q: What is Cache Concurrent?

Concurrency here refers to the concurrency problem caused by multiple Redis clients setting keys at the same time. In fact, Redis itself is a single-threaded operation, multiple clients operate concurrently, according to the principle of first-come-first-execute, first-come-first-execute, the rest of the blocking.

Another solution, of course, is to serialize Redis. set operations in a queue, one by one.

### Q: What is Cache Preheating?

Cache preheating is to load the relevant cached data directly into the cached system after the system is online.
This can avoid the problem of querying the database first and then caching the data when the user requests it! Users directly query the pre-heated cached data!

**Solutions:**

1. Write a cache refresh page directly and operate it manually when online.
2. The amount of data is not large, so it can be loaded automatically when the project starts. The purpose is to load the data into the cache before the system goes online.

### Q: Redis Hotspot Key Discovery and Common Solutions?

 For Redis, frequent access of the same key in a partition is known as a hotspot key. 

 Causes of hotkey problems

- The size of user consumption data is much greater than that of production data, as in the cases of hot sale items, hot news, hot issue comments, and celebrity broadcasts.

  Hotkey problems tend to occur unexpectedly, for example, the sales price promotion of popular commodities during Double 11 Shopping Festival. When one of these commodities is browsed or purchased tens of thousands of times, a large number of requests occur, which causes a hotkey problem. Similarly, hotkey problems tend to occur in scenarios where there are more writes than reads. For example, hot news, hot issue comments, and celebrity broadcasts.

- In these cases, the hotkey access is much higher than the access of other Redis keys. Therefore, most of the access traffic is centralized to a specific Redis instance, and the Redis instance may reach a performance bottleneck.

  When a piece of data is accessed on the server, the data is usually split or sliced. During this process, the corresponding key is accessed on the server. When the access traffic exceeds the performance threshold of the server, the hotkey key problem occurs.

Impact of hotkey problems

- The traffic is concentrated and reaches the upper limit of the physical network adapter.
- Too many requests queue up, crashing the sharding service of the cache.
- The database is overloaded. A service avalanche occurs.

**Common solutions**

1. Server cache solution

The client sends requests to the server. The server is a multi-thread service, and a local cache space based on the cache LRU policy is available. When the server is congested, it directly repatriates the requests rather than forwarding them to the database. Only after the congestion is cleared can the server send the requests from the client to the database and re-write the data to the cache. By using this solution, the cache is accessed and rebuilt.

However, this solution has the following problems:

- Cache building problem of the multi-thread service when the cache fails
- Cache building problem when the cache is missing
- Dirty reading problem

2. "MemCache + Redis" solution

In this solution, a separate cache is deployed on the client to resolve the hotkey problem. The client first accesses the service layer and then the cache layer of the same server. This solution has the following advantages: nearby access, high speeds, and no bandwidth limit. However, it has the following disadvantages:

- Wasted memory resources
- Dirty reading problem

3. Local cache solution

Using the local cache incurs the following problems:

- Hotspots must be detected in advance.
- The cache capacity is limited.
- The inconsistency duration is long.
- The omission of hotkeys.

If traditional hotkey solutions are all defective, how can the hotkey problems be resolved?

**ApsaraDB for Redis solution for hotkey problems**

4. Read/write splitting solution

The following describes the functions of different nodes in the architecture:

- Load balancing is implemented at the SLB layer.
- Read/write splitting and automatic routing are implemented at the proxy layer.
- Write requests are processed by the master node.
- Read requests are processed by the read-only node.
- High availability (HA) is implemented on the replica node and the master node.

In practice, the client sends requests to SLB, and SLB distributes these requests to multiple proxies. The proxies identify and classify the requests and distribute them. For example, a proxy sends all write requests to the master node and all read requests to the read-only node. But the read-only node in the module can be expanded to solve the problem of hotkey reading. Read/write splitting supports flexible scaling for hotkey reading and can store a large number of hotkeys. It is client-friendly.

5. Hotspot data solution

In this solution, hotkeys are discovered and stored to resolve the hotkey problem. The client accesses SLB and distributes requests to a proxy through SLB. Then, the proxy forwards the requests to the background Redis by the means of routing.

A cache is added on the server. Specifically, a local cache is added to the proxy. This cache uses the LRU algorithm to cache hotspot data. A hotspot data calculation module is added to the background database node to return the hotspot data.

The proxy architecture has the following benefits:

- The proxy caches the hotspot data locally, and its reading capability is horizontally scalable.
- The database node regularly calculates the hotspot data set.
- The database feeds the hotspot data back to the proxy.
- The proxy architecture is completely transparent to the client, and no compatibility is required.

**Process hotkeys**

1. Read hotspot data

The processing of hotkeys is divided into two jobs: writing and reading. During the data writing process, SLB receives data K1 and writes it to a Redis database through a proxy. If K1 becomes a hotkey after the calculation conducted by the background hotspot module, the proxy caches the hotspot. In this way, the client can directly access K1 the next time, without using Redis. The proxy can be horizontally expanded, so the accessibility of the hotspot data can be enhanced infinitely.

2. Discover hotspot data

The database first counts the requests that occur in a cycle. When the number of requests reaches the threshold, the database locates the hotkeys and stores them in an LRU list. When a client attempts to access data by sending a request to the proxy, Redis enters the feedback phase and marks the data if it finds that the target access point is a hotspot.

The database uses the following methods to calculate the hotspots:

- Hotspot statistics based on statistical thresholds.
- Hotspot statistics based on the statistical cycle.
- Statistics collection method based on the version number without resetting the initial value.
- Calculating hotspots on the database has little impact on the performance and only occupies a small amount of memory.

**Comparison of two solutions**

The preceding analysis shows that compared with the traditional solutions, Alibaba Cloud has made significant improvements in resolving the hotkey problem. The read/write splitting solution and the hotspot data solution can be expanded horizontally. These two solutions are transparent to the client, though they cannot ensure complete data consistency. The read/write splitting solution supports storing a larger amount of hotspot data, while the proxy-based hotspot data solution is more cost-effective.


## References

[1] [Top 10 Redis Interview Questions & Answers](https://career.guru99.com/top-10-redis-interview-questions/)

[2] [Redis Interview Questions](https://www.javatpoint.com/redis-interview-questions-and-answers)

Redis Cache Problems

- [What is cache penetration, cache breakdown and cache avalanche?](https://www.pixelstech.net/article/1586522853-What-is-cache-penetration-cache-breakdown-and-cache-avalanche)
- [How to Solve the Five Difficulties of Redis Avalanche, Penetration and Concurrent](http://appdianping.com/2019/03/27/how-to-solve-the-five-difficulties-of-redis-avalanche-penetration-and-concurrent/)
- [Redis Hotspot Key Discovery and Common Solutions](https://dzone.com/articles/redis-hotspot-key-discovery-and-common-solutions)