# AgentPhone233

原生 Kotlin Android 手机 Agent，基于 [DSH-Android v0.3.8](https://github.com/jackwener/DSH-Android/tree/v0.3.8) 的 Compose 界面、Node.js 24 和 Android 能力桥接架构。

- [下载 Android 1.2.0 APK](https://github.com/neko233-com/AgentPhone233-app/releases/download/v1.2.0/app-release.apk)：约 **79.89 MB**，Android 10 及以上，arm64-v8a。
- [下载 Windows x64 内网管理器 1.2.2](https://github.com/neko233-com/AgentPhone233-app/releases/download/manager-v1.2.2/AgentPhone233-manager-1.2.2-windows-amd64.zip)：约 **3.44 MB**。

大小采用十进制 MB（1 MB = 1,000,000 字节）。管理器独立更新，手机应用的更新入口保持 Android 版本。

支持 OpenAI 兼容服务、DeepSeek 和 MiMo 预设、上游模型发现、自定义 BaseURL、设备操作、用量监控和内网管理。应用自动创建私有工作目录；模型 API Key 保存在手机端，不需要交给电脑管理器。

## 电脑同时管理多台手机

1. 解压 Windows 管理器，运行 `AgentPhone233-manager.exe`，在电脑浏览器打开 `http://127.0.0.1:23833`。
2. 手机安装 APK、配置自己的模型，并按 Android 要求授予无障碍等权限，在手机权限设置中开启局域网管理。
3. 电脑网页扫描设备，核对手机显示的证书指纹，用配对令牌连接设备。选中多台设备后可以批量发送任务、分别跟进、插话或停止任务，并查看历史和画面。

电脑与手机需要网络互通。管理网页默认监听 `0.0.0.0:23833`，其他内网电脑可访问；手机通道验证证书指纹和令牌，Windows 配对记录由当前用户的 DPAPI 保护。已安装 Android SDK Platform Tools 时，还可通过本机 ADB 模拟器端口转发发现设备。

管理器的 `--check-startup` 使用临时数据和随机回环端口自检后自动退出。可用 `--listen 127.0.0.1:23848 --data-dir D:/AgentPhone233-manager-data` 指定端口及独立配对目录；`--run-for 2m` 用于定时诊断并正常退出。

其他内网电脑打开 `http://服务器内网IP:23833`。首次连接时，在服务器电脑的 `http://127.0.0.1:23833` 页面点击“显示内网访问码”，然后在其他电脑输入。访问码不写日志，管理器重启后更新。1.2.2 已通过实际 `0.0.0.0` 套接字、内网 IP 浏览器登录及 API、MuMu 内网 HTTP 访问和 UDP leader 发现检查。

## 已验证范围

DeepSeek 和 MiMo 此前已在 MuMu 完成真实模型卸载、安装 TapTap 并搜索原神等验证。Android 11 及以上可在系统授权后使用内置无线调试，无需另外安装 Shizuku；Google Android 15 模拟器已验证配对、后台屏幕和恢复路径。首次使用仍需授予 Android 系统权限。

管理器与两台隔离 MuMu 上的正式 1.2.0 APK，使用本地模型服务验证了网页发现配对、并发手机工具、历史及画面、同时插话、单台停止隔离、离线恢复和管理器重启恢复。正式 EXE 启动自检及 Go 竞态检查通过。多机手机控制测试使用 ADB 转发的证书绑定 TLS；本次按模拟器标准完成验收。

Android 1.2.0 APK SHA-256：`d691a155c4a19c39f74a7951f69c6f678af98b02e8e3e702ef15f697adf02e05`。管理器的校验文件随其 Release 提供。

本仓库仅发布安装包、更新清单、说明与许可证，源码仓库保持私有。原项目采用 Apache-2.0，相关依赖许可证随应用提供。
