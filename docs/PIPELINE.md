# 旗舰流水线母版：PDF / 提纲 → 口播动效成片

> 拍板：果汁工作小组 2026-10-12  
> 目标：一条可从头跑到尾的 B/C 旗舰（不是再堆 Skill）

## 0. 一句话定义

把一份 **PDF 或结构化提纲** 变成一条可发布的 **16:9 口播动效成片**（可选竖版切片），并留下可复用的打样 config，下次只换文案即可量产。

## 1. 输入约定

### 1.1 合法输入（三选一）

| 类型 | 格式 | 最低字段 |
|---|---|---|
| A. PDF | `.pdf` | 可读正文；页序清晰 |
| B. 结构化提纲 | `.md` / YAML | 见提纲 schema |
| C. 推串学习源 | X 帖串摘要 | 整理成提纲 schema 后再进线 |

### 1.2 提纲 schema（B/C 必须满足）

见 `schemas/outline.schema.yaml`。最低：`title` + `hook` + ≥2 `chapters`，每章 ≥1 `claim`。

落点：`input/<slug>/source.pdf` 或 `input/<slug>/outline.yaml`。

### 1.3 输入验收（进线前门禁）

- [ ] 有 `title` + `hook` + ≥2 个 `chapters`
- [ ] 每个 chapter 至少 1 个 `claim`
- [ ] 无版权不明整段粘贴；引用需标来源
- [ ] 文件落点正确

不通过 → 退回补字段，不进分镜。

## 2. 阶段与产物

| 阶段 | 负责 | 产物路径 | 完成定义 |
|---|---|---|---|
| **S0 立项** | 文档台 | `input/<slug>/` + `HANDOFF.md` | schema 齐、slug 定好 |
| **S1 分镜** | 剪辑台 | `storyboard/<slug>/shots.md` | 每镜有口播+画面+时长估 |
| **S2 动效轨** | 剪辑台 | `motion/<slug>/timeline.md` + 样片镜 | Seedance 四段式写进轨 |
| **S3 打样** | 剪辑台 | `config/<slug>/sample.json` + 样片 mp4 | 只验风格/节奏 |
| **S4 量产** | 剪辑台/自动化 | `export/<slug>/master-16x9.mp4` | 只换文案，config 不动 |
| **S5 切片/封面** | 剪辑台 | `export/<slug>/shorts/` + `cover-3x4/` | 可选 |
| **S6 入库** | 文档台 | 索引回链 | INDEX 更新 |

每镜强制字段见 `schemas/shot.schema.yaml`。打样 config 见 `schemas/sample-config.schema.json`。

量产规则：**只允许改** `talk` / `on_screen_text` / 章节文案；改皮肤或镜头词表 = 新打样。

## 3. 挂链资产

| 优先级 | 资产 | 挂在哪 |
|---|---|---|
| 1 | Seedance 四段式 + 真人八维 + 稳定区 | S2 `motion` + 每镜 `safe_zone` |
| 2 | 镜头 24 词表 | S1 每镜强制 `lens` |
| 3 | 打样定 config → 量产只换文案 | S3→S4 |
| 4 | 火柴人第二皮肤 | `meta.skin=stickman` |
| 5 | 推串→3 分钟学习视频 | 输入源形态 C |

方法卡正文放 `methods/`。

## 4. 验收清单

### 流水线级

- [ ] 合格提纲可按 S0→S4 产出 `master-16x9.mp4`
- [ ] README 写清输入 / 步骤 / 产物路径
- [ ] 至少 1 次打样→只换文案量产对照
- [ ] 失败时有明确退回阶段

### 成片级

- [ ] 开场 3s 内出现钩子
- [ ] 章节板可读；底字幕不挡稳定区
- [ ] 每镜有词表内 `lens`；动效符合四段式
- [ ] 横版 16:9；结尾口播可保留果汁习惯句

### 文档级

- [ ] `HANDOFF.md` 含 slug、输入类型、当前阶段、阻塞项
- [ ] 方法卡与 config 版本号一致
