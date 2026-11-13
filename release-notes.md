Nous 1.0.4 · 插件兼容性修复

原生客户端在插件安装和打开之前读取本机 preferences.appVersion，网页使用在线发布版本。版本与插件包同时准备完成后才创建页面，按 requiresHost 阻止不兼容客户端，显示明确更新提示。异步回复绑定原始 iframe 和 nonce，避免切换页面后收到旧请求结果。下载器业务保留在独立插件中。

全能下载器1.1.5修复Android视频模型、解析/重试/重置、下载接口参数及设置回调，并增加实际Android业务类回归。Windows与Android安装包构建，APK签名及lint通过；自动检查与原生桌面插件测试通过。Android采用API35/Robolectric测试，尚无实机验证。

Windows只提供安装版；Android名称Nous。门户仓库不上传主程序源码。插件完整对应源码与模块独立发布，所有发行文件均保存在GitHub，原IP服务器仅提供网站和接口。
