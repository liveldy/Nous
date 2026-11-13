Nous 1.0.2 · 修复更新与网页登录

修复“客户端与关于”读取缺少 changes 的版本记录时白屏，兼容 notes 并过滤异常记录。增加通用、隔离的官方网页登录窗口，供可信插件获取当前平台 Cookie；验证与本地保存由插件负责。全能下载器 1.1.2 独立发布，修复 Android 回调类型并增加五个平台的网页登录导入。

Windows 仅提供安装版，Android 应用名称 Nous。宿主与插件发行物统一保存在各自 GitHub Release，服务器不保存客户端或插件分发文件。

验证：17 项自动检查、实际 Electron 网页登录窗口隔离与 HTTP-only Cookie 提取、原生安装/权限/导航/设置/停用/重启/卸载、Android 实际构造签名回归、真实下载暂停与重启恢复及 SHA256、网页和移动布局的关于页面。Android 完成构建和 lint；没有连接的实机，尚未验证真实平台账号的完整登录流程。

插件独立发行：https://github.com/liveldy/Nous-Plugin-YunX/releases/tag/v1.1.2
