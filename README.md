# Internet Data Sources used by D-Rats

This will be one or more configuration files for the
external data sources used by D-Rats.

Sometimes the data sources used by D-Rats need to be updated
after D-Rats has been installed.

It is also useful to have this documented.

Generally when a program is configured to use an external
third party data source, there may be a requirement to show
some attribution as to the source.

This file is maintained in [YAML](https://yaml.org/spec/) format.

Advanced maintainers can copy the tests/pre-commit script to inside the
.git/hooks directory which if the proper tools are installed, will test
the format of the files in a git commit action.  This requires shellcheck,
yamllint, and codespell to be installed.

Possible format:

```yaml
---
  datasources:
    - datatype: name
      - source: name of source
        url: https://source.example.com
        notice: |
          Notice required for data use
        password: false
```
