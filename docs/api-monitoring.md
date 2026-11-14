# API 监视

接口以列表展示，保留编辑、密钥复制、状态检测、模型与账户信息、生成测速及删除。每日用量使用同一张图，以不同颜色的线展示每个接口的请求与 Token，左轴为请求数、右轴为 Token 数，支持缩放、平移和全屏。用量统计为 Nous 记录的已完成模型调用，日期边界为 Asia/Shanghai。旧版本没有记录每日明细，不根据累计数倒推历史。

本机检测和后台检测均使用对应客户端的网络通道、系统代理及 VPN。不同设备与服务器网页端的检测记录隔离；服务器直连结果不会覆盖客户端结果。最近有效元数据持久保存，临时连接失败会显示错误并保留上次有效参数；修改地址、密钥或协议后重新校验。开启自动检测的接口在设备在线时定期更新。

## Devin

使用 [Devin API v3](https://docs.devin.ai/api-reference/authentication)，Base URL 为 `https://api.devin.ai/v3`。API Key 为 `cog_…` 格式，使用 Bearer 认证；组织 ID 为 `org-…`，它不是第二把 API 密钥。

监视只执行 GET：`/self` 验证身份；`/organizations/{org_id}/sessions?first=1` 查询会话可访问性与接口提供的总数；`/organizations/{org_id}/consumption/daily` 查询最近30天 ACU。余额或消费权限不足时单独显示该项错误，不伪造值，不把身份认证成功误判为整项断线。

Devin 是任务 API，不提供此应用所需的兼容聊天推理接口，因此不出现在开发、写作和助手的模型选择中，不提供生成测速，不将 ACU 换算为 Token。监视不会创建、归档或终止 Devin 任务。消费查询遵循官方 PST（UTC-08:00）日边界。

接口文档：[会话列表](https://docs.devin.ai/api-reference/v3/sessions/organizations-sessions)、[组织每日用量](https://docs.devin.ai/api-reference/v3/consumption/organizations-consumption-daily)、[OpenAPI](https://docs.devin.ai/v3-openapi.json)。
