# ljudge-py

[![PyPI version](https://badge.fury.io/py/ljudge.svg)](https://badge.fury.io/py/ljudge)

python bindings for [ljudge](https://github.com/quark-zju/ljudge)

## Installation

First install [ljudge](https://github.com/quark-zju/ljudge)

Install ljudge-py with pip:
```
$ pip install ljudge
```

## Usage

```python
import ljudge

opts = {
    'user-code': 'ac.c',
    'max-cpu-time': '1.0',
    'max-compiler-cpu-time': '10',
    'max-memory': '32m',
    'testcase': [
        {
            'input': '1.in',
            'output': '1.out',
        },
        {
            'input': '2.in',
            'output': '2.out',
        }
    ],
}

ljudge.run(opts)

#{u'compilation': {u'log': u'a.c: In function \'main\':\na.c:5:6: warning: ignoring return value of \'scanf\', declared with attribute warn_unused_result [-Wunused-result]\n scanf("%d%d", &a, &b);\n      ^', u'success': True}, u'testcases': [{u'time': 0.001, u'result': u'ACCEPTED', u'memory': 225280}, {u'time': 0.001, u'result': u'WRONG_ANSWER', u'memory': 225280}]}

```