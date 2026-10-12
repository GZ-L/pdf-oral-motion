# shots — `<slug>`

| 字段 | 值 |
|---|---|
| slug | `<slug>` |
| aspect | `16:9` |
| skin | `ui-demo` \| `stickman` |
| duration_target_sec | `60–180` |
| schema | `schemas/shot.schema.yaml` |
| lens_vocab | `methods/` 内 24 词表（填专名） |
| seedance | 四段式：setup → action → hold → out |

> 填法：复制 yaml 块改内容。`lens` / `safe_zone` / 四段 `motion` 为强制字段。

---

## A. 钩子（s00，0–3s）

```yaml
shot_id: s00
chapter_id: hook
lens: ""                  # 必填：24 词表专名，如「大字标题切入」
duration_sec: 3
talk: ""                  # 开场钩子一句（对齐 outline.hook）
on_screen_text: ""
motion:
  setup: ""               # 起幅/静帧
  action: ""              # 进入动作
  hold: ""                # 停顿可读
  out: ""                 # 切出/过渡
safe_zone: "底字幕避开下 15%；口播人脸居中偏上"
```

<!-- 示例（量产时删除）
shot_id: s00
chapter_id: hook
lens: 大字标题切入
duration_sec: 3
talk: "今天用一份提纲，直接跑出口播动效成片。"
on_screen_text: "PDF → 口播动效"
motion:
  setup: 黑场+标题字入
  action: 字放大定住
  hold: 停 0.6s
  out: 切章节板
safe_zone: 字幕在下安全区外
-->

---

## B. 章节板（目录镜）

```yaml
shot_id: s01
chapter_id: board
lens: ""                  # 如「章节列表板」
duration_sec: 4
talk: ""                  # 可读「一共讲 N 点」或静音
on_screen_text: ""        # 列出 c1 / c2 / … 标题
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: "列表居中；勿挡角标"
```

---

## C. 口播 + 动效轨（按章复制）

### 章 c1 — `<章标题>`

```yaml
shot_id: s10
chapter_id: c1
lens: ""
duration_sec: 8
talk: ""                  # 对齐 outline.chapters[].beats[].talk
on_screen_text: ""        # 结论短句 / 关键词
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: ""
```

```yaml
shot_id: s11
chapter_id: c1
lens: ""
duration_sec: 8
talk: ""
on_screen_text: ""
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: ""
```

### 章 c2 — `<章标题>`

```yaml
shot_id: s20
chapter_id: c2
lens: ""
duration_sec: 8
talk: ""
on_screen_text: ""
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: ""
```

```yaml
shot_id: s21
chapter_id: c2
lens: ""
duration_sec: 8
talk: ""
on_screen_text: ""
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: ""
```

> 更多章：复制「章 c*」整块，递增 `shot_id`（建议 s30、s31…）。

---

## D. 结尾

```yaml
shot_id: s90
chapter_id: ending
lens: ""
duration_sec: 5
talk: ""                  # 默认可「我是果汁…」+ CTA（点赞收藏自取）
on_screen_text: ""
motion:
  setup: ""
  action: ""
  hold: ""
  out: ""
safe_zone: ""
```

---

## E. 验收镜（成片级，对齐母版 §4.2）

- [ ] 开场 3s 内出现钩子（口播或大字）
- [ ] 章节板可读；底字幕不挡 `safe_zone`
- [ ] 每镜 `lens` 在 24 词表内
- [ ] 每镜 `motion` 符合四段式（setup/action/hold/out）
- [ ] 横版 16:9；结尾口播可保留果汁习惯句
- [ ] 时长估加总 ≈ `duration_target_sec`（±15%）
- [ ] 无未授权素材说明（若有 UI 包装需标注）

**S1 完成定义：** 本文件每镜字段填齐 → 进入 `motion/<slug>/timeline.md`（S2）。
