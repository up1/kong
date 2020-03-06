Test helpers for Kong (integration) tests
=========================================

To generate the documentation run the following command in the `./spec` directory
of the Kong source tree:

```
# install ldoc using LuaRocks
luarocks install ldoc

# generate the docs
ldoc .
```

## Environment variables

When testing Kong will ingore the `KONG_xxx` environment variables that are
usually used to configure it. This is to make sure the tests run deterministic.
If for some reason this behaviour needs to be overridden, then the `KONG_TEST_xxx`
version of the variable can be used, that will be respected by the Kong test
instance.

To prevent the test helpers from cleaning the Kong working directory, the
variable `KONG_TEST_DONT_CLEAN` can be set.
This comes in handy when inspecting then logs after the tests completed.
