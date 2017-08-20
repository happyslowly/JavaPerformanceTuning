# Chapter 2. An Approach to Performance Testing

## Test a real application

### Micro Benchmarks

A micro benchmark is a test designed to measure a very small unit of performance.

#### Micro benchmarks must use their results

#### Micro benchmarks must not include extraneous operations

In a micro benchmark, the input values must be pre-calculated.

#### Micro benchmarks must measure the correct input

### Macro benchmarks

The best thing to use to measure performance of an application is the application
itself, in conjunction with any external resources it uses.

### Meso benchmarks

Meso benchmarks have fewer pitfalls than micro benchmarks and are easier to work
with than macro benchmarks. Meso benchmarks are also good for automated testing, 
particularly at the module level.

## Understand Throughput, Batching, and Response Time

### Elapsed Time (Batch) Measurements

The simplest way of measuring performance is to see how long it takes to accomplish
a certain task.

In the Java world, there is one wrinkle to this: *just-in-time compilation*. Essentially
it means that it takes a few minutes (or longer) for the code to be fully optimized 
and operate at peak performance. For that (and other) reasons, performance studies
of Java are quite concerned about warm-up periods. On the other hand, in many
cases the performance of the application from start to finish is what matters.

### Throughput Measurements

A throughput measurement is based on the amount of work that can be accomplished
in a certain period of time.

In a client-server test, a throughput measurement means that clients have no think
time. The measurement is frequently referred to as:
- transactions per second (TPS)
- requests per second (RPS)
- operations per second (OPS)

### Response Time Tests

The length of time it takes between sending a request from a client until the
response is received.

The difference between a response time and a throughput test is that client
threads in a response-time test sleep for some period of time between operations.
This time is referred to as think time.

There are two ways of measuring response time.
- reported as an average
- reported as a percentile

One difference between the two numbers is in the way outliers affect the calculation
of the average. Outliers can more easily occur in Java applications because of
the pause times introduced by garbage collection.

## Understand Variability

TODO

## Test Early, Test Often

- Automate everything
- Measure everything
- Run on the target system
