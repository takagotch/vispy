### vispy
---
https://github.com/vispy/vispy

```py
// vispy/conftest.py
def pytest_configure(config):
  config.addinvalue_line(
    'markers',
    'vispy_app_test: Test that require a valid GUI application.')
  warning_lines = """
  ignore:.*imp module.*:
  ignore:Using or importing the ABCs.*:
  """
  for warning_line in warning_lines.split('\n'):
    warning_line = warning_line.strip()
    if warning_line and not warning_line.startswith('#'):
      config.addinivalue_line('filterwarnings', warning_line)

```

```
```

```
```


