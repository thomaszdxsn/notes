---
title: 使用Docker将Django项目容器化
tags: docker,django,container,devops
notebook: django
---

## checklist

我想要将django项目容器化，我的需要如下:

- 将项目打包成docker image
- 可以通过image下面的一个entrypoint，运行不同的进程，代表不同的容器。比如开启uwsgi进程，开启celery进程，或者直接执行pytest
- 希望使用poetry进行依赖管理，希望不要每次容器打包都重新下载依赖
- 希望使用外部的服务, 如redis/mysql

我不需要的:

- 不需要容器编排


## 参考链接

- [cookiecutter-django](https://github.com/pydanny/cookiecutter-django)
