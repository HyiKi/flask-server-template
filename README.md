# flask-server-template

English / [中文](README_ZH.md)

## Introduction

**flask-server-template** is a framework designed for quickly setting up lightweight web applications. The main entry point is the `server::handler` function in the `server.py` file. Your code development primarily focuses on this file.

Below is a simple guide on how to use this repository:

### Step 1: Install Dependencies

To get started, install the project dependencies by running the following command:

```bash
pip install -r requirements.txt
```

### Step 2: Write Your Function Code in `server.py`

In the `server.py` file, write your function code. For example:

```python
def handler():
    <your code>
```

### Step 3: Start the Web Application in the Background

Start the web application in the background, assuming the startup port is `8099`:

```bash
nohup gunicorn -b 127.0.0.1:8099 server:app &
```

### Step 4: Verify the Web Application Service with curl

Use the `curl` command to verify if the web application service is running correctly:

```bash
curl --location --request POST 'http://127.0.0.1:8099'
```

In less than five minutes, you will have a fully functional web application ready to go :)
