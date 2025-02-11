![Build Status](https://github.com/felfert/jclouds-shaded/actions/workflows/ci.yml/badge.svg)
![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://stand-with-ukraine.pp.ua)
# jclouds-shaded

This project provides a shaded version of apache jclouds where
both guava is relocatded from `com.google.common` to `shaded.com.google.common`
and guice is relocated from `com.google.inject` to `shaded.com.google.inject`.
Since v2.7.0, `com.google.errorprone` is relocated to `shaded.com.google.errorprone` as well.
This makes it possible to be used in environments where guava, guice and errorprone
are used with different versions.

The primary use-case for this project is the [jclouds-plugin](https://github.com/jenkinsci/jclouds-plugin)
for [jenkins](https://www.jenkins.io/). The reason for it being a **separate** project and **not** a maven module,
is this bug: (https://issues.apache.org/jira/browse/MSHADE-326)

To use this project in your maven project, create the following dependency in your pom.xml:
```
<dependency>
    <groupId>com.github.felfert</groupId>
    <artifactId>jclouds-shaded</artifactId>
    <version>2.7.0</version>
</dependency>
```
