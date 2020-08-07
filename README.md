<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-http-last-modified-view.svg?maxAge=3600)](https://pypi.org/project/django-http-last-modified-view/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-http-last-modified-view.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-http-last-modified-view.py/actions)

### Installation
```bash
$ [sudo] pip install django-http-last-modified-view
```

#### Examples
`get_http_last_modified`
```python
from django_http_last_modified_view.views import HttpLastModifiedMixin

class MyView(HttpLastModifiedMixin,...):

    def get_http_last_modified(self):
        return self.obj.http_last_modified
```

`dispatch`, `self.http_last_modified`:
```python
class MyView(HttpLastModifiedMixin,...):
    def dispatch(self, *args, **kwargs):
        self.http_last_modified = obj.last_modified_at
        return super().dispatch(*args, **kwargs)
```

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>