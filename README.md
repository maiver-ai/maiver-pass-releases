# MAIVER PASS

MAIVER PASS 的公开安装包与签名更新清单仓库。业务源码保持私有。

## 下载与安装

前往 [Releases](https://github.com/maiver-ai/maiver-pass-releases/releases/latest) 下载 DMG，将 MAIVER PASS 拖入 Applications，再从 Applications 启动。当前提供 Apple Silicon（arm64）版本，验证环境为 macOS 15.7.9。

macOS 安装提醒：此发布版 DMG 文件目前未经签名。首次运行时，macOS 会将其拦截。请前往“系统设置” > “隐私与安全性”，然后点击“仍要打开”以允许运行。

首次使用需要管理员提供的 MAIVER 账号；Agent CLI 需另行安装。

## 应用内更新

从 0.6.1 起，在“设置 → 软件更新”点击“检查更新”。发现更高版本后可下载、验证签名、安装并重启。0.6.0 用户需要先手动安装一次。相同版本号的重新打包不会触发自动更新。

固定更新入口：[latest.json](https://github.com/maiver-ai/maiver-pass-releases/releases/latest/download/latest.json)。检查与下载不需要 GitHub 账号或令牌。更新前请暂停 Agent 调用。

## 附件与校验

- `.dmg`：首次安装。
- `.app.tar.gz` 与 `.sig`：自动更新包及签名。
- `latest.json`：版本、说明、下载地址和签名。
- `SHA256SUMS`：发行附件摘要。
- `release-manifest.json`：构建与源码基线记录。
- `RELEASE_NOTES.md`：发布说明。

只下载 DMG 时，执行 `shasum -a 256 MAIVER-PASS-0.6.1-macos-arm64.dmg`，与 SHA256SUMS 对应行比较。全部附件下载后可执行 `shasum -a 256 -c SHA256SUMS`。

更新签名公钥见 [updater.pub](updater.pub)。当前为公开预览版，尚无 Apple Developer ID 签名或 Apple 公证，更新签名不能替代 Apple 公证。分发仓库标签仅标识二进制版本，不是业务源码的完整快照。
