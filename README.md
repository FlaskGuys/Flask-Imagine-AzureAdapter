Flask-Imagine-AzureAdapter
============

[![Author](https://img.shields.io/badge/author-Kronas-blue.svg)](https://github.com/kronas)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/kronas/Flask-Imagine/master/LICENSE)
[![Documentation Status](https://readthedocs.org/projects/flask-imagine/badge/?version=latest)](http://flask-imagine.readthedocs.org/en/latest/?badge=latest)

Microsoft Azure BLOB storage adapter for [Flask-Imagine](https://github.com/FlaskGuys/Flask-Imagine) extension.

Installation
------
```
$ pip install Flask-Imagine-AzureAdapter
```

Configuration example
------
```
from flask import Flask
from flask.ext.imagine import Imagine
from flask.ext.imagine_azure_adapter import FlaskImagineAzureAdapter

app = Flask(__name__)

app.config['IMAGINE_ADAPTERS'] = {
    'azure': FlaskImagineAzureAdapter
}

app.config['IMAGINE_ADAPTER'] = {
    'name': 'azure',
    'account_name': 'your_account_name',
    'account_key': 'your_account_key',
    'container_name': 'your_container_name',
    'domain': 'domain.tld'      # Domain name for using static website hosting
    'schema': 'https'
}

# ... Another configuration options

# Init extension
imagine = Imagine(app)
#  or 
imagine = Imagine()
imagine.init_app(app)
```
