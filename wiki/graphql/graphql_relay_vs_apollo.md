---
title: Relay Vs. Apollo
tags: graphql,relay,apollo
notebook: graphql
---

 -- | Relay | Apollo
 :-: | :-: | :-:
 由谁维护 | Facebook | Meteor
 技术栈 | 只有React/React Native可以使用，必须配置babel | 不限制框架和平台（可以适用于任意的前端框架和移动native平台）
 GraphQL API | 要求编写特定结构的GraphQL Schema | 可以使用任意的GraphQL Schema
 复杂度 | 学习曲线陡峭: 在黑盒下面有很多黑魔法 | 低门槛: 可以让你快速开始编写代码，一些特性需要自己手动编写，比如分页，筛选
 弹性 | 几乎没有弹性，对于React组建和Relay的集成有严格的约束 | 极富弹性，可以渐进地为整个项目替换为apollo，比如可以保持一部分query继续使用REST
 Fragment的使用情况 | 非常依赖fragment，是每个组建表达需要数据的主要方式 | Apollo中的fragment只是一个可选工具，使用的话会很便利，不使用也没什么
 GraphQL Subscription | 支持 | 支持
 适宜场景 | 大型的，复杂的，长期的项目 | 中小型应用

