# anthropic-new-rule · S3 打样三镜

风格验收字卡样片（无 A-roll）。皮肤 `ui-demo`，palette 见 `config/anthropic-new-rule/sample.json`。

**成片 mp4 不进 git**，挂在 GitHub Release：[`anthropic-new-rule-s3-samples`](https://github.com/GZ-L/pdf-oral-motion/releases/tag/anthropic-new-rule-s3-samples)

| 文件 | 时长 | 下载 | 字卡 / 元素 |
|---|---|---|---|
| `s00.mp4` | ~10s | [下载](https://github.com/GZ-L/pdf-oral-motion/releases/download/anthropic-new-rule-s3-samples/s00.mp4) | 小字「全片 AI 制作」；大标题「Anthropic 出了条新规」(accent)；caption「AI 做的片 · 但不聊制作 → 新规」 |
| `s11.mp4` | ~11s | [下载](https://github.com/GZ-L/pdf-oral-motion/releases/download/anthropic-new-rule-s3-samples/s11.mp4) | 双卡：日期（card-A）+ 核心条款（card-B）；高亮「持续」「无必要」 |
| `s41.mp4` | ~14s | [下载](https://github.com/GZ-L/pdf-oral-motion/releases/download/anthropic-new-rule-s3-samples/s41.mp4) | 示意双按钮 A/B；数字 0%→75%→94%；限制小字 hold≥2s |
| `sample-reel.mp4` | ~35s | [下载](https://github.com/GZ-L/pdf-oral-motion/releases/download/anthropic-new-rule-s3-samples/sample-reel.mp4) | 上三镜顺序拼接 |

## 缺什么
- **A-roll**（真人/口播画面）未进样片；本批仅验风格/节奏/字幕安全区。
- 官方截图、产品真实 UI 未用；按钮为「描述性按钮」示意卡。
- 音轨无（纯画面打样）。

## 验收看什么
1. **Palette**：bg `#0B0D10` / surface `#161A22` / text `#F4F6FA` / accent `#C8FF3D` / warn `#FFD166` / border `#2A3140`
2. **字幕安全区**：底部 15% 内无关键标题/大数字；caption 贴安全区上沿
3. **节奏**：s00 四段（小字→zoom→hold→淡出）；s11 hold≥1.5s 可读；s41 限制小字 hold≥2s
4. **护栏**：Pain Axis 不说「模型真的疼」；带条件小字；无黄白人设

## 规格
1920×1080 · 16:9 · H.264 · yuv420p · 30fps
