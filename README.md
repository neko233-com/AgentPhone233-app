# AgentPhone233

原生 Kotlin Android 手机 Agent，基于 [DSH-Android v0.3.8](https://github.com/jackwener/DSH-Android/tree/v0.3.8) 的 Compose 界面、Node.js 24 和 Android 能力桥接架构。

[下载 1.1.1 预览版 APK](https://github.com/neko233-com/AgentPhone233-app/releases/tag/v1.1.1) · Android 10 及以上 · arm64-v8a

支持接入 OpenAI 兼容服务，以及 DeepSeek、MiMo 预设；可获取上游模型列表。应用自动创建私有工作目录，并支持设备操作、任务用量监控和局域网管理。

预览版已在 MuMu 上通过真实 DeepSeek 手机操作验证。Android 11 及以上可在系统授权后使用内置无线调试，无需安装 Shizuku；Google Android 15 模拟器已验证配对和 shell，MuMu 的调试服务未提供对应连接。部分 Shizuku 专有能力尚未替代。MiMo 的真实接口复测和实体局域网发现仍待验证。任务可能消耗较多 token，Android 系统权限需要授权。

本版使用新的私有发布签名。若已安装不同签名的旧版，可能需要卸载重装；卸载会删除该应用的数据。

APK SHA-256：`a3032aebe2d60a42cbf54b95379ce5fdbdebc3846d32491971ad3b88b4f5a9b1`

本仓库仅发布安装包、更新清单与许可证。原项目采用 Apache-2.0，相关依赖的许可证随应用提供。
