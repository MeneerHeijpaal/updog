## WORK IN PROGRESS!!

I am forking this repository and changing it to make it more suitable for my own usecases.

---

![Version 1.4](http://img.shields.io/badge/version-v1.4-green.svg)
![Python 3.8](http://img.shields.io/badge/python-3.8-blue.svg)
[![MIT License](http://img.shields.io/badge/license-MIT%20License-blue.svg)](https://github.com/sc0tfree/updog/blob/master/LICENSE)
[![sc0tfree Twitter](http://img.shields.io/twitter/url/http/shields.io.svg?style=social&label=Follow)](https://twitter.com/sc0tfree)

<p>
  <img src="https://sc0tfree.squarespace.com/s/updog.png" width=85px alt="updog"/>
</p>

Updog is a replacement for Python's `SimpleHTTPServer`. 
It allows uploading and downloading via HTTP/S, 
can use user supplied SSL certificates and use HTTP basic auth.

<p align="center">
  <img src="https://sc0tfree.squarespace.com/s/updog-screenshot.png" alt="Updog screenshot"/>
</p>

## Installation

Install:

```bash
git clone https://github.com/NVQXE23I/updog.git
```

## Usage

`python updog.py [-d DIRECTORY] [-p PORT] [--password PASSWORD] [--ssl]`

| Argument                            | Description                                      |
|-------------------------------------|--------------------------------------------------| 
| -d DIRECTORY, --directory DIRECTORY | Root directory [Default=.]                       | 
| -p PORT, --port PORT                | Port to serve [Default=9090]                     |
| --password PASSWORD                 | Use a password to access the page. (No username) |
| --ssl                               | Enable transport encryption via SSL              |
| --version                           | Show version                                     |
| -h, --help                          | Show help                                        |

## Examples

**The shortcut *https* is just the following command:**

`python updog.py --p443 --ssl`

**Serve from your current directory:**

`python updog/py`

**Serve from another directory:**

`python updog.py -d /another/directory`

**Serve from port 1234:**

`python updog.py -p 1234`

**Password protect the page:**

`python updog.py --password examplePassword123!`

*Please note*: updog uses HTTP basic authentication.
To login, you should leave the username blank and just
enter the password in the password field.

**Use an SSL connection:**

`python updog.py --ssl`

*Please note*: (If you want to use `--ssl` option, put the correct files in the **/certs** directory.
Otherwise you will get a error message.)

## Thanks

A special thank you to [Nicholas Smith](http://nixmith.com) for
designing the updog logo.
