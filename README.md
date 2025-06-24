# redis-practice

# 🔥 Redis Learning Journey by Bharat Patel

Welcome to my Redis learning journey! This repository tracks my step-by-step exploration of Redis — from basics to advanced features — including real hands-on exercises and notes.

---

## 📚 Index

1. [Getting Started with Redis](#getting-started-with-redis)
2. [String Data Type](#1-redis-string-data-type)
   - [Exercises](#string-exercises)
3. [Hash Data Type](#2-redis-hash-data-type)
   - [Exercises](#hash-exercises)
4. [Upcoming Topics](#upcoming-topics)

---

## Getting Started with Redis

- 📦 Installed Redis locally via Docker
- 🧪 Used `redis-cli` for practice
- 🌐 Plan to set up a self-hosted Redis server with replication and Sentinel (coming soon!)

---

## 1. Redis String Data Type

Redis Strings are binary-safe and the simplest type in Redis. They store text, numbers, or even JSON.

### Common Commands:

```
SET key value
GET key
APPEND key value
INCR key
SET key value EX seconds
SET key value NX
```

### String Exercises

| #   | Description                     | Command                               |
| --- | ------------------------------- | ------------------------------------- |
| 1   | Store `"Redis is fun!"`         | `SET quote "Redis is fun!"`           |
| 2   | Increment `counter` by 10       | `SET counter 0` → `INCRBY counter 10` |
| 3   | Decrement `score` by 2          | `DECRBY score 2`                      |
| 4   | Append `" Patel"` to `"Bharat"` | `APPEND name " Patel"`                |
| 5   | Set expiring OTP                | `SET otp:1234 "567890" EX 60`         |
| 6   | Set `status` only if not exists | `SET status "active" NX`              |
| 7   | Update & get old value          | `GETSET last_login "2025-06-13"`      |
| 8   | Set multiple keys               | `MSET a 1 b 2 c 3`                    |
| 9   | Get multiple keys               | `MGET a b c`                          |
| 10  | Set session with expiry         | `SET session:user1 "active" EX 30`    |

---

## 2. Redis Hash Data Type

Hashes store multiple fields under one key — perfect for structured data like user profiles or product info.

### Common Commands:

```
HSET key field value
HGET key field
HGETALL key
HINCRBY key field increment
HINCRBYFLOAT key field increment
HDEL key field
```

### Hash Exercises

| #   | Description                   | Command                                                     |
| --- | ----------------------------- | ----------------------------------------------------------- |
| 1   | Create user hash              | `HSET user:1 name "Bharat" age 40 city "Ahmedabad"`         |
| 2   | Get `city` field              | `HGET user:1 city`                                          |
| 3   | Get all fields                | `HGETALL user:1`                                            |
| 4   | Increment age                 | `HINCRBY user:1 age 1`                                      |
| 5   | Float increment rating        | `HSET user:1 rating 4.5` → `HINCRBYFLOAT user:1 rating 0.3` |
| 6   | Delete field `city`           | `HDEL user:1 city`                                          |
| 7   | Check if field exists         | `HEXISTS user:1 email`                                      |
| 8   | Create product hash           | `HSET product:101 name "Smartphone" price 19999 stock 25`   |
| 9   | Update stock to 50            | `HSET product:101 stock 50`                                 |
| 10  | Get `name` and `price` fields | `HMGET product:101 name price`                              |

---

## 🧭 Upcoming Topics

- [ ] Redis Lists – FIFO Queues
- [ ] Redis Sets – Unordered Collections
- [ ] Sorted Sets – Leaderboards
- [ ] Pub/Sub and Streams
- [ ] Persistence (RDB / AOF)
- [ ] Redis Replication
- [ ] Redis Sentinel (HA)
- [ ] Redis Cluster
- [ ] Caching Patterns
- [ ] Lua Scripts and Transactions

---

## 👋 Connect with Me

I'm documenting this journey to help others and stay accountable.

- 💼 [LinkedIn](https://www.linkedin.com/in/bharatpatel/)
- 🧵 Follow the hashtag: `#BharatLearnsRedis`
- 🛠️ Ask me anything via GitHub Discussions (coming soon)

---

> ⭐ **Star** this repo if you find it useful, or fork it to start your own Redis learning journal!
