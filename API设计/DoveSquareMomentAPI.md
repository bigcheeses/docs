# 鸽子广场API设计 V1.0

## 动态模块
| 接口URL | 请求方式 | 说明 |
| ------- | -------- | ---- |
| /api/v1/moment | POST |用户发布动态|
| /api/v1/moment/recommendation |  GET |获取头条推荐 |
| /api/v1/moment/top | GET  |  获取热榜动态|
| /api/v1/moment/like | GET  |  给动态点赞/取消点赞 |
| /api/v1/moment/history |  GET |  获取用户浏览历史 |
| /api/v1/moment/search | GET  |通过关键字或直接获取动态 |
| /api/v1/moment/follow| GET  |  获取关注博主发布的动态 |
| /api/v1/moment/updatefollow |  GET |  更新用户互相关注状态 |
| /api/v1/moment/updatelike | GET  |  更新用户对动态的赞状态|
| /api/v1/moment/one|  GET |  根据id获取动态 |
| /api/v1/moment/uploadoneimage |  POST |   上传一张动态图片|
| /api/v1/moment/publish |  POST |用户发布动态（图片已上传）|
| /api/v1/moment/myall| GET  |  获得用户发布的所有动态 |
| /api/v1/moment/delete |  GET |  删除用户动态 |


## 用户模块

| 接口URL                | 请求方式 | 说明              |
| ---------------------- | -------- | ----------------- |
| /api/v1/login/wechat   | POST     | 用户登入          |
| /api/v1/logout/wechat  | POST     | 用户登出          |
| /api/v1/user/profile   | GET      | 获取个人详细信息  |
| /api/v1/user/profile   | PUT      | 修改个人信息      |
| /api/v1/user           | GET      | 获取用户列表      |
| /api/v1/user/following | POST     | 关注用户          |
| /api/v1/user/following | DELETE   | 取关用户          |
| /api/v1/oauth/wechat/  | POST     | 微信用户token认证 |
| /api/v1/user/avatar    | POST     | 用户头像上传      |



## 评论模块

| 接口URL                   | 请求方式 | 说明               |
| ------------------------- | -------- | ------------------ |
| /api/v1/comment           | GET      | 获取动态的所有评论 |
| /api/v1/comment/tomoment  | GET      | 对动态进行评论     |
| /api/v1/comment/tocomment | GET      | 对评论进行评论     |
| /api/v1/comment/like      | GET      | 对评论进行点赞     |
| /api/v1/comment/top       | GET      | 获取动态的神评论   |
| /api/v1/comment/mine      | GET      | 获取和我相关的评论 |
| /api/v1/comment/mylike    | GET      | 获取和我相关的点赞 |
| /api/v1/comment/delete    | GET      | 对评论进行删除     |

## 收藏单模块

| 接口URL                         | 请求方式 | 说明           |
| ------------------------------- | -------- | -------------- |
| /api/v1/star/moment/list/       | GET      | 获取个人收藏单 |
| /api/v1/star/moment/list/       | POST     | 创建收藏单     |
| /api/v1/star/moment/list/delete | GET      | 删除收藏单     |
| /api/v1/star/moment/list/       | PUT      | 修改收藏单     |
| /api/v1/star/moment/            | POST     | 收藏动态       |
| /api/v1/star/moment/delete      | GET      | 取消收藏动态   |

## 私信模块

| 接口URL         | 请求方式 | 说明                     |
| --------------- | -------- | ------------------------ |
| /api/v1/message | GET      | 获取关于我的所有私信     |
| /api/v1/message | GET      | 获取与对方所有的私信内容 |
| /api/v1/message | POST     | 发送私信                 |
| /api/v1/message | POST     | 更新私信的未读状态       |
