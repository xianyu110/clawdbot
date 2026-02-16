# 仓库指南

- 仓库：https://github.com/openclaw/openclaw
- GitHub issues/评论/PR 评论：使用字面多行字符串或 `-F - <<'EOF'`（或 `$'...'`）来实现真正的换行；永远不要嵌入 "\\n"。

## 项目结构与模块组织

- 源代码：`src/`（CLI 连接在 `src/cli`，命令在 `src/commands`，web 提供者在 `src/provider-web.ts`，基础设施在 `src/infra`，媒体管道在 `src/media`）。
- 测试：同位置的 `*.test.ts`。
- 文档：`docs/`（图片、队列、Pi 配置）。构建输出位于 `dist/`。
- 插件/扩展：位于 `extensions/*`（工作区包）。将仅插件使用的依赖保留在扩展的 `package.json` 中；除非核心使用它们，否则不要将它们添加到根 `package.json`。
- 插件：安装时在插件目录运行 `npm install --omit=dev`；运行时依赖必须位于 `dependencies` 中。避免在 `dependencies` 中使用 `workspace:*`（npm install 会中断）；将 `openclaw` 放在 `devDependencies` 或 `peerDependencies` 中（运行时通过 jiti 别名解析 `openclaw/plugin-sdk`）。
- 从 `https://openclaw.ai/*` 提供的安装程序：位于同级仓库 `../openclaw.ai`（`public/install.sh`、`public/install-cli.sh`、`public/install.ps1`）。
- 消息通道：重构共享逻辑（路由、白名单、配对、命令门控、入门、文档）时，始终考虑**所有**内置 + 扩展通道。
  - 核心通道文档：`docs/channels/`
  - 核心通道代码：`src/telegram`、`src/discord`、`src/slack`、`src/signal`、`src/imessage`、`src/web`（WhatsApp web）、`src/channels`、`src/routing`
  - 扩展（通道插件）：`extensions/*`（例如 `extensions/msteams`、`extensions/matrix`、`extensions/zalo`、`extensions/zalouser`、`extensions/voice-call`）
- 添加通道/扩展/应用/文档时，更新 `.github/labeler.yml` 并创建匹配的 GitHub 标签（使用现有通道/扩展标签颜色）。

## 文档链接（Mintlify）

- 文档托管在 Mintlify（docs.openclaw.ai）。
- `docs/**/*.md` 中的内部文档链接：根相对路径，不带 `.md`/`.mdx`（示例：`[Config](/configuration)`）。
- 处理文档时，阅读 mintlify skill。
- 章节交叉引用：在根相对路径上使用锚点（示例：`[Hooks](/configuration#hooks)`）。
- 文档标题和锚点：避免在标题中使用破折号和撇号，因为它们会破坏 Mintlify 锚点链接。
- 当 Peter 询问链接时，回复完整的 `https://docs.openclaw.ai/...` URL（不是根相对路径）。
- 当你修改文档时，在回复末尾附上你引用的 `https://docs.openclaw.ai/...` URL。
- README（GitHub）：保留绝对文档 URL（`https://docs.openclaw.ai/...`），以便链接在 GitHub 上正常工作。
- 文档内容必须是通用的：不要使用个人设备名称/主机名/路径；使用占位符，如 `user@gateway-host` 和 "gateway host"。

## 文档国际化（zh-CN）

- `docs/zh-CN/**` 是生成的；除非用户明确要求，否则不要编辑。
- 流程：更新英文文档 → 调整词汇表（`docs/.i18n/glossary.zh-CN.json`）→ 运行 `scripts/docs-i18n` → 仅在指示时应用针对性修复。
- 翻译记忆：`docs/.i18n/zh-CN.tm.jsonl`（生成的）。
- 参见 `docs/.i18n/README.md`。
- 该流程可能很慢/低效；如果拖延，请在 Discord 上联系 @jospalmbier，而不是绕过它。

## exe.dev VM 操作（通用）

