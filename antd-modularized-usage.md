---
title: antd 配置按需加载
tags: antd,es6,tree-shake
notebook: dev
---

## 歧义

[官方文档](https://ant.design/docs/react/introduce-cn#%E6%8C%89%E9%9C%80%E5%8A%A0%E8%BD%BD)有歧义，在中文文档中，这个配置的说明叫做“按需加载”，在英文文档中，叫做“Use modularzed antd (使用模块化antd)”。

## 使用babel插件

1. 保证tree-shake
2. 不需要手动引入css

```javascript
// .babelrc
{
  "plugins": [
    ["import", { "libraryName": "antd", "libraryDirectory": "es", "style": "css" }] // `style: true` for less
  ]
}
```

## 手动引入

1. 需要手动引入css
2. 示例中需要手动引入到深层的组件，全局引入组件是否有效，没有说明

```javascript
import DatePicker from 'antd/es/date-picker'; // for js
import 'antd/es/date-picker/style/css';       // for css
// import 'antd/es/date-picker/style';        // that will import less
```