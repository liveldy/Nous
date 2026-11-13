# 第三方组件与素材

本清单说明主要直接组件，不取代随依赖附带的 LICENSE。前端、Go、Node 和 Python 的精确依赖分别由各目录锁文件记录。

| 组件 | 版本 / 来源 | 许可证或说明 |
| --- | --- | --- |
| Penguin Harness | [`@prismshadow/penguin-core` 0.2.18](https://github.com/Prism-Shadow/penguin-harness) | Apache-2.0；实际 SDK 用于本地和云端开发任务 |
| Mihomo | [v1.19.34](https://github.com/MetaCubeX/mihomo/tree/v1.19.34) | GPL-3.0；`desktop/bin/Mihomo-LICENSE.txt`；对应源码 `releases/Mihomo-Source-v1.19.34.tar.gz`，下载页随包提供 |
| Mem Reduct | [v3.5.2](https://github.com/henrypp/memreduct/tree/v.3.5.2) | GPL-3.0；独立可执行程序；随附许可证与对应源码 releases/MemReduct-Source-v3.5.2.tar.gz |
| BreezeBlue | [breeze-blue 0.23.0](https://pypi.org/project/breeze-blue/) | MIT；已有语音工具的服务接口 |
| Edge TTS | [7.3.1](https://github.com/rany2/edge-tts) | LGPL-3.0；语音工具的无密钥回退；原始 wheel 随 runtime/wheels 保留 |
| HEV SOCKS5 Tunnel | [commit 786edc86](https://github.com/heiher/hev-socks5-tunnel/tree/786edc86f92e17e91d180f43f1f70cd323f6a243) | MIT；完整 vendored 源码和子模块许可证在 `third_party/hev-socks5-tunnel` |
| JSON Schema for Go | [santhosh-tekuri/jsonschema v6.0.3](https://github.com/santhosh-tekuri/jsonschema/tree/v6.0.3) | Apache-2.0；服务端复用公开插件 Schema 校验元信息 |
| React / Vite / TypeScript | 锁文件版本 | MIT |
| jsrsasign | 11.1.5 | MIT；原 IP 的 HTTP 页面使用 RSA 发布清单验签回退 |
| AndroidX WebKit / Core | 1.12.1 / 1.15.0 | Apache-2.0；限制原生消息调用来源及系统安装文件共享 |
| Electron | 45.3.0 | MIT；分发组件附带各自声明 |
| Lucide | [lucide.dev](https://lucide.dev/license) | ISC；统一界面图标 |
| IBM Plex Sans | [IBM Plex](https://github.com/IBM/plex) | SIL Open Font License 1.1；自托管字体 |
| react-markdown / remark / rehype | 锁文件版本 | MIT；Markdown 渲染链 |
| KaTeX | 锁文件版本 | MIT；公式与字体 |
| MarkItDown | [Microsoft MarkItDown](https://github.com/microsoft/markitdown) | MIT；DOCX 转换 |
| PyMuPDF / PyMuPDF4LLM | [官方仓库](https://github.com/pymupdf/PyMuPDF) | AGPL / 商业双许可，具体见 Python 安装包条款 |
| Tesseract / antiword / FFmpeg | Linux 系统包 | 各包自带的 Apache / GPL / LGPL 条款 |

模型价格及智能体等综合评测来自 [ZeroEval / LLM Stats](https://llm-stats.com)，以 [OpenRouter](https://openrouter.ai/models) 补充价格。其余评测来自 [Arena 公开数据集](https://huggingface.co/datasets/lmarena-ai/leaderboard-dataset)、[Open ASR Leaderboard](https://huggingface.co/spaces/hf-audio/open_asr_leaderboard) 与 [TTS Arena](https://huggingface.co/spaces/ttsds/tts-arena-v2)。界面保留来源和日期；数据使用仍应遵循相应数据源条款。

品牌标记 SVG 来自公共模型品牌图标，标识权益属于对应品牌。用户提供的 Nous 指南针、AI 角色及表情素材按项目要求使用，素材包未附作者和许可证信息。没有使用外部图库照片或视频。

本次交互设计参考 [DawnBreaker](https://github.com/liveldy/DawnBreaker) 的折跃门与拾光者公开行为和文档，未复制其 AGPL 程序源码。本机网络调用使用独立实现与 Mihomo 官方控制接口。

破晓下载器作为独立插件使用 [CYQawa/YunX](https://github.com/CYQawa/YunX) Android v1.3.1 与 [tidain/YunX-Desktop](https://github.com/tidain/YunX-Desktop) Windows v1.3.3，均为 AGPL-3.0。插件移植业务层，运行模块 ZIP、完整修改源码与对应上游源码归档发布在 [Nous-Plugin-YunX](https://github.com/liveldy/Nous-Plugin-YunX)；下载器业务未写入 Nous 本体，不发布原版安装程序。
