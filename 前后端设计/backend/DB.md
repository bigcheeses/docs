# 鸽子广场数据库设计

## 用户 User

| 属性       | 类型 | 备注     |
| ---------- | ---- | -------- |
| id         |      |          |
| phone      |      |          |
| password   |      |          |
| student_id |      |          |
| username   |      |          |
| avatar     |      |          |
| intro      |      |          |
| wechat_id  |      | 接入微信 |
| fan        |      | 粉丝数   |
| follow     |      | 关注数   |
| created_at |      | 注册时间 |

## User Profile

待定

## 关注 Follow

| 属性      | 类型 | 备注           |
| --------- | ---- | -------------- |
| id        |      |                |
| user_id   |      | 用户id         |
| follow_id |      | 用户关注的人id |

## 动态 Moment

| 属性        | 类型 | 备注   |
| ----------- | ---- | ------ |
| id          |      |        |
| user_id     |      |        |
| content     |      |        |
| image       |      |        |
| like        |      | 点赞数 |
| star        |      | 收藏数 |
| comment     |      | 评论数 |
| share       |      | 分享数 |
| hot_comment |      | 热评id |

## 评论 Comment

| 属性      | 类型 | 备注       |
| --------- | ---- | ---------- |
| id        |      |            |
| moment    |      |            |
| user_id   |      |            |
| parent_id |      | 上级评论id |
| time      |      |            |
| content   |      |            |
| like      |      | 点赞数     |

## 消息 Message

| 属性         | 类型 | 备注                    |
| ------------ | ---- | ----------------------- |
| id           |      |                         |
| from_user_id |      |                         |
| to_user_id   |      |                         |
| content      |      |                         |
| created_at   |      |                         |
| type         |      | 文字/图片/视频【0/1/2】 |
| read         |      | 是否已读                |

## 标签 Tag

| 属性 | 类型 | 备注 |
| ---- | ---- | ---- |
| id   |      |      |
| name |      |      |

**Moment Tag**

| 属性      | 类型 | 备注 |
| --------- | ---- | ---- |
| id        |      |      |
| tag_id    |      |      |
| moment_id |      |      |

## 点赞 Like

| 属性       | 类型 | 备注 |
| ---------- | ---- | ---- |
| id         |      |      |
| user_id    |      |      |
| moment_id  |      |      |
| comment_id |      |      |
| created_at |      |      |

## 收藏表 Star

| 属性                | 类型 | 备注 |
| ------------------- | ---- | ---- |
| id                  |      |      |
| user_id             |      |      |
| moment_id           |      |      |
| created_at          |      |      |

## 浏览记录 History

| 属性       | 类型 | 备注 |
| ---------- | ---- | ---- |
| id         |      |      |
| user_id    |      |      |
| moment_id  |      |      |
| created_at |      |      |

## 热榜 Top

| 属性   | 类型 | 备注 |
| ------ | ---- | ---- |
| id     |      |      |
| moment |      |      |