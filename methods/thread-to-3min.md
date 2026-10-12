# 方法卡：推串 → 学习视频（输入源形态 C）

- **挂阶段**：进线前 → S0；把 X 推串整理成提纲 schema 再进 `input/<slug>/`
- **来源**：https://x.com/op7418/status/2109467496298516760 · 前置 https://x.com/op7418/status/2108966708740505828

## 链路

`拉取全文 → 结构化长文（补概念+链接+中文排版）→ 写成 outline.yaml → 进本流水线 → 约 3 分钟学习成片`

## 本流水线角色

- **不是**另开一条剪辑链
- **是**合法输入类型 C：经 X收藏台整理成 §1.2 提纲 schema 后，与 PDF/提纲同等进线

## X收藏台交付物（进 S0 前）

```yaml
title: ...
hook: ...
chapters:
  - id: c1
    title: ...
    beats:
      - claim: ...
        talk: ...      # 可由推串句子改写
        visual: ...
ending: ...
meta:
  duration_target_sec: 180
  aspect: "16:9"
  skin: "ui-demo"   # 或 stickman
  source: "x-thread"
  source_url: "https://x.com/.../status/..."
```

落点：`input/<slug>/outline.yaml` + `HANDOFF.md`（注明原帖 URL）

## 禁止

- 未过 schema 门禁直接塞原始推文进分镜
- 无来源 URL 的整段粘贴
