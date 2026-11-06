# AgentPhone233

原生 Kotlin Android 手机 Agent，支持 OpenAI 兼容服务、DeepSeek/MiMo 预设和电脑 Web 多设备管理。

## 统一下载：1.2.2

**[下载 APK＋Windows 管理器整合包（83.33 MB）](https://github.com/neko233-com/AgentPhone233-app/releases/download/v1.2.2/AgentPhone233-1.2.2-all-in-one.zip)**

一次下载即可得到 Android APK、可直接运行的 Windows x64 管理器、使用说明和校验信息。[查看本版所有文件](https://github.com/neko233-com/AgentPhone233-app/releases/tag/v1.2.2)。

需要单独下载时：

- [Android APK（79.89 MB）](https://github.com/neko233-com/AgentPhone233-app/releases/download/v1.2.2/app-release.apk)：实际应用版本 1.2.0，Android 10 及以上，arm64-v8a。
- [Windows x64 管理器（约 3.44 MB）](https://github.com/neko233-com/AgentPhone233-app/releases/download/v1.2.2/AgentPhone233-manager-1.2.2-windows-amd64.zip)：实际组件版本 1.2.2。

发布版本统一为 1.2.2；未变化的 APK 保留真实版本和正式签名。大小统一采用十进制 MB（1 MB = 1,000,000 字节）。

## 使用方法

1. 将 app-release.apk 安装到手机，配置自己的模型，按 Android 提示授予权限并开启局域网管理。
2. 在电脑运行解压后的 manager/AgentPhone233-manager.exe，本机浏览器打开 `http://127.0.0.1:23833`。
3. 扫描并配对多台手机，即可批量发送任务、分别跟进、插话、停止，并查看历史和手机画面。

管理器默认监听 **0.0.0.0:23833**。其他内网电脑打开 `http://服务器内网IP:23833`；首次访问时，在服务器本机页面点击“显示内网访问码”，然后输入该访问码。访问码不写日志，管理器重启后更新。

模型 API Key 留在手机端；电脑管理器使用证书指纹和配对令牌连接手机，Windows 配对记录由当前用户的 DPAPI 保护。应用自动创建私有工作目录，提供用量监控和内置无线调试能力。首次使用仍需按 Android 要求授予无障碍等权限。

## 验证与校验

两台 MuMu 的正式 APK 已通过多机控制流程，包括发现配对、并发手机工具、历史与画面、同时插话、单台停止隔离、离线恢复和管理器重启恢复。内网 IP 浏览器与 MuMu 登录/API 请求、UDP leader 发现、Go 竞态检查和 EXE 自检通过；DeepSeek/MiMo 此前已完成真实模型手机操作验证。本次按模拟器标准完成验收。

Release 提供 SHA256SUMS.txt；整合 ZIP 内还包含 components.json 和逐文件校验值。Android APK SHA-256：`d691a155c4a19c39f74a7951f69c6f678af98b02e8e3e702ef15f697adf02e05`。

本仓库仅公开当前整合发布、更新清单、说明及许可证，源码保持私有。基于 [DSH-Android v0.3.8](https://github.com/jackwener/DSH-Android/tree/v0.3.8)，采用 Apache-2.0，依赖许可证随应用提供。
