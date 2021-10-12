# Expecto partronum

How to design a magical rate limiter?


## Why we need rate limiter?

* Prevent Dos
* Reduce cost
* Prevent server from being overloaded

## Requirements
* Accurately limit excessive requests
* Low latency
* Little memory
* Distributed rate limiting
* Exception handling
* High fault toleranc

```
* Request amount
* Coupling to system?
* Notification
```

## Problems

### Where should the rate limiter be implemented?


* API gateway
* Server Side

#### Tradeoff

* Coupling to system?
* Full control of rate limit algorithms
* Using microservice already?
* Engineer resource
* Request amount?

---

### What is the rules of throttle, What is the algorithms using for rate limiting?

* Token bucket
* Leaking bucket
* Fixed window counter
* Sliding window log
* Sliding window counter

#### Tradeoff

* How hard to implement?
* Memory
* Allow burst of traffic?
* Accurate?
* Specific usecase?

---

### Where shall we store the counter?

* DB or In-Memory cache?

---

### Notification to client

#### HTTP

* If request is rate limited
    * Return `HTTP-429(too many requests)`
* HTTP headers
    * `X-Ratelimit-Remaining`: The remaining number of allow requests within the window.
    * `X-Ratelimit-Limit`: How many calls the client can make per time window.
    * `X-Ratelimit-Retry-After`: The number of second to wait until you can make a request again without being throttled.

---

### [Distributed] Race condition: How to prevent race condition?

* Redis

---

### [Distributed] Synchronization issue: How to synchronize on multi-rate-limiter service?

* sticky sessions
* centralized data stored

## Solutions

__todo__

## Algorithms details

__todo__

## Sources

https://medium.com/@saisandeepmopuri/system-design-rate-limiter-and-data-modelling-9304b0d18250
https://engineering.classdojo.com/blog/2015/02/06/rolling-rate-limiter/
