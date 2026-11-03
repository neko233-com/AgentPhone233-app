# AgentPhone

原生 Kotlin 手机 Agent，基于 [DSH-Android v0.3.8](https://github.com/jackwener/DSH-Android/tree/v0.3.8) 的 Compose、内嵌 Node.js 24 和 Android 能力桥接架构。

本仓库用于公开发布 APK、更新清单和许可证说明。源码仓库保持私有；不会复制旧工程历史、API Key 或签名文件。

原生重构版本正在验证，通过验收的安装包将发布在 [Releases](https://github.com/neko233-com/AgentPhone233-app/releases)。

- 自己的 API Key 接入 DeepSeek、MiMo 或 OpenAI 兼容服务，自动获取模型并验证工具调用。
- 自动创建 App 私有工作目录，默认完全访问；Android 系统权限仍需首次授予。
- 引擎随 APK 打包，首次启动不下载 rootfs；扩展和更新支持镜像回退及完整性校验。
- 原始项目采用 Apache-2.0，保留相应许可证和依赖署名。
