# Chapter 1. Introduction

## JVM Tuning Flags

Boolean flags use this syntax: `-XX:+FlagName` enables the flag, and `-XX:-FlagName`
disables the flag. Flags that require a parameter use this syntax: `-XX:FlagName=something`.
`-XX:PrintFlagsFinal` determines the default value for a particular flag in a
particular environment.

## The Complete Performance Story

- Write Better Algorithms

- Write Less Code

- Oh Go Ahead, Prematurely Optimize

  Avoid code constructs that are known to be bad for performance

  ```java
  log.log(Level.FINE, "I am here, and the value of X is "
          + calcX() + " and Y is " + calcY());

  // better
  if (log.isLoggable(Level.FINE)) {
      log.log(Level.FINE,
              "I am here, and the value of X is {} and Y is {}",
              new Object[]{calcX(), calcY()});
  }
  ```

- Look Elsewhere: The Database is Always the Bottleneck

- Optimize for the Common Case