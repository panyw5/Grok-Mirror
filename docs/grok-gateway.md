
## 聊天 API 接口

POST: /v1/chat/completions

- 请求头:

| 字段 | 类型 | 默认值 | 必填 | 描述 |
| --- | --- | --- |--- |--- |
| `Authorization` | `string` | `None` | `是` | `Bearer ${ AUTHORIZATION }` 或 <br> `Bearer ${`[Sso Token](./docs/get-sso-token.jpg)`}` <br><br> 推荐使用环境变量中的 AUTHORIZATION，自动轮询token |

- 请求参数:

| 参数名            | 类型    | 是否必须 | 描述                                                               |
| ----------------- | ------- | -------- | ------------------------------------------------------------------ |
| model             | string  | 是       | 模型名称 <br> `grok-2` `grok-3` `grok-3-think` `grok-3-deepsearch` |
| messages          | array   | 是       | 消息内容                                                           |
| stream            | boolean | 否       | 是否开启流式返回                                                   |
| conversation_id   | string  | 否       | 会话 ID，用于临时聊天                                              |
| parent_message_id | string  | 否       | 父消息 ID，用于临时聊天                                            |



## 批量录入token
POST: /api/batch-add-grok-token

- 请求参数:

| 参数名            | 类型    | 是否必须 | 描述                      |
| ----------------- | ------- | -------- | ------------------------- |
| sso_token_list             | []string  | 是       | sso token 列表                     |


## 登录
POST: /api/login
- 请求参数:

| 参数名            | 类型    | 是否必须 | 描述                      |
| ----------------- | ------- | -------- | ------------------------- |
| user_name             | string  | 是       | 用户名 (用于隔离)                    |
| email_md5             | string  | 是       | 邮箱md5（前提已经录入了token）                     |

## 登录接口v2 （无需录入token）
POST: /api/login-v2
- 请求参数:

| 参数名            | 类型    | 是否必须 | 描述                      |
| ----------------- | ------- | -------- | ------------------------- |
| user_name             | string  | 是       | 用户名 (用于隔离)                    |
| sso_token             | string  | 是       | sso_token                     |

## 获取 Grok 列表
PSOT: /api/get-grok-list
- 请求参数:

| 参数名            | 类型    | 是否必须 | 描述                      |
| ----------------- | ------- | -------- | ------------------------- |
| page             | string  | 否      | 页码                     |
| page_size             | string  | 否       | 页面大小                     |

