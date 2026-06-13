# NexaAct

[English](README.md) | [简体中文](README.zh-CN.md)

NexaAct 是一个AI Coding桌面端，基于Openai Codex基础上深度改造的应用。对其他第三方的api兼容做了优化，让第三方的api也能使用上性能优越的上下文管理和插件，mcp，skill统一管理的Coding工具。支持登录和管理多个openai的账号，提供自定义api的快速添加方式同时拥有远程控制功能。

![NexaAct desktop workspace](.github/assets/nexaact-main.png)

## 核心功能

### 多个 OpenAI 账号与任意 API

NexaAct 可以在一个桌面应用里管理多个 OpenAI 账号，方便切换不同账号使用。

同时，NexaAct 支持自定义API接口，以及 DeepSeek、Qwen、Claude、Gemini、OpenRouter 或其他API提供商。

![NexaAct API model settings](.github/assets/api-model-settings.svg)

### 内置远程控制

NexaAct 内置远程控制功能。登录 Cloudflare 后，可以用手机扫码，在浏览器里控制和查看电脑上的 NexaAct 工作状态，且无需下载手机App。

远程控制基于用户自己的 Cloudflare 基础设施。数据完全自己保管。

<p>
  <img src=".github/assets/remote-workspace-list.svg" alt="NexaAct remote workspace project list" width="360" />
  <img src=".github/assets/remote-workspace-chat.svg" alt="NexaAct remote workspace chat composer" width="360" />
</p>

### 插件、Skills、MCP 与自动化

NexaAct 兼容 OpenAI/Codex 风格的插件工作流，并支持在应用内添加、导入和管理 Skills、插件、MCP Server 与自动化工具。

![NexaAct skills marketplace](.github/assets/skills-marketplace.svg)

### 多个第三方账号管理

支持多个Cloudflare和GitHub账号管理，可以让ai根据需要把不同的项目部署到不同的GitHub账号或者Cloudflare账号。


### 数据默认本地保存

所有 NexaAct 工作区数据均保存在你的本机设备上。NexaAct 不提供也不依赖集中式托管后台来保存 prompts、聊天、文件、API keys 或工作区历史。

## macOS 安装提醒

在 macOS 上，首次启动可能需要手动授权，因为打包版本可能不是通过 Mac App Store 分发。

如果 macOS 阻止首次打开 NexaAct，请前往 **System Settings > Privacy & Security** 授权，然后重新打开应用。根据 macOS 版本不同，可能还需要选择 **Open Anyway** 或确认信任该应用。

如果 macOS 提示 **“NexaAct” 已损坏，无法打开**，通常不是安装包真的损坏，而是因为 NexaAct 通过网站或 GitHub 下载，且当前构建可能还没有 Apple 公证，macOS Gatekeeper 给下载文件加了隔离标记。先把 NexaAct 拖到 Applications，然后运行：

```sh
xattr -dr com.apple.quarantine /Applications/NexaAct.app
```

如果 DMG 在安装前就被拦截，请先对下载目录里的 DMG 运行：

```sh
xattr -dr com.apple.quarantine ~/Downloads/NexaAct_0.1.0_aarch64.dmg
```

然后重新打开 DMG，把 NexaAct 拖到 Applications 再打开。这个命令只是移除 NexaAct 的 macOS 下载隔离标记，不会修改你的应用数据或工作区文件。

## 当前状态

NexaAct 目前正在持续开发中，后续功能会持续完善（后续会更新antigravity和Claude的账号管理）。

远程控制功能也仍在持续优化中，部分远程功能可能会有bug。

macOS 是目前主要开发和测试的平台作为首发。Windows 和 Linux 后续会更新并上架：

**jellysugnorina703@gmail.com**
