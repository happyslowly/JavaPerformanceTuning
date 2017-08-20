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
with than macro benchmarks. Meso benchmarks are also good for automated testing, particularly at the module
level.
