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

### Where?

Where should the rate limiter be implemented?

* API gateway
* Server Side

#### Tradeoff

* Full control of rate limit algorithms
* Using microservice already?
* Engineer resource

---

### How?

The rules of throttle, What is the algorithms using for rate limiting?

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

* Different kind of rate limiter
    * client-side
    * server-side API rate limiter
* Request amount
* Coupling to system?
* Notification

### Request amount
### Coupling to system?
### Notification

## Solutions

__todo__

## Algorithms details

__todo__
