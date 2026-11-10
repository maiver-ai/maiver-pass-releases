# MAIVER PASS

MAIVER PASS 的公开安装包与签名更新清单仓库。业务源码保持私有，此仓库不包含账号或用户数据。

## 下载与安装

前往 [Releases](https://github.com/maiver-ai/maiver-pass-releases/releases/latest) 下载适合本机架构的 DMG。打开后将 MAIVER PASS 拖入 Applications，再从 Applications 启动。当前提供 Apple Silicon（arm64）版本，验证环境为 macOS 15.7.9。

首次使用需要管理员提供的 MAIVER 账号，Agent CLI 需另行安装。

## 应用内更新

0.6.1 起，在“设置 → 软件更新”点击“检查更新”，确认新版本后下载并安装。更新包会验证签名及签名绑定的版本号，随后停止本地 SDK、安装并重启。请先暂停 Agent 工具调用。旧版 0.6.0 没有更新器，需要手动安装一次。

固定更新入口：[latest.json](https://github.com/maiver-ai/maiver-pass-releases/releases/latest/download/latest.json)。更新不需要 GitHub 账号或令牌。

账号、设备身份和待上传队列保留。自动迁移仅针对已登记且内容未被修改的接线；Agent 可能需要重启，Codex 可能需要重新审查 /hooks 信任。

## 文件说明

- `.dmg`：首次安装。
- `.app.tar.gz` 与 `.sig`：应用内更新与签名。
- `latest.json`：当前版本、说明和按架构选择的下载地址。
- `SHA256SUMS`：下载文件摘要。
- `release-manifest.json`：构建版本及源码基线信息。

更新签名公钥见 [updater.pub](updater.pub)。私钥不在此仓库和安装包中。

## 当前分发状态

当前版本为受控测试/公开预览版本，尚未使用 Apple Developer ID 签名或完成 Apple 公证。更新包签名与 Apple 公证是不同的机制，浏览器下载后可能被 macOS Gatekeeper 拦截。具体限制以各 Release 说明为准。

发布包可能来自有未提交更改的私有工作区，请查看每个版本的 release-manifest.json；不要将本分发仓库标签误认为业务源码的完整版本快照。
