# testing-openapi-generator-cli
Testing some openapi-generator-cli generator edge cases.

## ✅ No oneOf
Sample spec without using any `oneOf`.  

Generator works fine.

```
bin/test test1-no-union
```

## ❌ oneOf with a single type
Sample spec using a `oneOf` that only has one type in it.

Generator fails.

```
bin/test test2-union-with-one-type
```

## ❌ oneOf with two types
Sample spec using a `oneOf` that only has two types in it.

Generator fails.

```
bin/test test3-union-with-two-types
```

## ✅ oneOf with one type and null

Sample spec using a `oneOf` that allows one type or null.

Generator works fine.

```
bin/test test4-union-with-one-type-and-null
```
