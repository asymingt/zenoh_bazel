# Zenoh build with bazel

Checkout code:

```
git clone https://github.com/asymingt/zenoh_bazel
```

Make sure you have initialized the two submodules:

```
git submodule update --init --recursive
```

Run a Zenoh-C example:

```
bazel run //:z_pub_c
```

Run a Zenoh-C++ example:

```
bazel run //:z_pub_cpp
```

Run the unit tests for the two modules.

```
bazel test @zenoh_c//...
bazel test @zenoh_cpp//...
```

# Things that don't work yet

- Zenoh-C/C++ tests: the ones that don't pass upstream are disabled.
- Zenoh-C features: shared memory and unstable features don't work yet.