# jclouds-shaded

This project provides a shaded version of apache jclouds where
both guava is relocatded from `com.google.common` to `shaded.com.google.common`
and guice is relocated from `com.google.inject` to `shaded.com.google.inject`.
This makes it possible to be used in environments wher both guava and guice
are used with different versions.

The primary use-case for this project is the [jclouds-plugin](https://github.com/jenkinsci/jclouds-plugin)
for [jenkins](https://www.jenkins.io/). The reason for it being a **separate** project and **not** a maven module,
is this bug: (https://issues.apache.org/jira/browse/MSHADE-326)

