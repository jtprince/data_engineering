---
title: "Python Dict Traversal"
date: 2019-11-07T12:17:00-07:00
draft: true
---

Traversing nested dict and list data structures in python.

```python
data = {
    'foo': {
        'bar': 'baz'
    }
}
```

Github projects sorted by most stars.

1. [glom](https://github.com/mahmoud/glom) (1068★)

    `pip install glom`

    ```python
    from glom import glom
    glom.glom(data, 'foo.bar')  # -> "baz"
    ```

1. [JMESPath](https://github.com/jmespath/jmespath.py) (884★)

    `pip install jmespath`

    ```python
    import jmespath
    jmespath.search('foo.bar', data)  # -> "baz"

    # or compile before using, like re.compile
    expression = jmespath.compile('foo.bar')
    expression.search(data)
    ```

    [Specification](http://jmespath.org/specification.html)

1. [jsonpath-rw](https://github.com/kennknowles/python-jsonpath-rw) (421★)

    `pip install jsonpath-rw`

1. [dpath](https://github.com/akesterson/dpath-python) (324★)

    `pip install dpath`

    ```python
    import dpath.util
    dpath.util.get(data, "foo/bar")  # -> "baz"

    # also
    dpath.util.search
    ```

1. [json-pointer](https://github.com/stefankoegl/python-json-pointer) (76★)

    Uses [RFC 6901](http://tools.ietf.org/html/rfc6901) for pointer syntax.

    `pip install jsonpointer`

    ```python
    from jsonpointer import resolve_pointer
    resolve_pointer(data, '/foo/bar')  # -> "baz"
    ```

1. [dictquery](https://github.com/cyberlis/dictquery) (45★)

    SQL like syntax.

    `pip install dictquery`


## Related

* [pycatj](https://github.com/dbarrosop/pycatj) (flattening json)
* [marshmallow](https://marshmallow.readthedocs.io/en/stable/) (object serialization)
* [pythonQL](https://github.com/pythonql/pythonql) (sql like query language)
* [Dee](https://www.quicksort.co.uk/DeeDoc.html) (sql like query language)
* [jsons](https://jsons.readthedocs.io/en/latest/) (json serializing objects)
* [pandas json_normalize](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.io.json.json_normalize.html)
