---
title: poetry项目如何配置清华pypi源？
tags: python,poetry,pypi
notebook: python
---

## 豆瓣源的问题

poetry设置douban的pypi有各种各样的问题：

1. 这个[issue](https://github.com/python-poetry/poetry/issues/1841)报告了一个豆瓣源无效的问题，原因是`https://pypi.douban.com/simple/`会redirect到
    `https://pypi.doubanio.com/simple/`，而且有反爬虫手段，返回非200状态码，导致poetry无法下载依赖
2. 在设置豆瓣源为doubanio.com域名之后，仍然有问题。一些库的最新版本在douban搜索不到，也会造成poetry流程失败。

## 替换为清华源

参考: https://mirror.tuna.tsinghua.edu.cn/help/pypi/

```yaml
[[tool.poetry.source]]
name = "tsinghua"
url = "https://pypi.tuna.tsinghua.edu.cn/simple/"
default = true
```