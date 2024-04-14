# OnlineJudge 2.0

[![Python](https://img.shields.io/badge/python-3.8.0-blue.svg?style=flat-square)](https://www.python.org/downloads/release/python-362/)
[![Django](https://img.shields.io/badge/django-3.2.9-blue.svg?style=flat-square)](https://www.djangoproject.com/)
[![Django Rest Framework](https://img.shields.io/badge/django_rest_framework-3.12.0-blue.svg?style=flat-square)](http://www.django-rest-framework.org/)
[![Build Status](https://travis-ci.org/QingdaoU/OnlineJudge.svg?branch=master)](https://travis-ci.org/QingdaoU/OnlineJudge)

> #### An onlinejudge system based on Python and Vue. [Demo](https://qduoj.com)

[中文文档](README-CN.md)

## Overview

+ Based on Docker; One-click deployment
+ Separated backend and frontend; Modular programming; Micro service
+ ACM/OI rule support; realtime/non-realtime rank support
+ Amazing charting and visualization
+ Template-problem support
+ More reasonable permission control
+ Multi-language support: `C`, `C++`, `Java`, `Python2`, `Python3`
+ Markdown & MathJax support
+ Contest participants IP limit(CIDR)

Main modules are available below:

+ Backend(Django): [https://github.com/QingdaoU/OnlineJudge](https://github.com/QingdaoU/OnlineJudge)
+ Frontend(Vue): [https://github.com/QingdaoU/OnlineJudgeFE](https://github.com/QingdaoU/OnlineJudgeFE)
+ Judger Sandbox(Seccomp): [https://github.com/QingdaoU/Judger](https://github.com/QingdaoU/Judger)
+ JudgeServer(A wrapper for Judger): [https://github.com/QingdaoU/JudgeServer](https://github.com/QingdaoU/JudgeServer)

## Installation

Follow me:  [https://github.com/QingdaoU/OnlineJudgeDeploy/tree/2.0](https://github.com/QingdaoU/OnlineJudgeDeploy/tree/2.0)

## Documents

[http://opensource.qduoj.com/](http://opensource.qduoj.com/)

## Browser Support

Modern browsers(chrome, firefox) and Internet Explorer 10+.

## Thanks

+ I'd appreciate a star if you find this helpful.
+ Thanks to everyone that contributes to this project.
+ Special thanks to [heb1c](https://github.com/hebicheng), who has given us a lot of suggestions.

## License

[MIT](http://opensource.org/licenses/MIT)

## INSTALL
+ use python 3.8.0
+ run command to install package python: pip install -r deploy/requirements.txt
+ please install PostgresSQL 12 and Redis lastest version: https://redis.io/docs/install/install-redis/install-redis-on-windows/
+ [Optional] please check dev-setting.py to change your username & password and port of Database to connect
+ python manage.py makemigrations
+ python manage.py migrate
+ python manage.py inituser --username=root --password=rootroot --action=create_super_admin
+ Final run commnad to start server: python manage.py runserver
+ [Optional] for run test API run command: python run_test.py {name_application_api}nvm 

# Compiler & Judger
## C ( GCC 9.4 )
- Cài đặt GCC
```
sudo apt update
sudo apt install build-essential
```
# Theo dõi queue redis
```
rq-dashboard --redis-url redis://127.0.0.1:6379/0
```