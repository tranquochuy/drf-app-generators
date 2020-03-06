# DRF Application Generators
Generate DRF standard apps with a single command.

## Installation
Install with pip

```bash
$ pip install -e git+https://github.com/tranquochuy/drf-app-generators#egg=drf-app-generators
```

To use DRF app generators, add it to INSTALLED_APPS.

```code-block:: python
INSTALLED_APPS = (
    ...
    'rest_framework',
    'drf_app_generators',
    ...
)
```

## Usage
To use the generators, run the following command.

```bash
$ python manage.py generate {app} {options}
```

| Options                 | Description                           |
|-------------------------|---------------------------------------|
|`--models`               | A list of model names.                |


Example: Generate a new app with 3 models.
```bash
    $ python manage.py generate book --models Book,Author,Label
```

```bash
    src/books/
    ├── __init__.py
    ├── admin.py
    ├── apis.py
    ├── apps.py
    ├── factories.py
    ├── filters.py
    ├── migrations
    │   ├── 0001_initial.py
    │   └── __init__.py
    ├── models.py
    ├── permissions.py
    ├── serializers.py
    └── tests
        ├── __init__.py
        ├── test_books_apis.py
        └── test_books_models.py
```

## Tests
A full application built with drf-generators can be found in the tests directory.

## License
MIT License. See [LICENSE](https://github.com/tranquochuy/drf-app-generators/blob/master/LICENSE).
