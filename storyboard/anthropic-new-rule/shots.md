# shots — `anthropic-new-rule`

| 字段 | 值 |
|---|---|
| slug | `anthropic-new-rule` |
| aspect | `16:9` |
| skin | `ui-demo` |
| duration_target_sec | `360`（约 5:45–6:25） |
| schema | `schemas/shot.schema.yaml` |
| lens_vocab | `methods/lens-24-vocab.md` |
| seedance | `methods/seedance-four-beat.md` |
| outline | `input/anthropic-new-rule/outline.yaml` |
| 护栏 | 主线=使用政策；勿说刑房促成新规；Pain Axis/便秘带条件；微软=背景对照；收尾果汁句 |

> S1 完成：每镜字段填齐 → 交 `motion/anthropic-new-rule/timeline.md`（S2）。`[需补]`=缺 A-roll/截图，不挡分镜。

---

## A. 钩子（s00）

```yaml
shot_id: s00
chapter_id: hook
lens: "Zoom in 3s 推向标题字"
duration_sec: 8
talk: "先说清楚：这条视频的口播、画面、字幕，基本都是 AI 做的——但今天不聊怎么做视频，Anthropic 出了条新规。"
on_screen_text: "全片 AI 制作 · Anthropic 出了条新规"
motion:
  setup: "黑场静帧，小字「全片 AI 制作」"
  action: "标题大字 Zoom in 定住"
  hold: "停 1s 可读"
  out: "L-cut 接章节板人声预入"
safe_zone: "底字幕下 15% 外；标题居中偏上"
```

---

## B. 章节板（s01）

```yaml
shot_id: s01
chapter_id: board
lens: "Pan 4s 横扫章节列表"
duration_sec: 5
talk: "今天按六块讲清楚：条款、边界、定义执行、案例、背景、日常建议。"
on_screen_text: "1 条款 · 2 边界 · 3 定义执行 · 4 案例 · 5 背景 · 6 建议"
motion:
  setup: "六条章节名淡入"
  action: "Pan 扫过列表，当前项高亮"
  hold: "全表定格 1s"
  out: "Wipe 切入 c1"
safe_zone: "列表居中；勿挡角标"
```

---

## C1. 时间与核心条款

```yaml
shot_id: s10
chapter_id: c1
lens: "Dolly in 6s 推向关键词卡"
duration_sec: 7
talk: "这次不光管你拿 Claude 干什么，还把「你怎么对待 Claude」写进了使用政策。"
on_screen_text: "怎么对待 Claude"
motion:
  setup: "政策封面静帧"
  action: "Dolly in 推关键词"
  hold: "高亮停住"
  out: "Jump cut 日期卡"
safe_zone: "关键词中上；字幕下安全区"
```

```yaml
shot_id: s11
chapter_id: c1
lens: "Freeze frame 定日期卡"
duration_sec: 9
talk: "10 月 8 日公布，11 月 12 日起生效。核心一句话：持续、无必要地虐待或残酷对待模型，算违规。"
on_screen_text: "2026-10-08 公布 · 2026-11-12 生效 · 持续+无必要"
motion:
  setup: "日期双卡入画"
  action: "核心条款展开，「持续」「无必要」高亮"
  hold: "Freeze frame 可读"
  out: "Cross dissolve 同节卡"
safe_zone: "双卡中部；字幕不挡日期"
```

```yaml
shot_id: s12
chapter_id: c1
lens: "Match cut 切同节对照"
duration_sec: 8
talk: "有意思的是，这条跟禁止霸凌他人、禁止虐待动物，写在同一节。聊天框里的 AI，也被加进了这组条款。"
on_screen_text: "同节：霸凌 · 虐待动物 · 对待模型"
motion:
  setup: "三列对照卡起幅"
  action: "Match cut 点亮第三列「模型」"
  hold: "三列并置 1.5s"
  out: "J-cut 预入边界反问"
safe_zone: "三列居中"
```

---

## C2. 边界：还能不能批评

```yaml
shot_id: s20
chapter_id: c2
lens: "Handheld 轻微晃动口播反问"
duration_sec: 12
talk: "比如你让它修 bug，说修好了却还报错，你回「这还没修好，重新检查」——这种不满和要求返工，不在这一条的限制范围里。"
on_screen_text: "普通不满 / 返工 ≠ 本条限制"
motion:
  setup: "报错示意静帧 [需补 UI]"
  action: "字幕句弹出 + Handheld 口播"
  hold: "排除项卡「普通不满」勾选"
  out: "Jump cut 排除项续"
safe_zone: "示意上半；口播/字幕下安全区"
```

