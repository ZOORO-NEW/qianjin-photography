# ImageGen 调用指南（摄影写实图）

本技能功能 1 通过 **ImageGen** 工具生成逼真摄影图像。以下为调用要点。

## 1. 额度提醒（必须）
生成前明确告知用户：**ImageGen 每张约消耗 5–10 credits**。用户确认后再调用。

## 2. 提示词语言
- **主提示词用英语**：写实摄影模型对英文摄影术语（lens, aperture, bokeh, golden hour, Kodak Portra）理解最好。
- **可追加中文风格说明**作为注释，但传给模型的 prompt 以英文为主。
- 参考 `portrait_prompts.md` / `landscape_prompts.md` / `humanity_macro_prompts.md` 的英文模板。

## 3. 写实感关键词（建议必带）
- 镜头：`35mm / 50mm / 85mm / 24mm wide / 100mm macro`
- 光圈：`f/1.8 / f/2.8 / f/8`（控制景深）
- 光线：`golden hour / natural window light / rim light / soft overcast / neon`
- 胶片感：`Kodak Portra 400 / film grain / high key`
- 画质：`photorealistic / sharp / high dynamic range / cinematic`

## 4. 画幅参数（--ar）
| 题材 | 画幅 | 说明 |
|---|---|---|
| 人像竖构 | 3:4 或 2:3 | 适配手机竖屏 |
| 风景横构 | 16:9 或 3:2 | 桌面/横屏 |
| 微距 / 方形 | 1:1 | 小红书方图 |
| 城市夜景 | 16:9 | 全景感 |

> 具体模型是否支持 `--ar` 以 ImageGen 实际参数为准；若不支持，用相近比例描述（如 "vertical composition"）。

## 5. 负向词（Negative Prompt）
始终附加，避免非摄影产物：
```
cartoon, anime, illustration, painting, 3d render, deformed hands, extra fingers, blurred, low quality, watermark, text, logo, oversaturated
```

## 6. 迭代策略
生图不满意时按以下顺序调：
1. **光线不对** → 改 golden hour / rim light / soft overcast。
2. **太假** → 加 `film grain` / `subtle grain` / `photorealistic` 强化。
3. **构图乱** → 明确镜头焦段与 `negative space` / `symmetrical`。
4. **主体歪** → 在负向词加 `deformed, extra fingers`（人像）。
5. 仍不行 → 换风格模板或降低复杂度（减少环境元素）。

## 7. 回传规范
生成后必须向用户回传：
- 实际使用的**英文提示词**（含负向词）
- 画幅
- 推荐实拍参数（镜头/光圈/光线），方便用户用真相机复刻
