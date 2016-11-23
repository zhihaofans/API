# [Acfun](http://www.acfun.tv)

# 一、用户类

## 1.登陆
**地址**： `http://www.acfun.tv/login.aspx`

**请求方式**： `POST`

**参数**：

- `username`: 用户名

- `password`: 密码，未加密

## 2.注册

### 2.1 检测手机是否注册
**地址**： `http://www.acfun.tv/mobileUnique.aspx`

**请求方式**： `GET`

**参数**：

- `mobile`: 手机号码

### 2.2 检测用户名是否注册
**地址**： `http://www.acfun.tv/username_unique.aspx`

**请求方式**： `GET`

**参数**：

- `username`: 用户名

### 2.3 获取网页验证码
**地址**： `http://www.acfun.tv/captcha.svl`

**请求方式**： `GET`

**参数**：

- `d`: 时间戳,以毫秒为单位

### 2.4 获取手机验证码验证码
**地址**： `http://www.acfun.tv/mobileValidate.aspx`

**请求方式**： `GET`

**参数**：

- `mobile`: 手机号码

- `captcha`: 网页验证码

### 2.4 使用手机号码注册
**地址**： `http://www.acfun.tv//mobileRegister.aspx?code=666666&mobile=*&password=123456&password2=123456&username=aaaaadsda`

**请求方式**： `POST`

**参数**：

- `mobile`: 手机号码

- `code`: 手机验证码

- `password`: 密码

- `password2`: 确认密码

- `username`: 用户名

## 3 获取未读信息
**地址**： `http://www.acfun.tv/member/unRead.aspx`

**请求方式**： `GET`

**需要登陆**

**参数**：

- `uid`: 用户id

## 4 签到
**地址**： `http://www.acfun.tv/webapi/record/actions/signin`

**请求方式**： `GET`

**需要登陆**

**参数**：

- `date`: 时间戳,以毫秒为单位

- `channel`: 未知

## 5 私信
**地址**： `http://www.acfun.tv/api/mail.aspx?name=getGroups&page=1`

**请求方式**： `GET`

**需要登陆**

**参数**：

- `name`: 操作名称

- `p2p`: 我的id与对方id，格式为`000-000` (我id-对方id)

- `content`: 私信内容

- `userId`: 对方id

- `page`: 页数

### 5.1 获取私信列表

**参数**：

- `name`= `getGroups`

- `page`= `1` (以实际为准)

### 5.2 读取某个私信

**参数**：

- `name`= `getMails`

- `page`= `1` (以实际为准)

- `p2p`= `000-000` (以实际为准)

### 5.3 检测是否有未读

**参数**：

- `name`= `isHaveUnreaded`

- `p2p`= `000-000` (以实际为准)

### 5.4 发送私信

**参数**：

- `name`= `newMail`

- `content`= `私信内容` (以实际为准)

- `userId`= `用户id` (以实际为准)

## 6 获取自己收藏夹

**请求方式**： `GET`

**需要登陆**

### 6.1 投稿

**地址**： `http://www.acfun.tv/member/collection.aspx`

**参数**：

- `count`：每页显示多少,最高为`20`

- `pageNo`：页数,从 `1` 开始

- `channelId`：频道id,默认为 `0`。频道:`动画:1`,`音乐:58`,`舞蹈:123`,`游戏:59`,`娱乐:60`,`科技:70`,`影视:68`,`体育:`69,`彼女:128`,`鱼塘:125`,`文章:63`。

### 6.2 合辑

**地址**： `http://www.acfun.tv/member/specialCollectList.aspx`

**参数**：

- `pageSize：`每页显示多少,最高为`20`

- `pageNo`：页数,从 `1` 开始

### 6.3 剧集

**地址**： `http://www.acfun.tv/bangumi/bangumi/stow/page`

**参数**：

- `pageSize：`每页显示多少,最高为`20`

- `pageNo`：页数,从 `1` 开始

- `sort`：不知道是什么,默认为 `7`

- `type`：(频道/分类;空白为所有,1动画,2电影,3综艺,4电视剧)

## 7 获取用户信息

**地址**： `http://www.acfun.tv/usercard.aspx`

**参数**：

- `username`：用户名

## 8 获取用户粉丝/关注

**地址**： `http://www.acfun.tv/api/friendExt.aspx`

**参数**：

- `name`：操作名称。粉丝为 `getFollowedList` ,关注为 `getFollowingList` 。

- `userId`：用户id

- `pageSize：`每页显示多少,最高为`20`

- `pageNo`：页数,从 `1` 开始


## 9 获取用户投稿

**地址**： `http://www.acfun.tv/u/contributeList.aspx`

**参数**：

- `name`：操作名称。粉丝为 `getFollowedList` ,关注为 `getFollowingList` 。

- `userId`：用户id

- `pageSize：`每页显示多少,最高为`20`

- `pageNo`：页数,从 `1` 开始

- `channelId`：频道id,默认为 `0`。频道:`动画:1`,`音乐:58`,`舞蹈:123`,`游戏:59`,`娱乐:60`,`科技:70`,`影视:68`,`体育:`69,`彼女:128`,`鱼塘:125`,`文章:63`。
