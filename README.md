# Producer/Consumer Problem

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

This repository implements the producer/consumer problem using threads. 

## Clone Project

```bash
$ git clone git@github.com:jorgearaujo81/ProducerConsumer.git
$ cd ProducerConsumer
```

## Running

```bash
$ make
$ make run
```

## Cleaning

```bash
$ make clean
```

## Specification

1. The program receives as a parameter the number of producers (P), the number of consumers (C), a limit N, and B that represents the size of the buffer, where each producer and each consumer must be threads.

### Input

```
P C N B
```

2. The program produces data through the function f(x) = 2x + 1, where x ≥ 0 and x ≤ N. When the value of x is the same as N, the producer resets the value of x and continues execution.

3. Each time an element is added by producer 𝑌 to the buffer, the message “**Producer Y producing Z at position H**” should be displayed, where Y is the identifier of the producer, Z is the value produced and H is the position of the buffer that the element will be added.

4. Consumers need to display the message “**Consumer I consuming J from position H**”, where I is the identifier of the consumer, J is the value consumed from the buffer, and H is the position being accessed in the buffer.

5. Producers will only produce if the buffer is not full and consumers can only consume if the buffer is not empty.

6. The program will run forever.

7. The entire execution part will have a pattern similar to the pattern below:

```
Producer Y producing Z at position H
Producer Y producing Z at position H
Producer Y producing Z at position H
Consumer I consuming J from position H
Consumer I consuming J from position H
Producer Y producing Z at position H
Consumer I consuming J from position H
Consumer I consuming J from position H
.
.
.
```

The order of messages from producers and consumers is not crucial in implementation. Of course, you can't consume more times than what was produced, at any time during the execution.

8. Inputs and Outputs:

## Examples Input and output

## Input

```
3 2 1 4
```

## Output

```
Producer 0 producing 1 at position 0
Producer 2 producing 1 at position 1
Consumer 1 consuming 1 from position 0
Producer 0 producing 3 in position 2
Consumer 0 consuming 1 from position 1
Producer 1 producing 1 in position 3
Consumer 0 consuming 3 from position 2
Consumer 0 consuming 1 from position 3
Producer 1 producing 3 at position 0
Producer 2 producing 3 in position 1
Consumer 0 consuming 3 from position 0
Consumer 1 consuming 3 from position 1
.
.
.
```

## References
```
[](Atividade6.pdf)
```
