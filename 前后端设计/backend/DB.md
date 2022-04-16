# 鸽子广场数据库设计 V0.1

## 用户 User

| 属性        | 类型   | 备注                                                         |
| ----------- | ------ | ------------------------------------------------------------ |
| id          |        |                                                              |
| phone       |        |                                                              |
| password    |        | 保留，可空                                                   |
| student_id  |        |                                                              |
| username    |        |                                                              |
| avatar      |        |                                                              |
| intro       |        |                                                              |
| admin_type  |        | 暂时只分管理员与普通用户                                     |
| actived_at  |        | 最近活跃时间                                                 |
| fan_num     |        | 粉丝数                                                       |
| follow_num  |        | 关注数                                                       |
| created_at  |        | 注册时间                                                     |
| openid      | string | 【微信小程序】用户唯一标识                                   |
| session_key | string | 【微信小程序】会话密钥                                       |
| unionid     | string | 【微信小程序】用户在开放平台的唯一标识符，若当前小程序已绑定到微信开放平台帐号下会返回，详见 [UnionID 机制说明](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/union-id.html)。 |

## User Profile

待定

## 关注 Follow

| 属性      | 类型 | 备注           |
| --------- | ---- | -------------- |
| id        |      |                |
| user_id   |      | 用户id         |
| follow_id |      | 用户关注的人id |

## 动态 Moment

| 属性         | 类型 | 备注                                     |
| ------------ | ---- | ---------------------------------------- |
| id           |      |                                          |
| user_id      |      |                                          |
| content      |      |                                          |
| images       |      | 动态附带的图片【暂时打算直接存url list】 |
| like_num     |      | 点赞数【以下几个数，考虑redis缓存】      |
| star_num     |      | 收藏数                                   |
| comment_num  |      | 评论数                                   |
| share_num    |      | 分享数                                   |
| hot_comment  |      | 热评id                                   |
| created_at   |      | 创建时间                                 |
| updated_at   |      | 最近编辑时间                             |
| is_published |      | 是否公开                                 |

## 评论 Comment

| 属性       | 类型 | 备注       |
| ---------- | ---- | ---------- |
| id         |      |            |
| moment     |      |            |
| user_id    |      |            |
| parent_id  |      | 上级评论id |
| created_at |      |            |
| content    |      |            |
| like_num   |      | 点赞数     |

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

| 属性    | 类型 | 备注     |
| ------- | ---- | -------- |
| id      |      |          |
| name    |      |          |
| use_num |      | 使用次数 |

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

## 收藏单 Star

| 属性       | 类型 | 备注 |
| ---------- | ---- | ---- |
| id         |      |      |
| user_id    |      |      |
| star_name  |      |      |
| created_at |      |      |

**Satr List**

| 属性      | 类型 | 备注 |
| --------- | ---- | ---- |
| id        |      |      |
| moment_id |      |      |
| star_id   |      |      |

## 浏览记录 History

| 属性       | 类型 | 备注 |
| ---------- | ---- | ---- |
| id         |      |      |
| user_id    |      |      |
| moment_id  |      |      |
| created_at |      |      |

## 热榜 Top【可以考虑加入redis】

| 属性   | 类型 | 备注 |
| ------ | ---- | ---- |
| id     |      |      |
| moment |      |      |