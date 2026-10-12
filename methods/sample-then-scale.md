# 方法卡：打样定 config → 量产只换文案

- **挂阶段**：S3→S4
- **来源**：https://x.com/hx831126/status/2109232384994611241

## 公式

`打样模型定标准（config + 自动检查）→ 量产 Bot 只换内容 → 人只拍板`

## 本流水线怎么做

1. **S3 打样**：用强审美路径出**第一条**样片镜；写入 `config/<slug>/sample.json`
2. **人审样片**：只验风格/节奏/可读性，不在此轮改文案结构
3. **S4 量产**：只读 config；只改 `talk` / `on_screen_text` / 章节文案；跑检查后交 `export/<slug>/master-16x9.mp4`
4. **换皮肤或词表** = 新打样，不算量产

## `sample.json` 最低键（与母版一致）

```json
{
  "slug": "",
  "aspect": "16:9",
  "skin": "ui-demo",
  "palette": {},
  "caption_style": {},
  "capsule_style": {},
  "seedance_profile": "four-beat-v1",
  "lens_vocab": "24-terms-v1",
  "sample_shot_ids": ["s01", "s03"]
}
```

## 禁止

- 量产轮改 palette / skin / lens_vocab
- 无样片验收直接批量出片