- 访问：稳定路径是 `ssh exe.dev` 然后 `ssh vm-name`（假设 SSH 密钥已设置）。
- SSH 不稳定：使用 exe.dev web 终端或 Shelley（web 代理）；为长时间操作保持 tmux 会话。
- 更新：`sudo npm i -g openclaw@latest`（全局安装需要 `/usr/lib/node_modules` 的 root 权限）。
- 配置：使用 `openclaw config set ...`；确保设置了 `gateway.mode=local`。
- Discord：仅存储原始令牌（不带 `DISCORD_BOT_TOKEN=` 前缀）。
- 重启：停止旧网关并运行：
  `pkill -9 -f openclaw-gateway || true; nohup openclaw gateway run --bind loopback --port 18789 --force > /tmp/openclaw-gateway.log 2>&1 &`
- 验证：`openclaw channels status --probe`、`ss -ltnp | rg 18789`、`tail -n 120 /tmp/openclaw-gateway.log`。

## 构建、测试和开发命令

- 运行时基线：Node **22+**（保持 Node + Bun 路径正常工作）。
- 安装依赖：`pnpm install`
- 如果缺少依赖（例如 `node_modules` 缺失、`vitest not found` 或 `command not found`），运行仓库的包管理器安装命令（优先使用锁文件/README 定义的 PM），然后重新运行确切请求的命令一次。将此应用于测试/构建/lint/类型检查/开发命令；如果重试仍然失败，报告命令和第一个可操作的错误。
- 预提交钩子：`prek install`（运行与 CI 相同的检查）
- 也支持：`bun install`（在修改依赖/补丁时保持 `pnpm-lock.yaml` + Bun 补丁同步）。
- 优先使用 Bun 执行 TypeScript（脚本、开发、测试）：`bun <file.ts>` / `bunx <tool>`。
- 在开发中运行 CLI：`pnpm openclaw ...`（bun）或 `pnpm dev`。
- Node 仍然支持运行构建输出（`dist/*`）和生产安装。
- Mac 打包（开发）：`scripts/package-mac-app.sh` 默认为当前架构。发布清单：`docs/platforms/mac/release.md`。
- 类型检查/构建：`pnpm build`
- TypeScript 检查：`pnpm tsgo`
- Lint/格式化：`pnpm check`
- 格式检查：`pnpm format`（oxfmt --check）
- 格式修复：`pnpm format:fix`（oxfmt --write）
- 测试：`pnpm test`（vitest）；覆盖率：`pnpm test:coverage`

## 编码风格与命名约定

- 语言：TypeScript（ESM）。优先使用严格类型；避免 `any`。
- 通过 Oxlint 和 Oxfmt 进行格式化/linting；在提交前运行 `pnpm check`。
- 为棘手或不明显的逻辑添加简短的代码注释。
- 保持文件简洁；提取辅助函数而不是 "V2" 副本。使用现有模式进行 CLI 选项和通过 `createDefaultDeps` 进行依赖注入。
- 目标是将文件保持在约 700 行代码以下；仅作为指导（不是硬性限制）。当它提高清晰度或可测试性时进行拆分/重构。
- 命名：在产品/应用/文档标题中使用 **OpenClaw**；在 CLI 命令、包/二进制文件、路径和配置键中使用 `openclaw`。

## 发布渠道（命名）

- stable：仅标记的发布（例如 `vYYYY.M.D`），npm dist-tag `latest`。
- beta：预发布标签 `vYYYY.M.D-beta.N`，npm dist-tag `beta`（可能在没有 macOS 应用的情况下发布）。
- dev：在 `main` 上移动头部（无标签；git checkout main）。

## 测试指南

