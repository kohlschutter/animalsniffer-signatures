# Animal Sniffer Signatures

## What

This repository provides signatures (as Maven artifacts) for the [Animal Sniffer Maven Plugin](https://www.mojohaus.org/animal-sniffer/animal-sniffer-maven-plugin/).

Currently, the following signatures are provided:

- Java 1.7
  
  ```
  <signature>
      <groupId>com.kohlschutter.animalsniffer</groupId>
      <artifactId>signatures-java-7</artifactId>
      <version>1.0.0</version>
  </signature>
  ```
  (Currently including classes from rt.jar, jsse.jar, jce.jar, alt-rt.jar)

## How

See [Checking a project against API signatures](https://www.mojohaus.org/animal-sniffer/animal-sniffer-maven-plugin/examples/checking-signatures.html) from the Animal Sniffer Maven Plugin website.

Building the signatures from scratch most likely requires setting `-Djava7.home=/path/to/java7home` with Maven.

## Why

I'm using retrolambda to convert Java 8 bytecode to run under Java 7. Since my code may inadvertently use API introduced in Java 1.8, running something like Animal Sniffer becomes mandatory.

Unfortunately, I couldn't find any other signatures for Java 1.7, so here we are.

## Who

Copyright 2023 by Christian Kohlschütter

Licensed under the Apache License, Version 2.0

