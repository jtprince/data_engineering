---
title: "Python Dict Traversal"
date: 2019-11-07T12:17:00-07:00
draft: true
---

Many tools exist for working with json, but it seems ideal to find solutions
that work with arbitrarily nested dicts and lists in python itself.

```
data = {
    'foo': {
        'bar': 'baz'
    }
}
```

1. [JMESPath](https://github.com/jmespath/jmespath.py)

    `pip install jmespath`

    ```python
    import jmespath
    jmespath.search('foo.bar', data)

    # or compile before using, like re.compile
    expression = jmespath.compile('foo.bar')
    expression.search(data)
    ```

    [Specification](http://jmespath.org/specification.html)

1. [json-pointer](https://github.com/stefankoegl/python-json-pointer)

    `pip install json-pointer`

    ```python
    from jsonpointer import resolve_pointer



    ```