- 框架：Vitest，V8 覆盖率阈值（70% 行/分支/函数/语句）。
- 命名：使用 `*.test.ts` 匹配源名称；e2e 在 `*.e2e.test.ts` 中。
- 在修改逻辑时推送前运行 `pnpm test`（或 `pnpm test:coverage`）。
- 不要将测试工作者设置为超过 16；已经尝试过了。
- 实时测试（真实密钥）：`CLAWDBOT_LIVE_TEST=1 pnpm test:live`（仅 OpenClaw）或 `LIVE=1 pnpm test:live`（包括提供者实时测试）。Docker：`pnpm test:docker:live-models`、`pnpm test:docker:live-gateway`。入门 Docker E2E：`pnpm test:docker:onboard`。
- 完整套件 + 覆盖内容：`docs/testing.md`。
- 变更日志：仅用户可见的更改；没有内部/元注释（版本对齐、appcast 提醒、发布流程）。
- 纯测试添加/修复通常**不需要**变更日志条目，除非它们改变用户可见的行为或用户要求添加。
- 移动端：在使用模拟器之前，检查连接的真实设备（iOS + Android）并在可用时优先使用它们。

## 提交与拉取请求指南

**完整维护者 PR 工作流（可选）：** 如果你想要仓库的端到端维护者工作流（分类顺序、质量标准、rebase 规则、提交/变更日志约定、共同贡献者政策以及 `review-pr` > `prepare-pr` > `merge-pr` 流程），请参见 `.agents/skills/PR_WORKFLOW.md`。维护者可以使用其他工作流；当维护者指定工作流时，遵循该工作流。如果未指定工作流，默认使用 PR_WORKFLOW。

