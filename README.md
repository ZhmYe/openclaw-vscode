 # OpenClaw-VSCode 项目简介

## 🚀 项目概述

**OpenClaw-VSCode** 是一款专为 VS Code 设计的扩展插件，旨在通过 WebSocket 协议与 **OpenClaw Gateway** 建立远程连接，为用户提供无缝的侧边栏聊天体验。无论您的网关部署在本地还是云端，都能一键连接，即刻开启智能对话。

---

## ✨ 核心特性

| 特性 | 说明 |
|------|------|
| 🌐 **远程连接** | 通过 WebSocket 与 OpenClaw Gateway 建立稳定连接 |
| 💬 **侧边栏聊天** | 集成于 VS Code 侧边栏的清爽聊天界面，编码沟通两不误 |
| 🔐 **令牌认证** | 支持网关令牌验证，确保连接安全可靠 |
| ⚙️ **可视化配置** | 通过 UI 界面轻松设置 URL 和 Token，无需手动编辑 JSON |
| 🔄 **自动重连** | 连接中断后自动恢复，保障会话连续性 |

---

## 🛠️ 快速开始

### 1. 安装扩展
在 VS Code 扩展市场中搜索 "OpenClaw" 并安装。

### 2. 配置连接
- 点击聊天面板中的 ⚙️ **配置** 按钮
- 输入 Gateway WebSocket 地址（例如：`ws://your-server:18789`）
- 输入网关令牌（如需要）

### 3. 开始连接
- 点击 **"连接"** 按钮
- 连接成功后即可开始聊天！

---

## ⚙️ 配置选项

在 VS Code 设置中搜索 "OpenClaw" 进行详细配置：

| 配置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| `openclaw.gatewayUrl` | string | `ws://localhost:18789` | Gateway WebSocket 地址 |
| `openclaw.gatewayToken` | string | `""` | 身份验证令牌 |
| `openclaw.autoConnect` | boolean | `false` | 启动时自动连接 |

### 配置示例

**本地网关**
```json
{
  "openclaw.gatewayUrl": "ws://localhost:18789",
  "openclaw.gatewayToken": ""
}
```

**远程网关**
```json
{
  "openclaw.gatewayUrl": "ws://your-server.com:18789",
  "openclaw.gatewayToken": "your-secret-token"
}
```

**安全连接（WSS）**
```json
{
  "openclaw.gatewayUrl": "wss://your-server.com:18789",
  "openclaw.gatewayToken": "your-secret-token"
}
```

---

## 🎮 可用命令

通过 VS Code 命令面板（`Ctrl+Shift+P` / `Cmd+Shift+P`）可执行以下操作：

- `OpenClaw: 连接到网关` — 连接至已配置的网关
- `OpenClaw: 断开连接` — 断开当前网关连接
- `OpenClaw: 配置连接` — 设置 URL 和 Token

---

## 💻 开发指南

```bash
# 安装依赖
npm install

# 编译项目
npm run compile

# 监听模式（开发时使用）
npm run watch

# 打包扩展
npm run package
```

---

## 📋 环境要求

- **VS Code**: 1.80.0 或更高版本
- **OpenClaw Gateway**: 需启用 WebSocket 支持

---

## 📄 开源协议

本项目采用 **MIT** 协议开源。

---

> 💡 **提示**: 确保您的 OpenClaw Gateway 已正确配置 WebSocket 端口并处于运行状态，以保证扩展能够正常连接。
>
---

# OpenClaw Remote Chat

VS Code extension for remote chat with OpenClaw Gateway via WebSocket.

## Features

- 🌐 **Remote Connection** - Connect to OpenClaw Gateway over WebSocket
- 💬 **Chat Interface** - Clean sidebar chat UI
- 🔐 **Token Auth** - Secure connection with gateway token
- ⚙️ **Easy Config** - Configure URL and token via UI
- 🔄 **Auto-Reconnect** - Automatic reconnection on disconnect

## Quick Start

1. **Install the extension**
2. **Configure connection**:
   - Click the ⚙️ Config button in the chat panel
   - Enter your Gateway WebSocket URL (e.g., `ws://your-server:18789`)
   - Enter your gateway token (optional)
3. **Connect**:
   - Click the "Connect" button
   - Start chatting!

## Configuration

Open VS Code settings and search for "OpenClaw":

- `openclaw.gatewayUrl` - Gateway WebSocket URL (default: `ws://localhost:18789`)
- `openclaw.gatewayToken` - Authentication token
- `openclaw.autoConnect` - Auto-connect on startup (default: `false`)

## Commands

- `OpenClaw: Connect to Gateway` - Connect to configured gateway
- `OpenClaw: Disconnect` - Disconnect from gateway
- `OpenClaw: Configure Connection` - Set URL and token

## Usage

### Local Gateway

```json
{
  "openclaw.gatewayUrl": "ws://localhost:18789",
  "openclaw.gatewayToken": ""
}
```

### Remote Gateway

```json
{
  "openclaw.gatewayUrl": "ws://your-server.com:18789",
  "openclaw.gatewayToken": "your-secret-token"
}
```

### Secure Connection (WSS)

```json
{
  "openclaw.gatewayUrl": "wss://your-server.com:18789",
  "openclaw.gatewayToken": "your-secret-token"
}
```

## Development

```bash
# Install dependencies
npm install

# Compile
npm run compile

# Watch mode
npm run watch

# Package
npm run package
```

## Requirements

- VS Code 1.80.0 or higher
- OpenClaw Gateway running with WebSocket support

## License

MIT
