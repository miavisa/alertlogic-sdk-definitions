# alertlogic-sdk-definitions
Alert Logic APIs definitions

[![Build Status](https://travis-ci.com/alertlogic/alertlogic-sdk-definitions.svg?branch=master)](https://travis-ci.com/alertlogic/alertlogic-sdk-definitions)
[![PyPI version](https://badge.fury.io/py/alertlogic-sdk-definitions.svg)](https://badge.fury.io/py/alertlogic-sdk-definitions)

Repository contains static definitions of Alert Logic APIs, used for documentation generation, 
[SDK](https://github.com/alertlogic/alertlogic-sdk-python) and [CLI](https://github.com/alertlogic/alcli).

### Usage

#### Install 
`pip install alertlogic-sdk-definitions`

For the one who doesn't require python code, GitHub releases are produced 
containing an archive with OpenAPI definitions only, see
[here](https://github.com/alertlogic/alertlogic-sdk-definitions/releases)

#### Test
`python -m unittest`

#### Use

List available service definitions:
```
>>> import alsdkdefs
>>> alsdkdefs.list_services()
['aefr', 'aerta', 'aetag', 'aetuner', 'aims', 'assets_query', 'credentials', 'deployments', 'ingest', 'iris', 'policies', 'search', 'themis']
```

Get path to a service definitions paths:
```
>>> import alsdkdefs
>>> alsdkdefs.get_service_defs("aerta")
['/usr/local/lib/python3.8/site-packages/alsdkdefs/apis/aerta/aerta.v1.yaml']
```

### Development

Please submit a PR. Please note that API definitions are updated automatically and any changes to it will be overwritten, see:
[automatic update process](doc/automatic_releases.md)