- 使用 `scripts/committer "<msg>" <file...>` 创建提交；避免手动 `git add`/`git commit`，以便暂存保持范围。
- 遵循简洁、面向行动的提交消息（例如，`CLI: add verbose flag to send`）。
- 分组相关更改；避免捆绑不相关的重构。
- 提交 PR 时阅读此内容：`docs/help/submitting-a-pr.md`（[提交 PR](https://docs.openclaw.ai/help/submitting-a-pr)）
- 提交问题时阅读此内容：`docs/help/submitting-an-issue.md`（[提交问题](https://docs.openclaw.ai/help/submitting-an-issue)）

## 简写命令

- `sync`：如果工作树是脏的，提交所有更改（选择一个合理的 Conventional Commit 消息），然后 `git pull --rebase`；如果 rebase 冲突且无法解决，停止；否则 `git push`。

## Git 注意事项

- 如果 `git branch -d/-D <branch>` 被策略阻止，直接删除本地引用：`git update-ref -d refs/heads/<branch>`。

## 安全与配置提示

- Web 提供者将凭据存储在 `~/.openclaw/credentials/`；如果注销，重新运行 `openclaw login`。
- Pi 会话默认位于 `~/.openclaw/sessions/` 下；基本目录不可配置。
- 环境变量：参见 `~/.profile`。
- 永远不要提交或发布真实的电话号码、视频或实时配置值。在文档、测试和示例中使用明显虚假的占位符。
- 发布流程：在任何发布工作之前，始终阅读 `docs/reference/RELEASING.md` 和 `docs/platforms/mac/release.md`；一旦这些文档回答了问题，就不要问常规问题。

## 故障排除

- 品牌重塑/迁移问题或旧配置/服务警告：运行 `openclaw doctor`（参见 `docs/gateway/doctor.md`）。

## 代理特定注意事项

- 词汇："makeup" = "mac app"。
- 永远不要编辑 `node_modules`（全局/Homebrew/npm/git 安装也是如此）。更新会覆盖。技能注释放在 `tools.md` 或 `AGENTS.md` 中。
- 在仓库中的任何地方添加新的 `AGENTS.md` 时，还要添加一个指向它的 `CLAUDE.md` 符号链接（示例：`ln -s AGENTS.md CLAUDE.md`）。
- Signal："update fly" => `fly ssh console -a flawd-bot -C "bash -lc 'cd /data/clawd/openclaw && git pull --rebase origin main'"` 然后 `fly machines restart e825232f34d058 -a flawd-bot`。
- 处理 GitHub Issue 或 PR 时，在任务结束时打印完整的 URL。
- 回答问题时，仅回复高置信度的答案：在代码中验证；不要猜测。
- 永远不要更新 Carbon 依赖。
- 任何具有 `pnpm.patchedDependencies` 的依赖必须使用精确版本（不带 `^`/`~`）。
- 修补依赖（pnpm 补丁、覆盖或供应商更改）需要明确批准；默认情况下不要这样做。
- CLI 进度：使用 `src/cli/progress.ts`（`osc-progress` + `@clack/prompts` spinner）；不要手工制作 spinner/bar。
- 状态输出：保持表格 + ANSI 安全包装（`src/terminal/table.ts`）；`status --all` = 只读/可粘贴，`status --deep` = 探测。
- 网关当前仅作为菜单栏应用运行；没有安装单独的 LaunchAgent/helper 标签。通过 OpenClaw Mac 应用或 `scripts/restart-mac.sh` 重启；要验证/终止，使用 `launchctl print gui/$UID | grep openclaw` 而不是假设固定标签。**在 macOS 上调试时，通过应用启动/停止网关，而不是临时 tmux 会话；在交接前终止任何临时隧道。**
- macOS 日志：使用 `./scripts/clawlog.sh` 查询 OpenClaw 子系统的统一日志；它支持跟踪/尾部/类别过滤器，并期望 `/usr/bin/log` 的无密码 sudo。
- 如果本地有共享护栏，请查看它们；否则遵循此仓库的指导。
- SwiftUI 状态管理（iOS/macOS）：优先使用 `Observation` 框架（`@Observable`、`@Bindable`）而不是 `ObservableObject`/`@StateObject`；除非兼容性需要，否则不要引入新的 `ObservableObject`，并在修改相关代码时迁移现有用法。
- 连接提供者：添加新连接时，更新每个 UI 界面和文档（macOS 应用、web UI、移动端（如果适用）、入门/概述文档）并添加匹配的状态 + 配置表单，以便提供者列表和设置保持同步。
- 版本位置：`package.json`（CLI）、`apps/android/app/build.gradle.kts`（versionName/versionCode）、`apps/ios/Sources/Info.plist` + `apps/ios/Tests/Info.plist`（CFBundleShortVersionString/CFBundleVersion）、`apps/macos/Sources/OpenClaw/Resources/Info.plist`（CFBundleShortVersionString/CFBundleVersion）、`docs/install/updating.md`（固定的 npm 版本）、`docs/platforms/mac/release.md`（APP_VERSION/APP_BUILD 示例）、Peekaboo Xcode 项目/Info.plists（MARKETING_VERSION/CURRENT_PROJECT_VERSION）。
- "到处升级版本" 意味着上述所有版本位置**除了** `appcast.xml`（仅在发布新的 macOS Sparkle 版本时触碰 appcast）。
- **重启应用：** "重启 iOS/Android 应用" 意味着重建（重新编译/安装）并重新启动，而不仅仅是终止/启动。
- **设备检查：** 在测试之前，在使用模拟器/仿真器之前验证连接的真实设备（iOS/Android）。
- iOS Team ID 查找：`security find-identity -p codesigning -v` → 使用 Apple Development (…) TEAMID。后备：`defaults read com.apple.dt.Xcode IDEProvisioningTeamIdentifiers`。
- A2UI bundle hash：`src/canvas-host/a2ui/.bundle.hash` 是自动生成的；忽略意外更改，仅在需要时通过 `pnpm canvas:a2ui:bundle`（或 `scripts/bundle-a2ui.sh`）重新生成。将哈希作为单独的提交提交。
- 发布签名/公证密钥在仓库外管理；遵循内部发布文档。
- 公证身份验证环境变量（`APP_STORE_CONNECT_ISSUER_ID`、`APP_STORE_CONNECT_KEY_ID`、`APP_STORE_CONNECT_API_KEY_P8`）预期在你的环境中（根据内部发布文档）。
- **多代理安全：** 除非明确请求，否则**不要**创建/应用/删除 `git stash` 条目（这包括 `git pull --rebase --autostash`）。假设其他代理可能正在工作；保持不相关的 WIP 不变，避免跨领域的状态更改。
- **多代理安全：** 当用户说 "push" 时，你可以 `git pull --rebase` 来集成最新更改（永远不要丢弃其他代理的工作）。当用户说 "commit" 时，仅限于你的更改。当用户说 "commit all" 时，以分组块提交所有内容。
- **多代理安全：** 除非明确请求，否则**不要**创建/删除/修改 `git worktree` 检出（或编辑 `.worktrees/*`）。
- **多代理安全：** 除非明确请求，否则**不要**切换分支/检出不同的分支。
- **多代理安全：** 只要每个代理都有自己的会话，运行多个代理就可以。
- **多代理安全：** 当你看到无法识别的文件时，继续；专注于你的更改并仅提交这些更改。
- Lint/格式化流失：
  - 如果暂存+未暂存的差异仅是格式化，自动解决而不询问。
  - 如果已经请求提交/推送，自动暂存并在同一提交中包含仅格式化的后续操作（或在需要时进行一个小的后续提交），无需额外确认。
  - 仅在更改是语义的（逻辑/数据/行为）时询问。
- Lobster seam：在 `src/terminal/palette.ts` 中使用共享的 CLI 调色板（没有硬编码的颜色）；根据需要将调色板应用于入门/配置提示和其他 TTY UI 输出。
- **多代理安全：** 专注于你的编辑报告；除非真正被阻止，否则避免护栏免责声明；当多个代理触碰同一文件时，如果安全则继续；仅在相关时以简短的 "存在其他文件" 注释结束。
- Bug 调查：在得出结论之前，阅读相关 npm 依赖的源代码和所有相关的本地代码；目标是高置信度的根本原因。
- 代码风格：为棘手的逻辑添加简短的注释；在可行时将文件保持在约 500 行代码以下（根据需要拆分/重构）。
- 工具模式护栏（google-antigravity）：避免在工具输入模式中使用 `Type.Union`；没有 `anyOf`/`oneOf`/`allOf`。对字符串列表使用 `stringEnum`/`optionalStringEnum`（Type.Unsafe enum），并使用 `Type.Optional(...)` 而不是 `... | null`。将顶级工具模式保持为 `type: "object"` 和 `properties`。
- 工具模式护栏：避免在工具模式中使用原始 `format` 属性名称；一些验证器将 `format` 视为保留关键字并拒绝模式。
- 当被要求打开 "session" 文件时，打开 `~/.openclaw/agents/<agentId>/sessions/*.jsonl` 下的 Pi 会话日志（使用系统提示的 Runtime 行中的 `agent=<id>` 值；除非给出特定 ID，否则为最新的），而不是默认的 `sessions.json`。如果需要来自另一台机器的日志，通过 Tailscale SSH 并在那里读取相同的路径。
- 不要通过 SSH 重建 macOS 应用；重建必须直接在 Mac 上运行。
- 永远不要向外部消息界面（WhatsApp、Telegram）发送流式/部分回复；只有最终回复应该在那里传递。流式/工具事件可能仍然会发送到内部 UI/控制通道。
- 语音唤醒转发提示：
  - 命令模板应保持为 `openclaw-mac agent --message "${text}" --thinking low`；`VoiceWakeForwarder` 已经对 `${text}` 进行了 shell 转义。不要添加额外的引号。
  - launchd PATH 是最小的；确保应用的启动代理 PATH 包括标准系统路径加上你的 pnpm bin（通常是 `$HOME/Library/pnpm`），以便在通过 `openclaw-mac` 调用时 `pnpm`/`openclaw` 二进制文件可以解析。
- 对于包含 `!` 的手动 `openclaw message send` 消息，使用下面提到的 heredoc 模式以避免 Bash 工具的转义。
- 发布护栏：未经操作员明确同意，不要更改版本号；在运行任何 npm publish/release 步骤之前，始终请求许可。

## NPM + 1Password（发布/验证）

- 使用 1password skill；所有 `op` 命令必须在新的 tmux 会话中运行。
- 登录：`eval "$(op signin --account my.1password.com)"`（应用已解锁 + 集成已开启）。
- OTP：`op read 'op://Private/Npmjs/one-time password?attribute=otp'`。
- 发布：`npm publish --access public --otp="<otp>"`（从包目录运行）。
- 在没有本地 npmrc 副作用的情况下验证：`npm view <pkg> version --userconfig "$(mktemp)"`。
- 发布后终止 tmux 会话。
