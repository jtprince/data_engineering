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

1. [glom](https://github.com/mahmoud/glom)

    `pip install glom`

    ```python
    from glom import glom
    glom.glom(data, 'foo.bar')  # -> "baz"
    ```


1. [JMESPath](https://github.com/jmespath/jmespath.py)

    `pip install jmespath`

    ```python
    import jmespath
    jmespath.search('foo.bar', data)  # -> "baz"

    # or compile before using, like re.compile
    expression = jmespath.compile('foo.bar')
    expression.search(data)
    ```

    [Specification](http://jmespath.org/specification.html)

1. [dpath](https://github.com/akesterson/dpath-python)

    `pip install dpath`

    ```python
    import dpath.util
    dpath.util.get(data, "foo/bar")  # -> "baz"

    # also
    dpath.util.search
    ```

1. [json-pointer](https://github.com/stefankoegl/python-json-pointer)

    Still trying to get working.


## Related

* [pycatj](https://github.com/dbarrosop/pycatj) (flattening json)
* [marshmallow](https://marshmallow.readthedocs.io/en/stable/) (object serialization)
* [jsons](https://jsons.readthedocs.io/en/latest/) (json serializing objects)
* [pandas json_normalize](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.io.json.json_normalize.html)
