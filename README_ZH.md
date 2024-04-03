# flask-server-template

[English](README.md) / 中文

## 简介

**flask-server-template** 是一个旨在快速搭建轻量级Web应用的框架。主要函数入口位于 `server.py` 文件中的 `server::handler` 函数，您的代码编写主要集中在这个文件中。

以下是关于如何使用这个代码库的简单指南：

### 步骤一：安装依赖

首先，通过以下命令安装项目所需的依赖：

```bash
pip install -r requirements.txt
```

### 步骤二：编写您的函数代码

在 `server.py` 文件中编写您的函数代码，例如：

```python
def handler():
    <your code>
```

### 步骤三：在后台启动Web应用

在后台启动Web应用，假设启动端口为 `8099`：

```bash
nohup gunicorn -b 127.0.0.1:8099 server:app &
```

### 步骤四：使用 curl 验证Web应用服务

使用 `curl` 命令验证Web应用服务是否正常运行：

```bash
curl --location --request POST 'http://127.0.0.1:8099'
```

在不到五分钟的时间内，您就可以搭建一个完整的Web应用了 :)
