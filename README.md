# Reactive Redis

Custom commands for Redis.

## Commands

### PUBLISHSET channel message

Posts a message to the given channel and stores it at the corresponding key.

### PUBLISHSETEX channel seconds message

Posts a message to the given channel, stores it at the corresponding key and sets an expiry in seconds.

### XMREVRANGE end start COUNT count key [key ...]

This command is exactly like XREVRANGE but allows retrieving multiple streams at the same time.

## Building

```bash
git clone https://github.com/reactivemarkets/reactive-redis.get
cd reactive-redis
cargo build --release
```

## Run

### Linux

```bash
redis-server --loadmodule ./target/release/libreactive_redis.so
```

### Mac

```bash
redis-server --loadmodule ./target/release/libreactive_redis.dylib
```

## Contributing

Refer to [CONTRIBUTING.md](./CONTRIBUTING.md)
