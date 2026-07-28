# 🦞 OpenClaw — Personal AI Assistant 🦞 OpenClaw — 个人人工智能助手



![OpenClaw](https://raw.githubusercontent.com/openclaw/openclaw/main/docs/assets/openclaw-logo-text.png)

**EXFOLIATE! EXFOLIATE! 去角质！去角质！**

[![CI status](https://camo.githubusercontent.com/1ddb1ef286e297deafb2a4372b7c65516ae65368fd22878a7454dabc2fc4738b/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f616374696f6e732f776f726b666c6f772f7374617475732f6f70656e636c61772f6f70656e636c61772f63692e796d6c3f6272616e63683d6d61696e267374796c653d666f722d7468652d6261646765)](https://github.com/openclaw/openclaw/actions/workflows/ci.yml?branch=main) [![GitHub release](https://camo.githubusercontent.com/9fcbb4c3c5cf1f8657a73e45b9c76a0074008d658c07f5558e474191c7aef8fb/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f762f72656c656173652f6f70656e636c61772f6f70656e636c61773f696e636c7564655f70726572656c6561736573267374796c653d666f722d7468652d6261646765)](https://github.com/openclaw/openclaw/releases) [![Discord](https://camo.githubusercontent.com/1860c01c5ab9a20c37ea5a09fcf7ea1471eb95ed7095bb99d3c5a7331061ccda/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f313435363335303036343036353930343836373f6c6162656c3d446973636f7264266c6f676f3d646973636f7264266c6f676f436f6c6f723d776869746526636f6c6f723d353836354632267374796c653d666f722d7468652d6261646765)](https://discord.gg/clawd) [![MIT License](https://camo.githubusercontent.com/608c8dfda488178950ce502d7697514db3a6a712579327ed90b9b594260f6355/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d4d49542d626c75652e7376673f7374796c653d666f722d7468652d6261646765)](https://github.com/xianyu110/clawdbot/blob/main/LICENSE)

**OpenClaw** is a *personal AI assistant* you run on your own devices. It answers you on the channels you already use (WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, iMessage, Microsoft Teams, WebChat), plus extension channels like BlueBubbles, Matrix, Zalo, and Zalo Personal. It can speak and listen on macOS/iOS/Android, and can render a live Canvas you control. The Gateway is just the control plane — the product is the assistant.
**OpenClaw** 是一个你可以在自己设备上运行的*个人 AI 助手* 。它会在你已经使用的频道（WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、iMessage、Microsoft Teams、WebChat）以及扩展频道如 BlueBubbles、Matrix、Zalo 和 Zalo Personal 上回答你。它可以在 macOS/iOS/Android 上说话和监听，还能渲染你控制的实时画布。网关只是控制平面——产品是助手。

If you want a personal, single-user assistant that feels local, fast, and always-on, this is it.
如果你想要一个个性化、单用户助理，感觉本地化、快速且始终在线，这就是你的选择。

[Website](https://openclaw.ai/) · [Docs](https://docs.openclaw.ai/) · [DeepWiki](https://deepwiki.com/openclaw/openclaw) · [Getting Started](https://docs.openclaw.ai/start/getting-started) · [Updating](https://docs.openclaw.ai/install/updating) · [Showcase](https://docs.openclaw.ai/start/showcase) · [FAQ](https://docs.openclaw.ai/start/faq) · [Wizard](https://docs.openclaw.ai/start/wizard) · [Nix](https://github.com/openclaw/nix-openclaw) · [Docker](https://docs.openclaw.ai/install/docker) · [Discord](https://discord.gg/clawd)
[网站 ](https://openclaw.ai/)·[ 文档 ](https://docs.openclaw.ai/)·[DeepWiki](https://deepwiki.com/openclaw/openclaw) ·[ 入门 ](https://docs.openclaw.ai/start/getting-started)·[ 更新 ](https://docs.openclaw.ai/install/updating)·[ 展示·](https://docs.openclaw.ai/start/showcase)[ 常见问题 ](https://docs.openclaw.ai/start/faq)·[ 巫师 ](https://docs.openclaw.ai/start/wizard)·[ 尼克斯 ](https://github.com/openclaw/nix-openclaw)·[Docker](https://docs.openclaw.ai/install/docker) ·[Discord](https://discord.gg/clawd)

Preferred setup: run the onboarding wizard (`openclaw onboard`) in your terminal. The wizard guides you step by step through setting up the gateway, workspace, channels, and skills. The CLI wizard is the recommended path and works on **macOS, Linux, and Windows (via WSL2; strongly recommended)**. Works with npm, pnpm, or bun. New install? Start here: [Getting started](https://docs.openclaw.ai/start/getting-started)
首选配置：在终端里运行入职向导（`openclaw`）。向导一步步引导你设置网关、工作区、渠道和技能。CLI 向导是推荐的路径，适用于 **macOS、Linux 和 Windows（通过 WSL2;强烈推荐）。** 适用于 NPM、PNPM 或 Bun。新安装？从这里开始：[ 开始](https://docs.openclaw.ai/start/getting-started)

**Subscriptions (OAuth): 订阅（OAuth）：**

- **[Anthropic](https://www.anthropic.com/)** (Claude Pro/Max)
  **[拟人版 ](https://www.anthropic.com/)**（Claude Pro/Max）
- **[OpenAI](https://openai.com/)** (ChatGPT/Codex)
  **[OpenAI](https://openai.com/)**（ChatGPT/Codex）

Model note: while any model is supported, I strongly recommend **Anthropic Pro/Max (100/200) + Opus 4.6** for long‑context strength and better prompt‑injection resistance. See [Onboarding](https://docs.openclaw.ai/start/onboarding).
模型说明：虽然支持任何型号，但我强烈推荐 **Anthropic Pro/Max（100/200）+ Opus 4.6**，因为它能提供长上下文强度和更好的提示注入抗性。参见[入职培训 ](https://docs.openclaw.ai/start/onboarding)。

## Models (selection + auth) 模型（选择+认证）



- Models config + CLI: [Models](https://docs.openclaw.ai/concepts/models)
  Config + CLI 模型：[ 模型](https://docs.openclaw.ai/concepts/models)
- Auth profile rotation (OAuth vs API keys) + fallbacks: [Model failover](https://docs.openclaw.ai/concepts/model-failover)
  认证配置文件轮换（OAuth 与 API 密钥）+ 回退：[ 模型故障切换](https://docs.openclaw.ai/concepts/model-failover)

## Install (recommended) 安装（推荐）



Runtime: **Node ≥22**.
运行时间： **节点≥22**。

```
npm install -g openclaw@latest
# or: pnpm add -g openclaw@latest

openclaw onboard --install-daemon
```



The wizard installs the Gateway daemon (launchd/systemd user service) so it stays running.
向导安装了 Gateway daemon（launchd/systemd 用户服务），使其保持运行。

## Quick start (TL;DR) 快速入门（简而言之;DR）



Runtime: **Node ≥22**.
运行时间： **节点≥22**。

Full beginner guide (auth, pairing, channels): [Getting started](https://docs.openclaw.ai/start/getting-started)
完整入门指南（认证、配对、频道）：[ 入门](https://docs.openclaw.ai/start/getting-started)指南

```
openclaw onboard --install-daemon

openclaw gateway --port 18789 --verbose

# Send a message
openclaw message send --to +1234567890 --message "Hello from OpenClaw"

# Talk to the assistant (optionally deliver back to any connected channel: WhatsApp/Telegram/Slack/Discord/Google Chat/Signal/iMessage/BlueBubbles/Microsoft Teams/Matrix/Zalo/Zalo Personal/WebChat)
openclaw agent --message "Ship checklist" --thinking high
```



Upgrading? [Updating guide](https://docs.openclaw.ai/install/updating) (and run `openclaw doctor`).
升级？[ 更新指南 ](https://docs.openclaw.ai/install/updating)（并运行 `openclaw 医生 `）。

## Development channels 开发渠道



- **stable**: tagged releases (`vYYYY.M.D` or `vYYYY.M.D-<patch>`), npm dist-tag `latest`.
  **稳定** ：带标签的发布（`vYYYY.M.D` 或 `vYYYY.M.D-<patch>`），npm dist-tag ` 最新 `。
- **beta**: prerelease tags (`vYYYY.M.D-beta.N`), npm dist-tag `beta` (macOS app may be missing).
  **测试**版：预发布标签（`vYYYY.M.D-beta.N`），npm dist-tag `beta`（macOS 应用可能缺失）。
- **dev**: moving head of `main`, npm dist-tag `dev` (when published).
  **开发**者：主项目负责``人，NPM 负责`人，发布`时担任非专业负责人。

Switch channels (git + npm): `openclaw update --channel stable|beta|dev`. Details: [Development channels](https://docs.openclaw.ai/install/development-channels).
切换频道（git + npm）： `openclaw update --channel stable|beta|dev` 。详情：[ 开发渠道 ](https://docs.openclaw.ai/install/development-channels)。

## From source (development) 源代码（开发）



Prefer `pnpm` for builds from source. Bun is optional for running TypeScript directly.
我更喜欢用 `pnpm` 来构建源代码。Bun 是直接运行 TypeScript 的可选选项。

```
git clone https://github.com/openclaw/openclaw.git
cd openclaw

pnpm install
pnpm ui:build # auto-installs UI deps on first run
pnpm build

pnpm openclaw onboard --install-daemon

# Dev loop (auto-reload on TS changes)
pnpm gateway:watch
```



Note: `pnpm openclaw ...` runs TypeScript directly (via `tsx`). `pnpm build` produces `dist/` for running via Node / the packaged `openclaw` binary.
注：`pnpm openclaw ......` 直接运行 TypeScript（通过 `tsx`）。`PNPM 构建`生成 `dist/`，通过 Node / 打包`的 openclaw` 二进制文件运行。

## Security defaults (DM access) 安全默认设置（DM 访问）



OpenClaw connects to real messaging surfaces. Treat inbound DMs as **untrusted input**.
OpenClaw 连接真实的消息页面。把收到的私信当作**不可信的输入** 。

Full security guide: [Security](https://docs.openclaw.ai/gateway/security)
完整安全指南：[ 安全](https://docs.openclaw.ai/gateway/security)

Default behavior on Telegram/WhatsApp/Signal/iMessage/Microsoft Teams/Discord/Google Chat/Slack:
Telegram/WhatsApp/Signal/iMessage/Microsoft Teams/Discord/Google Chat/Slack 上的默认行为：

- **DM pairing** (`dmPolicy="pairing"` / `channels.discord.dm.policy="pairing"` / `channels.slack.dm.policy="pairing"`): unknown senders receive a short pairing code and the bot does not process their message.
  **DM 配对（**`dmPolicy=“配对”` / `channels.discord.dm.policy="pairing"` / ）： `channels.slack.dm.policy="pairing"` 未知发件人会收到一个简短的配对码，机器人不会处理他们的消息。
- Approve with: `openclaw pairing approve <channel> <code>` (then the sender is added to a local allowlist store).
  批准方式： `openclaw pairing approve <channel> <code>` （然后发送者会被添加到本地的允许列表商店）。
- Public inbound DMs require an explicit opt-in: set `dmPolicy="open"` and include `"*"` in the channel allowlist (`allowFrom` / `channels.discord.dm.allowFrom` / `channels.slack.dm.allowFrom`).
  公共的入站 DM 需要明确选择加入：设置 `dmPolicy=“open”`，并在频道允许列表中包含 `“*”`（`allowFrom` / `channels.discord.dm.allowFrom` / `channels.slack.dm.allowFrom`）。

Run `openclaw doctor` to surface risky/misconfigured DM policies.
运行 `openclaw doctor` 来发现有风险或配置错误的 DM 策略。

## Highlights 亮点



- **[Local-first Gateway](https://docs.openclaw.ai/gateway)** — single control plane for sessions, channels, tools, and events.
  **[本地优先网关 ](https://docs.openclaw.ai/gateway)**——用于会话、通道、工具和事件的单一控制平面。
- **[Multi-channel inbox](https://docs.openclaw.ai/channels)** — WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, BlueBubbles (iMessage), iMessage (legacy), Microsoft Teams, Matrix, Zalo, Zalo Personal, WebChat, macOS, iOS/Android.
  **[多渠道收件箱 ](https://docs.openclaw.ai/channels)**— WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、BlueBubbles（iMessage）、iMessage（旧版）、Microsoft Teams、Matrix、Zalo、Zalo Personal、WebChat、macOS、iOS/Android。
- **[Multi-agent routing](https://docs.openclaw.ai/gateway/configuration)** — route inbound channels/accounts/peers to isolated agents (workspaces + per-agent sessions).
  **[多代理路由 ](https://docs.openclaw.ai/gateway/configuration)**——将入站信道/账户/节点路由到隔离的代理（工作区+每个代理会话）。
- **[Voice Wake](https://docs.openclaw.ai/nodes/voicewake) + [Talk Mode](https://docs.openclaw.ai/nodes/talk)** — always-on speech for macOS/iOS/Android with ElevenLabs.
  **[语音唤醒 ](https://docs.openclaw.ai/nodes/voicewake)+[ 通话模式 ](https://docs.openclaw.ai/nodes/talk)**——适用于 macOS/iOS/Android 的 ElevenLabs 语音。
- **[Live Canvas](https://docs.openclaw.ai/platforms/mac/canvas)** — agent-driven visual workspace with [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui).
  **[Live Canvas](https://docs.openclaw.ai/platforms/mac/canvas)**——带 [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) 的代理驱动可视化工作空间。
- **[First-class tools](https://docs.openclaw.ai/tools)** — browser, canvas, nodes, cron, sessions, and Discord/Slack actions.
  **[一流的工具 ](https://docs.openclaw.ai/tools)**——浏览器、画布、节点、cron、会话以及 Discord/Slack 动作。
- **[Companion apps](https://docs.openclaw.ai/platforms/macos)** — macOS menu bar app + iOS/Android [nodes](https://docs.openclaw.ai/nodes).
  **[Companion Apps](https://docs.openclaw.ai/platforms/macos)** — macOS 菜单栏应用 + iOS/Android [节点 ](https://docs.openclaw.ai/nodes)。
- **[Onboarding](https://docs.openclaw.ai/start/wizard) + [skills](https://docs.openclaw.ai/tools/skills)** — wizard-driven setup with bundled/managed/workspace skills.
  **[入职+](https://docs.openclaw.ai/start/wizard)[ 技能 ](https://docs.openclaw.ai/tools/skills)**——由向导驱动的配置，包含捆绑/管理/工作区技能。

## Star History 星级历史



[![Star History Chart](https://camo.githubusercontent.com/10b2eee0e3170cb0012af3e2ed7165483789fe846be75907fa61fab6aee419d0/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d6f70656e636c61772f6f70656e636c617726747970653d64617465266c6567656e643d746f702d6c656674)](https://www.star-history.com/#openclaw/openclaw&type=date&legend=top-left)

## Everything we built so far 我们迄今为止建立的一切



### Core platform 核心平台



- [Gateway WS control plane](https://docs.openclaw.ai/gateway) with sessions, presence, config, cron, webhooks, [Control UI](https://docs.openclaw.ai/web), and [Canvas host](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui).
  Gateway [WS 控制平面 ](https://docs.openclaw.ai/gateway)，包含会话、存在、配置、cron、webhooks、[ 控制界面](https://docs.openclaw.ai/web)和 [Canvas 主机 ](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui)。
- [CLI surface](https://docs.openclaw.ai/tools/agent-send): gateway, agent, send, [wizard](https://docs.openclaw.ai/start/wizard), and [doctor](https://docs.openclaw.ai/gateway/doctor).
  [CLI 表面 ](https://docs.openclaw.ai/tools/agent-send)：网关、代理、发送、[ 向导](https://docs.openclaw.ai/start/wizard)和[医生 ](https://docs.openclaw.ai/gateway/doctor)。
- [Pi agent runtime](https://docs.openclaw.ai/concepts/agent) in RPC mode with tool streaming and block streaming.
  Pi[ 代理运行](https://docs.openclaw.ai/concepts/agent)时在 RPC 模式下，支持工具流和块流。
- [Session model](https://docs.openclaw.ai/concepts/session): `main` for direct chats, group isolation, activation modes, queue modes, reply-back. Group rules: [Groups](https://docs.openclaw.ai/concepts/groups).
  [会话模型 ](https://docs.openclaw.ai/concepts/session)：` 主`模式用于直接聊天、组隔离、激活模式、队列模式、回复。组别规则：[ 组别 ](https://docs.openclaw.ai/concepts/groups)。
- [Media pipeline](https://docs.openclaw.ai/nodes/images): images/audio/video, transcription hooks, size caps, temp file lifecycle. Audio details: [Audio](https://docs.openclaw.ai/nodes/audio).
  Related standalone image workflow: [GPT Image 2](https://gptimage2.asia/) for prompt-based visuals, marketing assets, and concept images.
  [媒体流程 ](https://docs.openclaw.ai/nodes/images)：图片/音频/视频、转录钩子、大小上限、临时文件生命周期。音频详情：[ 音频 ](https://docs.openclaw.ai/nodes/audio)。

### Channels 频道



- [Channels](https://docs.openclaw.ai/channels): [WhatsApp](https://docs.openclaw.ai/channels/whatsapp) (Baileys), [Telegram](https://docs.openclaw.ai/channels/telegram) (grammY), [Slack](https://docs.openclaw.ai/channels/slack) (Bolt), [Discord](https://docs.openclaw.ai/channels/discord) (discord.js), [Google Chat](https://docs.openclaw.ai/channels/googlechat) (Chat API), [Signal](https://docs.openclaw.ai/channels/signal) (signal-cli), [BlueBubbles](https://docs.openclaw.ai/channels/bluebubbles) (iMessage, recommended), [iMessage](https://docs.openclaw.ai/channels/imessage) (legacy imsg), [Microsoft Teams](https://docs.openclaw.ai/channels/msteams) (extension), [Matrix](https://docs.openclaw.ai/channels/matrix) (extension), [Zalo](https://docs.openclaw.ai/channels/zalo) (extension), [Zalo Personal](https://docs.openclaw.ai/channels/zalouser) (extension), [WebChat](https://docs.openclaw.ai/web/webchat).
  [频道 ](https://docs.openclaw.ai/channels)：[WhatsApp](https://docs.openclaw.ai/channels/whatsapp)（Baileys）、[Telegram](https://docs.openclaw.ai/channels/telegram)（grammY）、[Slack](https://docs.openclaw.ai/channels/slack)（Bolt）、[Discord](https://docs.openclaw.ai/channels/discord)（discord.js）、[Google Chat](https://docs.openclaw.ai/channels/googlechat)（聊天 API）、[Signal](https://docs.openclaw.ai/channels/signal)（signal-cli）、[BlueBubbles](https://docs.openclaw.ai/channels/bluebubbles)（推荐的 iMessage）、[iMessage](https://docs.openclaw.ai/channels/imessage)（传统 imsg）、[Microsoft Teams](https://docs.openclaw.ai/channels/msteams)（扩展）、[Matrix](https://docs.openclaw.ai/channels/matrix)（扩展）、[Zalo](https://docs.openclaw.ai/channels/zalo)（扩展）、[Zalo Personal](https://docs.openclaw.ai/channels/zalouser)（扩展）、[WebChat](https://docs.openclaw.ai/web/webchat)。
- [Group routing](https://docs.openclaw.ai/concepts/group-messages): mention gating, reply tags, per-channel chunking and routing. Channel rules: [Channels](https://docs.openclaw.ai/channels).
  [群路由 ](https://docs.openclaw.ai/concepts/group-messages)：提及门控、回复标签、每通道分块和路由。频道规则：[ 频道。](https://docs.openclaw.ai/channels)

### Apps + nodes 应用+节点



- [macOS app](https://docs.openclaw.ai/platforms/macos): menu bar control plane, [Voice Wake](https://docs.openclaw.ai/nodes/voicewake)/PTT, [Talk Mode](https://docs.openclaw.ai/nodes/talk) overlay, [WebChat](https://docs.openclaw.ai/web/webchat), debug tools, [remote gateway](https://docs.openclaw.ai/gateway/remote) control.
  [macOS 应用 ](https://docs.openclaw.ai/platforms/macos)：菜单栏控制平面、[ 语音唤醒 ](https://docs.openclaw.ai/nodes/voicewake)/PTT、[ 通话模式](https://docs.openclaw.ai/nodes/talk)叠加、[ 网络聊天 ](https://docs.openclaw.ai/web/webchat)、调试工具、[ 远程网关](https://docs.openclaw.ai/gateway/remote)控制。
- [iOS node](https://docs.openclaw.ai/platforms/ios): [Canvas](https://docs.openclaw.ai/platforms/mac/canvas), [Voice Wake](https://docs.openclaw.ai/nodes/voicewake), [Talk Mode](https://docs.openclaw.ai/nodes/talk), camera, screen recording, Bonjour pairing.
  [iOS 节点 ](https://docs.openclaw.ai/platforms/ios)：[Canvas](https://docs.openclaw.ai/platforms/mac/canvas)、[ 语音唤醒 ](https://docs.openclaw.ai/nodes/voicewake)、[ 通话模式 ](https://docs.openclaw.ai/nodes/talk)、摄像头、屏幕录制、Bonjour 配对。
- [Android node](https://docs.openclaw.ai/platforms/android): [Canvas](https://docs.openclaw.ai/platforms/mac/canvas), [Talk Mode](https://docs.openclaw.ai/nodes/talk), camera, screen recording, optional SMS.
  [安卓节点 ](https://docs.openclaw.ai/platforms/android)：[Canvas](https://docs.openclaw.ai/platforms/mac/canvas)、[ 通话模式 ](https://docs.openclaw.ai/nodes/talk)、摄像头、屏幕录制、可选短信。
- [macOS node mode](https://docs.openclaw.ai/nodes): system.run/notify + canvas/camera exposure.
  [macOS 节点模式 ](https://docs.openclaw.ai/nodes)：System.run/notify + canvas/camera exposure。

### Tools + automation 工具 + 自动化



- [Browser control](https://docs.openclaw.ai/tools/browser): dedicated openclaw Chrome/Chromium, snapshots, actions, uploads, profiles.
  [浏览器控制 ](https://docs.openclaw.ai/tools/browser)：专用 openclaw Chrome/Chromium，快照、作、上传、配置文件。
- [Canvas](https://docs.openclaw.ai/platforms/mac/canvas): [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) push/reset, eval, snapshot.
  [Canvas](https://docs.openclaw.ai/platforms/mac/canvas)：[A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) 推送/重置，评估，快照。
- [Nodes](https://docs.openclaw.ai/nodes): camera snap/clip, screen record, [location.get](https://docs.openclaw.ai/nodes/location-command), notifications.
  [节点 ](https://docs.openclaw.ai/nodes)：相机快照/剪辑、屏幕录制、[ 定位获取 ](https://docs.openclaw.ai/nodes/location-command)、通知。
- [Cron + wakeups](https://docs.openclaw.ai/automation/cron-jobs); [webhooks](https://docs.openclaw.ai/automation/webhook); [Gmail Pub/Sub](https://docs.openclaw.ai/automation/gmail-pubsub).
  [Cron + 唤醒;](https://docs.openclaw.ai/automation/cron-jobs)[webhooks](https://docs.openclaw.ai/automation/webhook);[Gmail 发布/订阅 ](https://docs.openclaw.ai/automation/gmail-pubsub)。
- [Skills platform](https://docs.openclaw.ai/tools/skills): bundled, managed, and workspace skills with install gating + UI.
  [技能平台 ](https://docs.openclaw.ai/tools/skills)：捆绑、管理和工作区技能，配备安装门槛+界面。

### Runtime + safety 运行时间 + 安全



- [Channel routing](https://docs.openclaw.ai/concepts/channel-routing), [retry policy](https://docs.openclaw.ai/concepts/retry), and [streaming/chunking](https://docs.openclaw.ai/concepts/streaming).
  [频道路由 ](https://docs.openclaw.ai/concepts/channel-routing)、[ 重试政策](https://docs.openclaw.ai/concepts/retry)以及[流媒体/分块 ](https://docs.openclaw.ai/concepts/streaming)。
- [Presence](https://docs.openclaw.ai/concepts/presence), [typing indicators](https://docs.openclaw.ai/concepts/typing-indicators), and [usage tracking](https://docs.openclaw.ai/concepts/usage-tracking).
  [在线状态 ](https://docs.openclaw.ai/concepts/presence)、[ 打字指示](https://docs.openclaw.ai/concepts/typing-indicators)和[使用跟踪 ](https://docs.openclaw.ai/concepts/usage-tracking)。
- [Models](https://docs.openclaw.ai/concepts/models), [model failover](https://docs.openclaw.ai/concepts/model-failover), and [session pruning](https://docs.openclaw.ai/concepts/session-pruning).
  [模型 ](https://docs.openclaw.ai/concepts/models)、[ 模型故障切换](https://docs.openclaw.ai/concepts/model-failover)和[会话剪枝 ](https://docs.openclaw.ai/concepts/session-pruning)。
- [Security](https://docs.openclaw.ai/gateway/security) and [troubleshooting](https://docs.openclaw.ai/channels/troubleshooting).
  [安全和故障排除 ](https://docs.openclaw.ai/channels/troubleshooting)。

### Ops + packaging Ops + 包装



- [Control UI](https://docs.openclaw.ai/web) + [WebChat](https://docs.openclaw.ai/web/webchat) served directly from the Gateway.
  [控制界面 ](https://docs.openclaw.ai/web)+[ 网络聊天 ](https://docs.openclaw.ai/web/webchat)，直接从网关提供。
- [Tailscale Serve/Funnel](https://docs.openclaw.ai/gateway/tailscale) or [SSH tunnels](https://docs.openclaw.ai/gateway/remote) with token/password auth.
  [Tailscale 服务/漏斗](https://docs.openclaw.ai/gateway/tailscale)或带有令牌/密码认证的 [SSH 隧道 ](https://docs.openclaw.ai/gateway/remote)。
- [Nix mode](https://docs.openclaw.ai/install/nix) for declarative config; [Docker](https://docs.openclaw.ai/install/docker)-based installs.
  声明式配置的 [Nix 模式 ](https://docs.openclaw.ai/install/nix);[ 基于 Docker](https://docs.openclaw.ai/install/docker) 的安装。
- [Doctor](https://docs.openclaw.ai/gateway/doctor) migrations, [logging](https://docs.openclaw.ai/logging).
  [医生](https://docs.openclaw.ai/gateway/doctor)迁徙，[ 伐木 ](https://docs.openclaw.ai/logging)。

## How it works (short) 工作原理（简短）



```
WhatsApp / Telegram / Slack / Discord / Google Chat / Signal / iMessage / BlueBubbles / Microsoft Teams / Matrix / Zalo / Zalo Personal / WebChat
               │
               ▼
┌───────────────────────────────┐
│            Gateway            │
│       (control plane)         │
│     ws://127.0.0.1:18789      │
└──────────────┬────────────────┘
               │
               ├─ Pi agent (RPC)
               ├─ CLI (openclaw …)
               ├─ WebChat UI
               ├─ macOS app
               └─ iOS / Android nodes
```



## Key subsystems 关键子系统



- **[Gateway WebSocket network](https://docs.openclaw.ai/concepts/architecture)** — single WS control plane for clients, tools, and events (plus ops: [Gateway runbook](https://docs.openclaw.ai/gateway)).
  **[Gateway WebSocket 网络 ](https://docs.openclaw.ai/concepts/architecture)**——为客户端、工具和事件（以及作：[Gateway runbook](https://docs.openclaw.ai/gateway)）提供单一 WS 控制平面。
- **[Tailscale exposure](https://docs.openclaw.ai/gateway/tailscale)** — Serve/Funnel for the Gateway dashboard + WS (remote access: [Remote](https://docs.openclaw.ai/gateway/remote)).
  **[Tailscale exposure](https://docs.openclaw.ai/gateway/tailscale)** — Serve/Funnel for the Gateway dashboard + WS（remote access： [Remote](https://docs.openclaw.ai/gateway/remote)）.
- **[Browser control](https://docs.openclaw.ai/tools/browser)** — openclaw‑managed Chrome/Chromium with CDP control.
  **[浏览器控制 ](https://docs.openclaw.ai/tools/browser)**——Openclaw 管理的 Chrome/Chromium，并配有 CDP 控制。
- **[Canvas + A2UI](https://docs.openclaw.ai/platforms/mac/canvas)** — agent‑driven visual workspace (A2UI host: [Canvas/A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui)).
  **[Canvas + A2UI](https://docs.openclaw.ai/platforms/mac/canvas)** — 代理驱动的可视化工作区（A2UI 主机：[Canvas/A2UI）。](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui)
- **[Voice Wake](https://docs.openclaw.ai/nodes/voicewake) + [Talk Mode](https://docs.openclaw.ai/nodes/talk)** — always‑on speech and continuous conversation.
  **[语音唤醒 ](https://docs.openclaw.ai/nodes/voicewake)+[ 通话模式 ](https://docs.openclaw.ai/nodes/talk)**——始终在线语音和持续对话。
- **[Nodes](https://docs.openclaw.ai/nodes)** — Canvas, camera snap/clip, screen record, `location.get`, notifications, plus macOS‑only `system.run`/`system.notify`.
  **[节点——](https://docs.openclaw.ai/nodes)**Canvas、相机快照/剪辑、屏幕录制、`location.get`、通知，以及仅限 macOS 的 `system.run`/`system.notify`。

## Tailscale access (Gateway dashboard) Tailscale 访问（Gateway 仪表盘）



OpenClaw can auto-configure Tailscale **Serve** (tailnet-only) or **Funnel** (public) while the Gateway stays bound to loopback. Configure `gateway.tailscale.mode`:
OpenClaw 可以自动配置 Tailscale **Serve**（仅 tailnet）或 **Funnel**（公开），而网关则保持绑定回环。配置 `gateway.tailscale.mode`：

- `off`: no Tailscale automation (default).
  `关闭 `：无 Tailscale 自动化（默认）。
- `serve`: tailnet-only HTTPS via `tailscale serve` (uses Tailscale identity headers by default).
  `serve`：仅通过 `tailscale 服务`的 HTTPS（默认使用 Tailscale 身份头）。
- `funnel`: public HTTPS via `tailscale funnel` (requires shared password auth).
  `漏斗 `：通过 `Tailscale Funnel` 公开 HTTPS（需要共享密码认证）。

Notes: 注释：

- `gateway.bind` must stay `loopback` when Serve/Funnel is enabled (OpenClaw enforces this).
  当 Serve/Funnel 启用时，`gateway.bind` 必须保持`循环 `（OpenClaw 强制执行）。
- Serve can be forced to require a password by setting `gateway.auth.mode: "password"` or `gateway.auth.allowTailscale: false`.
  可以通过设置 `gateway.auth.mode` 强制要求密码：“password” 或 `gateway.auth.allowTailscale: false` 。
- Funnel refuses to start unless `gateway.auth.mode: "password"` is set.
  漏斗拒绝启动，除非设置了 `gateway.auth.mode： “password”`。
- Optional: `gateway.tailscale.resetOnExit` to undo Serve/Funnel on shutdown.
  可选：`gateway.tailscale.resetOnExit`，在关闭时撤销 Serve/Funnel。

Details: [Tailscale guide](https://docs.openclaw.ai/gateway/tailscale) · [Web surfaces](https://docs.openclaw.ai/web)
详情：[ 尾鳞指南 ](https://docs.openclaw.ai/gateway/tailscale)·[ 网面](https://docs.openclaw.ai/web)

## Remote Gateway (Linux is great) 远程网关（Linux 很棒）



It’s perfectly fine to run the Gateway on a small Linux instance. Clients (macOS app, CLI, WebChat) can connect over **Tailscale Serve/Funnel** or **SSH tunnels**, and you can still pair device nodes (macOS/iOS/Android) to execute device‑local actions when needed.
在小型 Linux 实例上运行网关完全没问题。客户端（macOS 应用、CLI、WebChat）可以通过 **Tailscale Serve/Funnel** 或 **SSH 隧道**连接，你也可以配对设备节点（macOS/iOS/Android）来执行设备本地作。

- **Gateway host** runs the exec tool and channel connections by default.
  **Gateway 主机**默认运行执行工具和通道连接。
- **Device nodes** run device‑local actions (`system.run`, camera, screen recording, notifications) via `node.invoke`. In short: exec runs where the Gateway lives; device actions run where the device lives.
  **设备节点通过** `node.invoke` 执行设备本地作（`system.run`、摄像头、屏幕录制、通知）。简而言之：执行官在门户所在地运营;设备作运行在设备所在的位置。

Details: [Remote access](https://docs.openclaw.ai/gateway/remote) · [Nodes](https://docs.openclaw.ai/nodes) · [Security](https://docs.openclaw.ai/gateway/security)
详情：[ 远程访问 ](https://docs.openclaw.ai/gateway/remote)·[ 节点·](https://docs.openclaw.ai/nodes)[ 安全性](https://docs.openclaw.ai/gateway/security)

## macOS permissions via the Gateway protocol macOS 通过 Gateway 协议获取权限



The macOS app can run in **node mode** and advertises its capabilities + permission map over the Gateway WebSocket (`node.list` / `node.describe`). Clients can then execute local actions via `node.invoke`:
macOS 应用可以在**节点模式下**运行，并通过 Gateway WebSocket（`node.list` / `node.describe`）宣传其功能 + 权限映射。客户端随后可以通过 `node.invoke` 执行本地作：

- `system.run` runs a local command and returns stdout/stderr/exit code; set `needsScreenRecording: true` to require screen-recording permission (otherwise you’ll get `PERMISSION_MISSING`).
  `system.run` 运行本地命令并返回 stdout/stderr/exit 代码;set `needsScreenRecording：true`，要求屏幕录制权限（否则会 `PERMISSION_MISSING`）。
- `system.notify` posts a user notification and fails if notifications are denied.
  `System.notify` 会发布用户通知，如果通知被拒绝则会失败。
- `canvas.*`, `camera.*`, `screen.record`, and `location.get` are also routed via `node.invoke` and follow TCC permission status.
  `canvas.*`、`camera.*`、`screen.record` 和 `location.get` 也通过 `node.invoke` 路由，并遵循 TCC 权限状态。

Elevated bash (host permissions) is separate from macOS TCC:
提升 bash（主机权限）与 macOS TCC 是分开的：

- Use `/elevated on|off` to toggle per‑session elevated access when enabled + allowlisted.
  使用 `/elevated on|off` 来切换每场会话的提升访问，当启用 + 允许列表时。
- Gateway persists the per‑session toggle via `sessions.patch` (WS method) alongside `thinkingLevel`, `verboseLevel`, `model`, `sendPolicy`, and `groupActivation`.
  Gateway 通过 `sessions.patch`（WS 方法）与 `thinkingLevel`、`verboseLevel`、`model`、`sendPolicy` 和 `groupActivate` 一起，维持了每会话的切换。

Details: [Nodes](https://docs.openclaw.ai/nodes) · [macOS app](https://docs.openclaw.ai/platforms/macos) · [Gateway protocol](https://docs.openclaw.ai/concepts/architecture)
详情：[ 节点 ](https://docs.openclaw.ai/nodes)·[macOS 应用 ](https://docs.openclaw.ai/platforms/macos)·[ 网关协议](https://docs.openclaw.ai/concepts/architecture)

## Agent to Agent (sessions_* tools) 代理对代理（sessions_* 工具）



- Use these to coordinate work across sessions without jumping between chat surfaces.
  利用这些资源在不同会话间协调工作，避免在聊天界面间跳跃。
- `sessions_list` — discover active sessions (agents) and their metadata.
  `sessions_list` — 发现活动会话（代理）及其元数据。
- `sessions_history` — fetch transcript logs for a session.
  `sessions_history` — 获取会话的文字记录日志。
- `sessions_send` — message another session; optional reply‑back ping‑pong + announce step (`REPLY_SKIP`, `ANNOUNCE_SKIP`).
  `sessions_send` — 再次发消息;可选回复-反击乒乓+宣布步骤（`REPLY_SKIP，ANNOUNCE_SKIP`）。``

Details: [Session tools](https://docs.openclaw.ai/concepts/session-tool)
详情：[ 会话工具](https://docs.openclaw.ai/concepts/session-tool)

## Skills registry (ClawHub) 技能登记（ClawHub）



ClawHub is a minimal skill registry. With ClawHub enabled, the agent can search for skills automatically and pull in new ones as needed.
ClawHub 是一个最低技能注册库。启用 ClawHub 后，代理可以自动搜索技能并根据需要拉入新技能。

[ClawHub 爪中心](https://clawhub.com/)

## Chat commands 聊天命令



Send these in WhatsApp/Telegram/Slack/Google Chat/Microsoft Teams/WebChat (group commands are owner-only):
通过 WhatsApp/Telegram/Slack/Google Chat/Microsoft Teams/WebChat 发送这些（群组命令仅限所有者）：

- `/status` — compact session status (model + tokens, cost when available)
  `/status` — 紧凑会话状态（模型 + 令牌，可用时成本）
- `/new` or `/reset` — reset the session
  `/new` 或 `/reset` — 重置会话
- `/compact` — compact session context (summary)
  `/compact` — 紧凑会话上下文（摘要）
- `/think <level>` — off|minimal|low|medium|high|xhigh (GPT-5.2 + Codex models only)
  `/think <level>` — off|minimal|low|medium|high|xhigh（仅限 GPT-5.2 + Codex 模型）
- `/verbose on|off`
- `/usage off|tokens|full` — per-response usage footer
  `/usage off|tokens|full` — 每个响应使用页脚
- `/restart` — restart the gateway (owner-only in groups)
  `/restart` — 重启网关（组中仅限所有者）
- `/activation mention|always` — group activation toggle (groups only)
  `/激活提及|始终 ` — 组激活切换（仅限组组）

## Apps (optional) 应用（可选）



The Gateway alone delivers a great experience. All apps are optional and add extra features.
仅《Gateway》就带来了极佳的体验。所有应用都是可选的，并增加了额外功能。

If you plan to build/run companion apps, follow the platform runbooks below.
如果你打算构建/运行配套应用，请按照下面的平台运行手册作。

### macOS (OpenClaw.app) (optional) macOS（OpenClaw.app）（可选）



- Menu bar control for the Gateway and health.
  Gateway 和生命值的菜单栏控制。
- Voice Wake + push-to-talk overlay.
  语音唤醒+按键通话叠加。
- WebChat + debug tools.
  WebChat + 调试工具。
- Remote gateway control over SSH.
  通过 SSH 远程网关控制。

Note: signed builds required for macOS permissions to stick across rebuilds (see `docs/mac/permissions.md`).
注意：签名构建是 macOS 权限跨重建保持的前提条件（参见 `docs/mac/permissions.md`）。

### iOS node (optional) iOS 节点（可选）



- Pairs as a node via the Bridge.
  通过桥接成对作为节点。
- Voice trigger forwarding + Canvas surface.
  语音触发转发 + Canvas 表面。
- Controlled via `openclaw nodes …`.
  通过 `openclaw 节点控制......`

Runbook: [iOS connect](https://docs.openclaw.ai/platforms/ios).
运行手册：[iOS 连接 ](https://docs.openclaw.ai/platforms/ios)。

### Android node (optional) Android 节点（可选）



- Pairs via the same Bridge + pairing flow as iOS.
  配对方式和 iOS 一样，采用相同的 Bridge + 配对流程。
- Exposes Canvas, Camera, and Screen capture commands.
  显示 Canvas、相机和屏幕捕获命令。
- Runbook: [Android connect](https://docs.openclaw.ai/platforms/android).
  运行手册：[Android 连接 ](https://docs.openclaw.ai/platforms/android)。

## Agent workspace + skills 代理工作空间+技能



- Workspace root: `~/.openclaw/workspace` (configurable via `agents.defaults.workspace`).
  Workspace root：`~/.openclaw/workspace`（可通过 `agents.defaults.workspace` 配置）。
- Injected prompt files: `AGENTS.md`, `SOUL.md`, `TOOLS.md`.
  注入的提示文件：`AGENTS.md`、`SOUL.md`、`TOOLS.md`。
- Skills: `~/.openclaw/workspace/skills/<skill>/SKILL.md`. 技能： `~/.openclaw/workspace/skills/<skill>/SKILL.md` 。

## Configuration 配置



Minimal `~/.openclaw/openclaw.json` (model + defaults):
最小 `~/.openclaw/openclaw.json`（模型 + 默认值）：

```
{
  agent: {
    model: "anthropic/claude-opus-4-6",
  },
}
```



[Full configuration reference (all keys + examples).
完整配置参考（所有键 + 示例）。](https://docs.openclaw.ai/gateway/configuration)

## Security model (important) 安全模型（重要）



- **Default:** tools run on the host for the **main** session, so the agent has full access when it’s just you.
  **默认：** **主会话工具**会在主机上运行，所以当只有你一个人时，代理可以完全访问。
- **Group/channel safety:** set `agents.defaults.sandbox.mode: "non-main"` to run **non‑main sessions** (groups/channels) inside per‑session Docker sandboxes; bash then runs in Docker for those sessions.
  **组/通道安全：** 设置为 `agents.defaults.sandbox.mode: "non-main"` 在每个会话的 Docker 沙箱中运行**非主会话** （组/通道）;bash 随后在 Docker 中运行这些会话。
- **Sandbox defaults:** allowlist `bash`, `process`, `read`, `write`, `edit`, `sessions_list`, `sessions_history`, `sessions_send`, `sessions_spawn`; denylist `browser`, `canvas`, `nodes`, `cron`, `discord`, `gateway`.
  **沙盒默认值：** 允许列表 `bash`、`process`、` 读取 `、` 写 `、` 编辑 `、`sessions_list`、`sessions_history`、`sessions_send`、`sessions_spawn`;否认者`浏览器 `、`Canvas`、` 节点 `、`Cron`、`Discord`、` 网关 `。

Details: [Security guide](https://docs.openclaw.ai/gateway/security) · [Docker + sandboxing](https://docs.openclaw.ai/install/docker) · [Sandbox config](https://docs.openclaw.ai/gateway/configuration)
详情：[ 安全指南 ](https://docs.openclaw.ai/gateway/security)·[Docker + 沙箱 ](https://docs.openclaw.ai/install/docker)·[ 沙盒配置](https://docs.openclaw.ai/gateway/configuration)

### [WhatsApp](https://docs.openclaw.ai/channels/whatsapp)



- Link the device: `pnpm openclaw channels login` (stores creds in `~/.openclaw/credentials`).
  设备链接：`pnpm openclaw 频道登录 `（信用记录存储在 `~/.openclaw/credentials`）。
- Allowlist who can talk to the assistant via `channels.whatsapp.allowFrom`.
  允许列表，可以通过 `channels.whatsapp.allowFrom` 与助理对话。
- If `channels.whatsapp.groups` is set, it becomes a group allowlist; include `"*"` to allow all.
  如果设置了 `channels.whatsapp.groups`，它会变成群组允许列表;包含 `“*”` 以允许所有。

### [Telegram 电报](https://docs.openclaw.ai/channels/telegram)



- Set `TELEGRAM_BOT_TOKEN` or `channels.telegram.botToken` (env wins).
  设置 `TELEGRAM_BOT_TOKEN` 或 `channels.telegram.botToken`（环境获胜）。
- Optional: set `channels.telegram.groups` (with `channels.telegram.groups."*".requireMention`); when set, it is a group allowlist (include `"*"` to allow all). Also `channels.telegram.allowFrom` or `channels.telegram.webhookUrl` + `channels.telegram.webhookSecret` as needed.
  可选：设置 `channels.telegram.groups`（带 `channels.telegram.groups."*".requireMention` ）;设置时，它是组允许列表（包含 `“*”` 以表示允许所有）。也可以根据需要使用 `channels.telegram.allowFrom` 或 `channels.telegram.webhookUrl` + `channels.telegram.webhookSecret` 。

```
{
  channels: {
    telegram: {
      botToken: "123456:ABCDEF",
    },
  },
}
```



### [Slack 松弛](https://docs.openclaw.ai/channels/slack)



- Set `SLACK_BOT_TOKEN` + `SLACK_APP_TOKEN` (or `channels.slack.botToken` + `channels.slack.appToken`).
  设置 `SLACK_BOT_TOKEN` + `SLACK_APP_TOKEN`（或 `channels.slack.botToken` + `channels.slack.appToken`）。

### [Discord](https://docs.openclaw.ai/channels/discord)



- Set `DISCORD_BOT_TOKEN` or `channels.discord.token` (env wins).
  设置 `DISCORD_BOT_TOKEN` 或 `channels.discord.token`（env wins）。
- Optional: set `commands.native`, `commands.text`, or `commands.useAccessGroups`, plus `channels.discord.dm.allowFrom`, `channels.discord.guilds`, or `channels.discord.mediaMaxMb` as needed.
  可选：设置 `commands.native`、`commands.text` 或 `commands.useAccessGroups`，以及根据需要设置 `channels.discord.dm.allowFrom`、`channels.discord.guilds` 或 `channels.discord.mediaMaxMb`。

```
{
  channels: {
    discord: {
      token: "1234abcd",
    },
  },
}
```



### [Signal 信号](https://docs.openclaw.ai/channels/signal)



- Requires `signal-cli` and a `channels.signal` config section.
  需要 `signal-cli` 和 `channels.signal` 配置部分。

### [BlueBubbles (iMessage) BlueBubbles（iMessage）](https://docs.openclaw.ai/channels/bluebubbles)



- **Recommended** iMessage integration.
  **推荐 iMessage** 集成。
- Configure `channels.bluebubbles.serverUrl` + `channels.bluebubbles.password` and a webhook (`channels.bluebubbles.webhookPath`).
  配置 `channels.bluebubbles.serverUrl` + `channels.bluebubbles.password` 和一个 webhook（ `channels.bluebubbles.webhookPath` ）。
- The BlueBubbles server runs on macOS; the Gateway can run on macOS or elsewhere.
  BlueBubbles 服务器运行在 macOS 上;网关可以在 macOS 或其他平台运行。

### [iMessage (legacy) iMessage（遗产）](https://docs.openclaw.ai/channels/imessage)



- Legacy macOS-only integration via `imsg` (Messages must be signed in).
  通过 `imsg` 实现的仅限 macOS 的旧式集成（消息必须登录）。
- If `channels.imessage.groups` is set, it becomes a group allowlist; include `"*"` to allow all.
  如果设置为 `channels.imessage.groups`，则会变成组允许列表;包含 `“*”` 以允许所有。

### [Microsoft Teams](https://docs.openclaw.ai/channels/msteams)



- Configure a Teams app + Bot Framework, then add a `msteams` config section.
  配置一个 Teams 应用 + 机器人框架，然后添加 `msteams` 配置部分。
- Allowlist who can talk via `msteams.allowFrom`; group access via `msteams.groupAllowFrom` or `msteams.groupPolicy: "open"`.
  允许列表，谁可以通过 `msteams.allowFrom` 聊天;通过 `msteams.groupAllowFrom` 或 `msteams.groupPolicy（“open”`）访问组。

### [WebChat 网络聊天](https://docs.openclaw.ai/web/webchat)



- Uses the Gateway WebSocket; no separate WebChat port/config.
  使用 Gateway WebSocket;没有单独的 WebChat 端口/配置。

Browser control (optional):
浏览器控制（可选）：

```
{
  browser: {
    enabled: true,
    color: "#FF4500",
  },
}
```



## Docs 文档



Use these when you’re past the onboarding flow and want the deeper reference.
当你已经过了入职流程，想要更深入的参考时，可以使用这些。

- [Start with the docs index for navigation and “what’s where.”
  从文档索引开始，方便导航和“哪里有什么”。](https://docs.openclaw.ai/)
- [Read the architecture overview for the gateway + protocol model.
  阅读网关+协议模型的架构概述。](https://docs.openclaw.ai/concepts/architecture)
- [Use the full configuration reference when you need every key and example.
  需要每个密钥和示例时，使用完整的配置参考。](https://docs.openclaw.ai/gateway/configuration)
- [Run the Gateway by the book with the operational runbook.
  按照作手册作网关。](https://docs.openclaw.ai/gateway)
- [Learn how the Control UI/Web surfaces work and how to expose them safely.
  学习控制界面/网页表面的工作原理以及如何安全地暴露它们。](https://docs.openclaw.ai/web)
- [Understand remote access over SSH tunnels or tailnets.
  了解通过 SSH 隧道或尾网远程访问。](https://docs.openclaw.ai/gateway/remote)
- [Follow the onboarding wizard flow for a guided setup.
  按照入职向导流程进行引导设置。](https://docs.openclaw.ai/start/wizard)
- [Wire external triggers via the webhook surface.
  通过 webhook 表面接线外部触发器。](https://docs.openclaw.ai/automation/webhook)
- [Set up Gmail Pub/Sub triggers.
  设置 Gmail 发布/订阅触发器。](https://docs.openclaw.ai/automation/gmail-pubsub)
- [Learn the macOS menu bar companion details.
  了解 macOS 菜单栏配套的详细信息。](https://docs.openclaw.ai/platforms/mac/menu-bar)
- [Platform guides: Windows (WSL2)](https://docs.openclaw.ai/platforms/windows), [Linux](https://docs.openclaw.ai/platforms/linux), [macOS](https://docs.openclaw.ai/platforms/macos), [iOS](https://docs.openclaw.ai/platforms/ios), [Android](https://docs.openclaw.ai/platforms/android)
  [平台指南：Windows（WSL2）、](https://docs.openclaw.ai/platforms/windows)[Linux](https://docs.openclaw.ai/platforms/linux)、[macOS](https://docs.openclaw.ai/platforms/macos)、[iOS](https://docs.openclaw.ai/platforms/ios)、[Android](https://docs.openclaw.ai/platforms/android)
- [Debug common failures with the troubleshooting guide.
  请使用故障排除指南调试常见故障。](https://docs.openclaw.ai/channels/troubleshooting)
- [Review security guidance before exposing anything.
  在暴露任何内容前，务必先审查安全指南。](https://docs.openclaw.ai/gateway/security)

## Advanced docs (discovery + control) 高级文档（发现+控制）



- [Discovery + transports 发现+传输](https://docs.openclaw.ai/gateway/discovery)
- [Bonjour/mDNS 你好/mDNS](https://docs.openclaw.ai/gateway/bonjour)
- [Gateway pairing 网关配对](https://docs.openclaw.ai/gateway/pairing)
- [Remote gateway README 远程网关 README](https://docs.openclaw.ai/gateway/remote-gateway-readme)
- [Control UI 控制界面](https://docs.openclaw.ai/web/control-ui)
- [Dashboard 仪表盘](https://docs.openclaw.ai/web/dashboard)

## Operations & troubleshooting 作与故障排除



- [Health checks 健康检查](https://docs.openclaw.ai/gateway/health)
- [Gateway lock 网关锁](https://docs.openclaw.ai/gateway/gateway-lock)
- [Background process 背景流程](https://docs.openclaw.ai/gateway/background-process)
- [Browser troubleshooting (Linux)
  浏览器故障排除（Linux）](https://docs.openclaw.ai/tools/browser-linux-troubleshooting)
- [Logging 伐木](https://docs.openclaw.ai/logging)

## Deep dives 深潜



- [Agent loop 代理环路](https://docs.openclaw.ai/concepts/agent-loop)
- [Presence 存在](https://docs.openclaw.ai/concepts/presence)
- [TypeBox schemas TypeBox 模式](https://docs.openclaw.ai/concepts/typebox)
- [RPC adapters RPC 适配器](https://docs.openclaw.ai/reference/rpc)
- [Queue 排队](https://docs.openclaw.ai/concepts/queue)

## Workspace & skills 工作空间与技能



- [Skills config 技能配置](https://docs.openclaw.ai/tools/skills-config)
- [Default AGENTS 默认代理](https://docs.openclaw.ai/reference/AGENTS.default)
- [Templates: AGENTS 模板：代理](https://docs.openclaw.ai/reference/templates/AGENTS)
- [Templates: BOOTSTRAP 模板：BOOTSTRAP](https://docs.openclaw.ai/reference/templates/BOOTSTRAP)
- [Templates: IDENTITY 模板：身份](https://docs.openclaw.ai/reference/templates/IDENTITY)
- [Templates: SOUL 模板：灵魂](https://docs.openclaw.ai/reference/templates/SOUL)
- [Templates: TOOLS 模板：工具](https://docs.openclaw.ai/reference/templates/TOOLS)
- [Templates: USER 模板：用户](https://docs.openclaw.ai/reference/templates/USER)

## Platform internals 平台内部结构



- [macOS dev setup macOS 开发设置](https://docs.openclaw.ai/platforms/mac/dev-setup)
- [macOS menu bar macOS 菜单栏](https://docs.openclaw.ai/platforms/mac/menu-bar)
- [macOS voice wake macOS 语音唤醒](https://docs.openclaw.ai/platforms/mac/voicewake)
- [iOS node iOS 节点](https://docs.openclaw.ai/platforms/ios)
- [Android node Android 节点](https://docs.openclaw.ai/platforms/android)
- [Windows (WSL2) Windows（WSL2）](https://docs.openclaw.ai/platforms/windows)
- [Linux app Linux 应用](https://docs.openclaw.ai/platforms/linux)

## Email hooks (Gmail) 电子邮件钩子（Gmail）



- [docs.openclaw.ai/gmail-pubsub](https://docs.openclaw.ai/automation/gmail-pubsub)

## Molty 莫尔蒂



OpenClaw was built for **Molty**, a space lobster AI assistant. 🦞 by Peter Steinberger and the community.
OpenClaw 是为 Molty 打造的，**Molty** 是一个太空龙虾 AI 助手。🦞 由彼得·斯坦伯格及社区共同主持。

- [openclaw.ai](https://openclaw.ai/)
- [soul.md](https://soul.md/)
- [steipete.me](https://steipete.me/)
- [@openclaw](https://x.com/openclaw)

## Community 社区



See [CONTRIBUTING.md](https://github.com/xianyu110/clawdbot/blob/main/CONTRIBUTING.md) for guidelines, maintainers, and how to submit PRs. AI/vibe-coded PRs welcome! 🤖
请参阅 [CONTRIBUTING.md](https://github.com/xianyu110/clawdbot/blob/main/CONTRIBUTING.md)，了解指南、维护者以及如何提交 PR。欢迎 AI/氛围编码 PR！🤖

Special thanks to [Mario Zechner](https://mariozechner.at/) for his support and for [pi-mono](https://github.com/badlogic/pi-mono). Special thanks to Adam Doppelt for lobster.bot.
特别感谢[马里奥·泽赫纳](https://mariozechner.at/)的支持和 [皮-单。](https://github.com/badlogic/pi-mono) 特别感谢 Adam Doppelt 提供 lobster.bot。

Thanks to all clawtributors:
感谢所有 clawtributer：