```yaml
shot_id: s21
chapter_id: c2
lens: "Tilt 下扫排除项清单"
duration_sec: 10
talk: "黑暗小说、普通反驳、模型测试和研究，都不是本条要管的。当然，其他使用规则仍然适用。"
on_screen_text: "排除：黑暗创作 · 反驳 · 测试/研究｜其他规则仍适用"
motion:
  setup: "排除项卡顶部"
  action: "Tilt 扫过勾选项"
  hold: "底部警示条「其他规则仍适用」"
  out: "Smash cut 完整定义"
safe_zone: "清单中部"
```

---

## C3. 完整定义与执行

```yaml
shot_id: s30
chapter_id: c3
lens: "Zoom in 推向「持续+无必要」"
duration_sec: 11
talk: "官方完整说法是虐待或残酷对待模型。针对极端情况——看不出有什么目的，却反复、残酷地对待模型。「持续」和「无必要」要一起看。"
on_screen_text: "虐待/残酷对待 · 极端 · 持续+无必要"
motion:
  setup: "核心条款卡"
  action: "Zoom in 极端情况卡叠入"
  hold: "两词并亮"
  out: "Whip pan 执行卡"
safe_zone: "卡片中区"
```

```yaml
shot_id: s31
chapter_id: c3
lens: "Smash cut 切「≠封号」"
duration_sec: 10
talk: "真到了这种情况，Claude 主要是结束当前对话。结束聊天和封号不能画等号；公告也没有给出骂几句、持续多久就算违规的数字。"
on_screen_text: "主要处理：结束对话 · ≠ 封号 · 频率未量化"
motion:
  setup: "执行方式卡"
  action: "Smash cut 叠「≠封号」"
  hold: "停住可读"
  out: "Cross dissolve 历史流程卡"
safe_zone: "中部大字幕"
```

```yaml
shot_id: s32
chapter_id: c3
lens: "Tracking 跟随引导→停流程"
duration_sec: 9
talk: "结束对话能力 2025 年 8 月就有了。设计是先引导，多次没用才停。这次补上的，是使用政策里的明确限制。"
on_screen_text: "2025-08：引导→再引导→停｜本次：政策明文"
motion:
  setup: "三步流程起点"
  action: "Tracking 沿箭头走到「停」"
  hold: "政策明文角标亮起"
  out: "Jump cut 刑房标题"
safe_zone: "流程条中部"
```

---

## C4. 案例：刑房与 Pain Axis

```yaml
shot_id: s40
chapter_id: c4
lens: "Dutch angle 短切入刑房标题后回正"
duration_sec: 14
talk: "公开项目「AI 刑房」在本地开放权重模型上人为干预内部状态。作者未证明模型真受苦；跟 Claude 聊天框不是同一种操作；官方也没把它列为更新原因。"
on_screen_text: "AI 刑房 · 开放权重本地 · ≠Claude 聊天 · 非新规起因"
motion:
  setup: "刑房事实卡 Dutch 起幅"
  action: "回正 + 护栏字幕逐条上"
  hold: "「非新规起因」定格"
  out: "Cross dissolve Pain Axis"
safe_zone: "护栏字幕下安全区外缘"
```

```yaml
shot_id: s41
chapter_id: c4
lens: "Speed ramp 数字 0%→75%→94%"
duration_sec: 16
talk: "《The Pain Axis》在特定微调+注入条件下，删除按钮选择从 0% 到 75%，对照垃圾邮件时到 94%。这是描述性按钮，不能套到普通 Qwen 或 Claude；也未证明模型主观上真的疼。"
on_screen_text: "0%→75% · 94% · 描述性按钮 · 未证主观疼痛"
motion:
  setup: "双按钮示意静帧"
  action: "Speed ramp 数字跳变"
  hold: "限制小字停留 2s"
  out: "Jump cut 0/560"
safe_zone: "数字居中；小字底部安全区外"
```

```yaml
shot_id: s42
chapter_id: c4
lens: "Freeze frame 定 0/560"
duration_sec: 12
talk: "无注入、只用自然语境侮辱时，560 次里一次没选删除按钮。便秘语料那则是开发者报告，未独立复现——第一人称「我难受」和真有体验要分开验证。"
on_screen_text: "无注入自然语境 0/560 · 便秘=开发者报告未复现"
motion:
  setup: "0/560 大字幕入"
  action: "Freeze frame + Tom's Guide 卡旁注 [需补图可后补]"
  hold: "分开验证字幕"
  out: "L-cut 入福祉背景"
safe_zone: "大数字中上"
```

---

## C5. 背景与同批其他规则

