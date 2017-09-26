# POW：每次运行时间都是不一样的，因为里面有时间属性。


## const targetBits = 20 情况下：

- 时间：4.5秒，hashcash：46万次
- 时间：4.4秒，hashcash：48万次
- 时间：1.6秒，hashcash：17万次

## const targetBits = 22 情况下：

- 时间：28秒，hashcash：334万次
- 时间：19秒，hashcash：327万次
- 时间：11秒，hashcash：134万次

## const targetBits = 24 情况下：

- 时间：126秒，hashcash：1443万次
- 时间：117秒，hashcash：1285万次
- 时间：168秒，hashcash：1836万次

## const targetBits = 26 情况下：

- 时间：201秒，hashcash：2289万次
- 时间：273秒，hashcash：2941万次
- 时间：268秒，hashcash：2898万次

## const targetBits = 27 情况下：

- 时间：268秒，hashcash：3009万次
- 时间：3568秒，hashcash：38816万次
- 时间：452秒，hashcash：4918万次

## const targetBits = 28 情况下：

- 时间：1986秒，hashcash：22690万次
- 时间：681秒，hashcash：7423万次
- 时间：190秒，hashcash：2096万次


我的机器hashcash是[sha256.Sum256(data)]  2.17M/sec。
但是本程序中 nonce尝试速度为 110k/sec, 说明bigInt等操作时间过长，有优化空间。

---------------------------
全网算力 6 exahash/s。
平均要计算 6GG次哈希运算才能得到一个块

---------------------------
hash碰撞：
 30个人中有同生日的概率P(30) = 70%
 70个人中有同生日的概率P(70) = 99%
 
    16位Hash碰撞概率为50%，则n = 301次
    32位Hash碰撞概率为50%，则n = 77162次
    128位MD5碰撞概率为50%，则n = 21,719,381,355,163,562,492次 2171亿亿次

http://www.freezhongzi.info/?p=100


# Blockchain in Go

A blockchain implementation in Go, as described in these articles:

1. [Basic Prototype](https://jeiwan.cc/posts/building-blockchain-in-go-part-1/)
2. [Proof-of-Work](https://jeiwan.cc/posts/building-blockchain-in-go-part-2/)
3. [Persistence and CLI](https://jeiwan.cc/posts/building-blockchain-in-go-part-3/)
4. [Transactions 1](https://jeiwan.cc/posts/building-blockchain-in-go-part-4/)
5. [Addresses](https://jeiwan.cc/posts/building-blockchain-in-go-part-5/)
6. [Transactions 2](https://jeiwan.cc/posts/building-blockchain-in-go-part-6/)
