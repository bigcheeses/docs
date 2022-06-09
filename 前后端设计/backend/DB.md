# 鸽子广场数据库设计 V2.0

## 用户 User

| 属性         | 类型     | 备注                                                         |
| ------------ | -------- | ------------------------------------------------------------ |
| id           | int      | 用户id（主键）                                               |
| grade        | datetime | 入学日期                                                     |
| gender       | char     | 用户性别                                                     |
| password     | char     | 保留，可空，用户登录密码                                     |
| username     | char     | 用户名                                                       |
| avatarUrl    | URL      | 用户头像URL                                                  |
| intro        | text     | 用户签名is                                                   |
| is_active    | boolean  | 用户是否可用                                                 |
| is_superuser | boolean  | 是否为超级用户                                               |
| is_staff     | boolean  | 是否为管理员                                                 |
| actived_at   | datetime | 最近活跃时间                                                 |
| fan_num      | int      | 粉丝数                                                       |
| follow_num   | int      | 关注数                                                       |
| created_at   | datetime | 注册时间                                                     |
| openid       | string   | 【微信小程序】用户唯一标识                                   |
| session_key  | string   | 【微信小程序】会话密钥                                       |
| unionid      | string   | 【微信小程序】用户在开放平台的唯一标识符，若当前小程序已绑定到微信开放平台帐号下会返回，详见 [UnionID 机制说明](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/union-id.html)。 |

## User Profile

待定

## 关注 Follow

| 属性      | 类型 | 备注                            |
| --------- | ---- | ------------------------------- |
| id        | int  | 主键（A关注B）                  |
| user_id   | int  | 用户B id(用户A关注的对象)(外键) |
| follow_id | int  | 用户A id（外键）                |

## 动态 Moment

| 属性         | 类型       | 备注                                           |
| ------------ | ---------- | ---------------------------------------------- |
| id           | int        | 动态id（主键）                                 |
| user_id      | int        | 用户id,发布动态的id(外键)                      |
| content      | richtext   | 发布动态的内容                                 |
| images       | json       | 动态附带的图片【暂时打算直接存url json】       |
| user_like    | ManyToMany | 点赞该动态的用户列表（会自动生成一个多对多表） |
| share_num    | int        | 分享数                                         |
| hot_comment  | int        | 热评id（外键）                                 |
| created_at   | datetime   | 创建时间                                       |
| updated_at   | datetime   | 最近编辑时间                                   |
| is_published | boolean    | 是否公开                                       |



## 点赞动态记录表 LikeMomentTime（记录用户点赞动态时间）

| 属性      | 类型     | 备注             |
| --------- | -------- | ---------------- |
| id        | int      | 点赞记录id(主键) |
| moment_id | int      | 动态id(外键)     |
| user_id   | int      | 用户id(外键)     |
| update_at | datetime | 用户点赞时间     |



## 用户浏览动态记录 MomentHistory

| 属性      | 类型     | 备注             |
| --------- | -------- | ---------------- |
| id        | int      | 浏览记录id(主键) |
| user_id   | int      | 用户id（外键）   |
| moment_id | int      | 动态id(外键)     |
| last_time | datetime | 最近浏览时间     |





## 评论 MomentComment

| 属性       | 类型       | 备注                                       |
| ---------- | ---------- | ------------------------------------------ |
| id         | int        | 评论记录id(主键)                           |
| moment_id  | int        | 被评论的动态id（外键）                     |
| reply_to   | int        | 回复用户的id                               |
| user_id    | int        | 评论的用户id(外键)                         |
| parent_id  | Tree       | 树结构，上级评论id(外键)，父节点等信息     |
| created_at | datetime   | 创建时间                                   |
| content    | richtext   | 评论的内容                                 |
| user_like  | ManyToMany | 点赞该评论的用户（会自动生成一个多对多表） |



## 点赞评论记录表 LikeMomentCommentTime（记录用户点赞评论时间）

| 属性      | 类型     | 备注             |
| --------- | -------- | ---------------- |
| id        | int      | 点赞记录id(主键) |
| moment_id | int      | 动态id(外键)     |
| user_id   | int      | 用户id(外键)     |
| update_at | datetime | 用户点赞时间     |





## 消息 Message

| 属性         | 类型     | 备注                    |
| ------------ | -------- | ----------------------- |
| id           | int      | 消息id（主键）          |
| from_user_id | int      | 发送者A的id(外键)       |
| to_user_id   | int      | 接收者B的id(外键)       |
| content      | RichText | 发送信息内容            |
| created_at   | datetime | 发送时间                |
| type         | SmallInt | 文字/图片/视频【0/1/2】 |
| is_read      | Boolean  | 是否已读                |

## 标签 Moment Tag

| 属性      | 类型 | 备注         |
| --------- | ---- | ------------ |
| id        | int  | 标签id(主键) |
| name      | char | 标签名字     |
| use_num   | int  | 使用次数     |
| moment_id | int  | 动态id(外键) |

## 收藏单 Moment Star

| 属性       | 类型       | 备注                                         |
| ---------- | ---------- | -------------------------------------------- |
| id         | int        | 收藏条目id(主键)                             |
| user_id    | int        | 收藏者id(外键)                               |
| moment     | ManyToMany | 收藏动态id列表(外键，会自动生成一个多对多表) |
| title      | char       | 收藏单名字，同一用户收藏单名不可相同         |
| created_at | datetime   | 创建时间                                     |
| update_at  | datetime   | 修改时间                                     |
| is_publish | boolean    | 是否公开                                     |



