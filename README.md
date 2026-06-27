# Conan recipe for LuaJIT library

This is a [Conan](https://conan.io/) v2-compatible recipe for [LuaJIT](https://luajit.org/) library.

It has been forked from the [Conan Center Index recipe](https://github.com/conan-io/conan-center-index/tree/master/recipes/luajit/all) and adds the following features:
- building any upstream commit, as LuaJIT switched to a rolling release mode
- building for iOS and Android platforms

The original CCI recipe supports only an ancient LuaJIT version, you can read more about this decision in https://github.com/conan-io/conan-center-index/issues/25032

## Usage

To build the recipe, you must provide upstream commit hash as version:

    conan create --version=<commit hash> ...

As a consequence, you can't use version range with this recipe.

And then, to consume this recipe:

```
# conanfile.txt
[requires]
luajit/<commit hash>
```

```python
# conanfile.py
self.requires("luajit/<commit hash>")
```