```yaml
shot_id: s50
chapter_id: c5
lens: "Rack focus 福祉卡→微软卡"
duration_sec: 14
talk: "Anthropic 2025 年就有模型福祉研究计划，并承认 AI 有没有意识尚无科学共识。微软负责人 2026-09 批评过拟人化路线——那是草案背景对照，早于这次新规。"
on_screen_text: "福祉研究 · 无科学共识 · 微软背景对照（早于新规）"
motion:
  setup: "福祉卡清晰、微软卡虚"
  action: "Rack focus 切到微软卡"
  hold: "「早于新规」角标"
  out: "Wipe 其他规则条"
safe_zone: "双卡左右分栏"
```

```yaml
shot_id: s51
chapter_id: c5
lens: "Pan 横扫其他规则条"
duration_sec: 12
talk: "这轮不只有「别虐待 Claude」：欺骗性宣传、选举假消息、武器制导、未经同意追踪、执法决策建议、可伤人硬件的急停要求、政府客户另行约定等，很多是把旧规则写得更明确。"
on_screen_text: "宣传·选举·武器·监控·执法·硬件急停·政府客户"
motion:
  setup: "规则条左侧起"
  action: "Pan 扫过各条上屏"
  hold: "收束「写得更明确」"
  out: "Jump cut 建议对比卡"
safe_zone: "条列中部"
```

---

## C6. 日常建议与收束

```yaml
shot_id: s60
chapter_id: c6
lens: "Split 用 Jump cut 弱反馈→具体反馈"
duration_sec: 10
talk: "下面是使用建议，不是官方礼貌条款。别只回「重做」——可以说预期 200、实际 500、日志在下面，先检查这个报错。"
on_screen_text: "弱：重做｜强：预期/实际/日志"
motion:
  setup: "左栏弱反馈"
  action: "Jump cut 右栏具体反馈"
  hold: "对比定格"
  out: "Match cut 验收句"
safe_zone: "左右分栏中部"
```

```yaml
shot_id: s61
chapter_id: c6
lens: "Dolly in 推向验收句"
duration_sec: 8
talk: "它说全部完成时，直接要「把测试跑一遍，把结果给我看」。是否完成看证据，跟语气温不温柔是两件事。"
on_screen_text: "把测试结果给我看"
motion:
  setup: "对话气泡远景"
  action: "Dolly in 推验收句"
  hold: "停 1s"
  out: "Cross dissolve 边界收束卡"
safe_zone: "字幕中下安全区外缘"
```

```yaml
shot_id: s62
chapter_id: c6
lens: "Orbit/Arc 环绕边界收束卡"
duration_sec: 10
talk: "普通批评和纠错仍然可以；极端、持续、无必要的残酷互动会受约束。持续多久、重复多少次算违规，公告还没有数字，得看后续执行。"
on_screen_text: "可批评 · 极端持续无必要受约束 · 频率未给出"
motion:
  setup: "收束卡正面"
  action: "慢 Orbit 半圈强调三块"
  hold: "「频率未给出」亮起"
  out: "Fade 接结尾口播"
safe_zone: "三块信息居中"
```

---

## D. 结尾（s90）

```yaml
shot_id: s90
chapter_id: ending
lens: "Dolly out 缓慢拉远口播"
duration_sec: 5
talk: "我是果汁，每天分享更多好用的 AI 知识。"
on_screen_text: "果汁 · 每天分享更多好用的 AI 知识"
motion:
  setup: "口播近景 [需补 A-roll]"
  action: "Dolly out 至半身"
  hold: "定格 CTA"
  out: "黑场"
safe_zone: "人脸中上；字幕下安全区"
```

---

## E. 验收镜（§4.2）

- [x] 开场 3s 内钩子（s00 标题/口播）
- [x] 章节板可读（s01）
- [x] 每镜 `lens` 在 24 词表内
- [x] 每镜 `motion` 四段式齐全
- [x] 16:9；结尾用果汁固定句（非黄白）
- [x] 时长估加总 ≈ 8+5+7+9+8+12+10+11+10+9+14+16+12+14+12+10+8+10+5 ≈ **190s 口播镜核**；按旧节拍扩气口/B-roll 后目标 **345–385s**（S2 timeline 拆细）
- [ ] A-roll / 部分截图 `[需补]` — 不挡进入 S2
- [x] 护栏字幕位已写入刑房 / Pain Axis / 微软镜

**S1 完成定义：** 本文件可交 S2。下一棒：`motion/anthropic-new-rule/timeline.md`（按 Seedance 四段式落到时间线，并把长镜按 ≤15s 口播节拍再拆如需）。
