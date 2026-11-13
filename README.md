# Nous

Nous官方门户、公开插件SDK与客户端发布仓库。**不包含Nous主程序源码。**

- [官方门户](https://liveldy.github.io/Nous/)
- [Nous 1.1.0 客户端](https://github.com/liveldy/Nous/releases/tag/v1.1.0)
- [原IP网页版](http://110.42.63.153:7783)
- [完整插件开发手册](docs/plugin-development.md) · [方法参考](docs/plugin-api-reference.md)
- [公开SDK 1.2.0下载](https://github.com/liveldy/Nous/releases/download/v1.1.0/Nous-Plugin-SDK-1.2.0.zip) · [独立示例](sdk/examples)
- [破晓下载器（DawnDownloader）](https://github.com/liveldy/Nous-Plugin-YunX)
- [版本与分发](docs/version-management.md)

Nous 1.1.0提供Plugin Interface1.2。插件api必须存在于宿主明确声明的supportedApis列表，另检查最低宿主版本、平台、权限和必需方法。此版明确兼容1.0、1.1、1.2；未知协议拒绝安装，不推断未来版本兼容。

Windows x64仅提供安装版，Android ARM64应用名Nous。客户端必须登录；网页版游客仅使用能力与成本。全部客户端与插件发行物保存在GitHub，服务器不保存分发包。

SDK与示例采用MIT，插件依各自及上游许可证。原生代码属于可信本机代码；安装授权不等于操作系统沙箱。宿主与插件产品版本分别维护。
