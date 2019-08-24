### redisson
---
https://github.com/redisson/redisson

```java
Config config = new Config();
config.useClusterServers()
  .addNodeAddress("redis://127.0.0.1:7181");

config = Config.fromYAML(new File("config-file.yaml"));


RedissonClient redisson = Redisson.create(config);
RedissonReactClient redissonReactive = Redisson.createReactive(config);

RedissonRXClient redissonRx = Redisson.createRx(config);


RMap<MyKey, MyValue> map = redisson.getMap("myMap");
RMapReactive<MyKey, MyValue> mapReactive = redissonReactive.getMap("myMap");
RMapRx<MyKey, MyValue> mapRx = redissonRx.getMap("myMap");

RLock lock = redisson.getLock("myLock");
RLockReactive lockReactive = redissonReactive.getLock("myLock");
RLockRx lockRx = redissonRx.getLock("myLock");

RExecutorService executor = redisson.getExecutorService("myExecutorService");
```

```
```

```
```


