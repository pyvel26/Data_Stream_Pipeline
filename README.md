# Data Stream Pipeline

## Introduction

 We will explore what big data looks like as it flows through the ETL pipeline into PostgreSQL. We can use a data stream to test a pipeline connection to a database.  We will send gigabytes of data towards PostgreSQL to see how it's being managed.  



## Installation

Requirements

PostgreSQL - at least entry level database knowledge to create tables
PyCharm or python interpreter - basic understanding of Python 


Modules used: 

mock_api.py:

from flask import Flask, Response, stream_with_context
import time
import uuid
import random

Ingest.py:

import requests
import psycopg2
from getpass import getpass 

