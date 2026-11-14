# API 监视

接口以列表展示，保留编辑、密钥复制、状态检测、模型与账户信息、生成测速及删除。每日用量使用同一张图，以不同颜色的线展示每个接口的请求与 Token，左轴为请求数、右轴为 Token 数，支持缩放、平移和全屏。用量统计为 Nous 记录的已完成模型调用，日期边界为 Asia/Shanghai。旧版本没有记录每日明细，不根据累计数倒推历史。

本机检测和后台检测均使用对应客户端的网络通道、系统代理及 VPN。不同设备与服务器网页端的检测记录隔离；服务器直连结果不会覆盖客户端结果。最近有效元数据持久保存，临时连接失败会显示错误并保留上次有效参数；修改地址、密钥或协议后重新校验。开启自动检测的接口在设备在线时定期更新。

## Devin

使用 [Devin API v3](https://docs.devin.ai/api-reference/authentication)，Base URL 为 `https://api.devin.ai/v3`。API Key 为 `cog_…` 格式，使用 Bearer 认证；组织 ID 为 `org-…`，可留空通过`/self`识别，它不是第二把 API 密钥。

监视只执行 GET：`/self` 验证身份；`/organizations/{org_id}/sessions?first=1` 查询会话可访问性与接口提供的总数；`/organizations/{org_id}/consumption/daily` 查询最近30天 ACU。余额或消费权限不足时单独显示该项错误，不伪造值，不把身份认证成功误判为整项断线。

Devin官方v3是云端任务API，与[Devin CLI的模型列表](https://docs.devin.ai/cli/models)属于不同入口。本应用沿用官方v3凭证，在接口详情展示协议提供的任务模式；预览模式是否启用以账户实际权限为准，不伪造Claude/GPT等底层模型目录。不提供Token生成测速，也不将ACU换算为Token。消费查询遵循官方PST（UTC-08:00）日边界。

在接口详情的“Devin云端任务”选择模式、填写任务与ACU上限（1–10），确认计费后创建会话。任务会在切换页面后继续跟踪，显示真实消息、状态、ACU及接口返回的超额用量；可继续已有会话、重新查询或停止，也可在Devin控制台查看。只读监视仍不会自动创建或停止任务。

提交具有账户范围的请求标识，重复点击或网络重试不重复创建收费会话。创建结果不确定时明确提示在控制台核对，不自动重新创建。服务重启后仅查询已知会话。原生端创建、查询与停止均通过对应设备，离线不回退服务器。完全关闭应用不代表供应商停止了已经接受的云端任务，可使用停止操作或供应商控制台管理。

接口文档：[会话列表](https://docs.devin.ai/api-reference/v3/sessions/organizations-sessions)、[组织每日用量](https://docs.devin.ai/api-reference/v3/consumption/organizations-consumption-daily)、[OpenAPI](https://docs.devin.ai/v3-openapi.json)。
