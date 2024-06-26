# `package:jnigen` Example

A sample command-line application that interops with Java code
using [`package:jnigen`](https://pub.dev/packages/jnigen),
with an entrypoint in `bin/` and library code in `lib/`.

## Regenerate Bindings

To generate bindings, run:

```terminal
dart run jnigen --config jnigen.yaml
```

## Run example

The dynamic libraries must be built, and the java source must be compiled before
running the example. 

```terminal
dart run jni:setup
javac java/dev/dart/Example.java
```

Now you can test the code:

```terminal
dart run jnigen_example:sum 17 25
```

Outputs:

```
42
```
