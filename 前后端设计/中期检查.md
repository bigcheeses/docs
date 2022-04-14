# 鸽子广场

<img src="https://gitee.com/yzketx/image-markdown/raw/master/img/202203171930584.jpg" alt="ae086a458fb7d1b4574d049e5efe2e9" style="zoom:50%;" />

> 浙商大师生交流平台，聚焦浙商大新闻，提供校内小工具

## 项目背景

<img src="https://gitee.com/yzketx/image-markdown/raw/master/img/202203180951574.png" alt="image-20220318095123373" style="zoom:80%;" />

## 思维导图

<img src="https://gitee.com/yzketx/image-markdown/raw/master/img/202203081856107.png" style="zoom:50%;" />

## 模块划分

### 用户

![image-20220317193729718](https://gitee.com/yzketx/image-markdown/raw/master/img/202203171937790.png)

| 功能         | 接口 (/user^)     | 描述                     |
| ------------ | ----------------- | ------------------------ |
| 登录/登出    | /login    /logout |                          |
| 注册         | /register         |                          |
| 修改密码     | /change_password  |                          |
| 第三方登入   | /third-auth       | 待定                     |
| 修改个人信息 | /profile          |                          |
| 个人简介     | /intro            | 个人的基本信息           |
| 课程表       | /school-timetable | 保存课程表信息           |
| 浏览记录     | /history          | 个人的动态及新闻浏览记录 |

### 动态

![image-20220317200326216](https://gitee.com/yzketx/image-markdown/raw/master/img/202203172003335.png)

| 功能      | 接口 (/moment^) | 描述 |
| --------- | --------------- | ---- |
| 发布      | post方法        |      |
| 详情/简介 | get方法  /intro |      |
| 标签      | /tag            |      |
| 评论      | /comment        |      |
| 点赞      | /like           |      |
| 收藏      | /star           |      |
| 关注      | /follow         |      |
| 搜索      | /search         |      |
| 分享      | /share          |      |

### 新闻

![image-20220317203334167](https://gitee.com/yzketx/image-markdown/raw/master/img/202203172033268.png)

| 功能               | 接口 (/news^)   | 描述                 |
| ------------------ | --------------- | -------------------- |
| 点赞               | /like           |                      |
| 分享               | /share          |                      |
| 抓取新闻【纯后端】 |                 | 获取微信公众号的新闻 |
| 详情/简介          | get方法  /intro |                      |
| 评论               | /comment        |                      |

### 消息

![image-20220317201832431](https://gitee.com/yzketx/image-markdown/raw/master/img/202203172018491.png)

| 功能             | 接口                                 | 描述 |
| ---------------- | ------------------------------------ | ---- |
| （与我相关）评论 | /user/comment(待定)  /user/commented |      |
| （与我相关）点赞 | /user/like(待定)  /user/liked        |      |
| 私聊             | /message                             |      |

## 前后端框架

### 后端

==Django== ==Restful API==

①齐全的功能。自带大量常用工具和框架，可轻松、迅速开发出一一个功能齐全的Web应用。

②完善的文档。Django已发展十余年，具有广泛的实践案例，同时Django提供完善的在线文档，Django用户能够更容易地找到问题的解决方案。

③强大的数据库访问组件。Django自带一个面向对象的、反映数据模型(以Python类的形式定义)与关系型数据库间的映射关系的映射器(ORM)，开发者无须学习SQL语言即可操作数据库。

④灵活的URL映射。Django提供一个基于正则表达式的URL分发器，开发者可灵活地编写URL。

⑤丰富的模板语言。Django模板语言功能丰富，支持自定义模板标签。Django也支持使用第三方模板系统，如jinja2等 。

⑥健全的后台管理系统。Django内置了-一个后台数据管理系统，经简单配置后，再编写少量代码即可使用完整的后台管理功能。

⑦完整的错误信息提示。Django提供 了非常完整的错误信息提示和定位功能，可在开发调试过程中快速定位错误或异常。

⑧强大的缓存支持。Django内置了一个缓存框架，并提供了多种可选的缓存方式。

 ==MTV==

| 层次                        | 职责                                                         |
| --------------------------- | ------------------------------------------------------------ |
| 模型（Model），即数据存取层 | 处理与数据相关的所有事务： 如何存取、如何验证有效性、包含哪些行为以及数据之间的关系等。 |
| 模板(Template)，即表现层    | 处理与表现相关的决定： 如何在页面或其他类型文档中进行显示。  |
| 视图（View），即业务逻辑层  | 存取模型及调取恰当模板的相关逻辑。模型与模板的桥梁。         |

### 前端

==MVP==

<img src="https://gitee.com/yzketx/image-markdown/raw/master/img/202203172353278.webp" alt="img" style="zoom:50%;" />

Presenter：连接View层与Model层的桥梁并对业务逻辑进行处理。

View：视图层，在View层中只负责对数据的展示，提供友好的界面与用户进行交互。

Model：数据层。负责对数据的存取操作，例如对数据库的读写，网络的数据的请求等。

- 模型与视图完全分离，我们可以修改视图而不影响模型
- 可以更高效地使用模型，因为所有的交互都发生在一个地方——Presenter内部
- 我们可以将一个Presenter用于多个视图，而不需要改变Presenter的逻辑
- 逻辑结构更加清晰，解决Activity代码臃肿问题

[APP设计链接](https://js.design/f/Kh8vOZ?p=p4NfHwUO5n)
