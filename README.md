# pdf-oral-motion

果汁旗舰流水线：**PDF / 提纲 → 口播动效成片**（16:9 横版为主，可选竖切）。

这是一条可从头跑到尾的工作流仓（B/C），不是 Skill 合集。目标：打样定 config → 下次只换文案量产。

## 怎么跑通（最短路径）

1. **放输入** → `input/<slug>/outline.yaml`（或 `source.pdf` + 由文档台转成提纲）
2. **过门禁** → 对照 `schemas/outline.schema.yaml`（title / hook / ≥2 chapters）
3. **分镜** → `storyboard/<slug>/shots.md`（每镜强制 `lens` 等字段，见 schemas）
4. **动效轨** → `motion/<slug>/timeline.md`（Seedance 四段式）
5. **打样** → `config/<slug>/sample.json` + 样片镜
6. **量产** → 只改文案，导出 `export/<slug>/master-16x9.mp4`

阶段定义与验收清单见 [`docs/PIPELINE.md`](docs/PIPELINE.md)。

## 目录

```
input/<slug>/          # 原始 PDF 或 outline.yaml + HANDOFF.md
storyboard/<slug>/     # 分镜 shots.md
motion/<slug>/         # 动效轨 timeline.md
config/<slug>/         # 打样 sample.json
export/<slug>/         # master + shorts/ + cover-3x4/
methods/               # 挂链方法卡（镜头词表、Seedance 等）
schemas/               # 输入与打样 schema
docs/PIPELINE.md       # 流水线母版
```

## 量产规则

- **允许改**：`talk` / `on_screen_text` / 章节文案  
- **不算量产（需新打样）**：换 skin、换镜头词表、改 palette / caption 等 config

## 协作

| 阶段 | 负责 |
|------|------|
| S0 立项 | 文档台 |
| S1–S5 分镜→导出 | 剪辑台 |
| 开仓 / Topics | Github台 |
| 方法卡 | X收藏台 → `methods/` |

## License

MIT（方法卡若引用外部资料，以卡内注明为准；勿把第三方「禁止商业用途」素材打进公开样片。）
