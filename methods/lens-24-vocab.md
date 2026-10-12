# 方法卡：镜头语言 24 词表

- **挂阶段**：S1 每镜强制字段 `lens`（切镜加转场名）
- **来源**：https://x.com/showheyohtaki/status/2109112248832503895
- **schema 对齐**：`schemas/shot.schema.yaml` → `lens`

## 精度公式

`名称 + 秒数 + 速度 + 对象`  
例：`3秒内缓慢 Dolly in 推向人物面部`

## 词表（24）

**运镜 01–08**  
Pan｜Tilt｜Dolly in｜Zoom in｜Tracking｜Orbit/Arc｜Crane up｜Dolly zoom

**风格/时间 09–16**  
Rack focus｜Handheld｜FPV｜Dutch angle｜Slow motion｜Speed ramp｜Time-lapse｜Freeze frame

**转场 17–24**（切镜时写）  
Jump cut｜Match cut｜Whip pan｜Cross dissolve｜Wipe｜Smash cut｜J-cut｜L-cut

## 本流水线规则

- 每镜 **必须** 1 个运镜专名（禁止「好看一点」「电影感」）
- 镜间切换再加 1 个转场专名
- `duration_sec` 与公式里的秒数一致

## 禁止

- 空 `lens` 或自由发挥非词表词（新词须先扩表并改 schema 版本）
