---
title: "Functional Interfaces in Java"
date: 2021-06-29T22:36:45+02:00
draft: false
---

Since Java 8, an interface with a single method is considered a functional interface and they can be implemented as lambdas.

{{< highlight java >}}
// Interface
@FunctionalInterface
public interface FeatureFlagService {
    Boolean isEnabled(String key);
}

// Implementation
FeatureFlagService flagService = key -> true;
{{< / highlight >}}

You may notice how the interfaces is marked with the `@FunctionalInterface` annotation. This is just to help other developers to understand this is clearly a functional interface, and it's supposed to have only one single method.

---

More information:
- [Oracle @FunctionalInterface Documentation](https://docs.oracle.com/javase/8/docs/api/java/lang/FunctionalInterface.html)
- [Baeldung Functional Interfaces](https://www.baeldung.com/java-8-functional-interfaces)