# MAIVER PASS

MAIVER PASS 的公开安装包分发仓库。业务源码保持私有。

## 下载与安装

前往 [Releases](https://github.com/maiver-ai/maiver-pass-releases/releases/latest) 下载 DMG，将 MAIVER PASS 拖入 Applications，再从 Applications 启动。当前提供 Apple Silicon（arm64）版本，验证环境为 macOS 15.7.9。

macOS 安装提醒：此发布版 DMG 文件目前未经签名。首次运行时，macOS 会将其拦截。请前往“系统设置” > “隐私与安全性”，然后点击“仍要打开”以允许运行。

首次使用需要管理员提供的 MAIVER 账号；Agent CLI 需另行安装。

## 校验与后续更新

Release 仅提供 `.dmg` 和 `SHA256SUMS`。下载两者后，在下载目录运行：

```bash
shasum -a 256 -c SHA256SUMS
```

后续版本请从 Releases 下载新版 DMG 手动安装。目前不发布自动更新清单或更新包，应用内“检查更新”暂不可用。

当前为公开预览版，尚无 Apple Developer ID 签名或 Apple 公证。分发仓库标签仅标识二进制版本，不是业务源码的完整快照。
