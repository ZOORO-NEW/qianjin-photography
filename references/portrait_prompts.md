# 人像摄影提示词库（8 大风格）

每个风格含：风格说明 / 英文提示词模板（替换 `{subject}` 为主体、`{environment}` 为环境）/ 推荐参数 / 负向词。
生图前提醒用户 ImageGen 消耗额度（约 5–10 credits/张）。

---

## 1. 日系清新 Japanese Fresh
**说明**：柔和自然光、低饱和、留白多，适合治愈系人像。
**英文模板**：
```
Japanese fresh portrait photography of {subject}, soft natural window light, light beige and pastel tones, minimalist background, gentle smile, 35mm lens, f/2.0, high key, subtle film grain, peaceful atmosphere --ar 3:4
```

## 2. 复古胶片 Retro Film
**说明**：柯达胶片感、暖褪色、轻微颗粒，怀旧情绪。
**英文模板**：
```
Retro film portrait of {subject}, Kodak Portra 400 look, warm faded tones, slight grain, sunlight through leaves, 1980s mood, 50mm lens, f/2.8 --ar 3:4
```

## 3. 时尚大片 Fashion Editorial
**说明**：棚拍硬光、强对比、杂志大片感。
**英文模板**：
```
High fashion editorial portrait of {subject}, studio lighting, dramatic shadow, Vogue style, sharp makeup, bold contrast, 85mm lens, f/4, clean background --ar 2:3
```

## 4. 暗调情绪 Moody Low-key
**说明**：单光源、深暗背景、沉静忧郁，电影感。
**英文模板**：
```
Moody low-key portrait of {subject}, single rim light, deep shadows, dark background, melancholic expression, 85mm lens, f/1.8, cinematic --ar 3:4
```

## 5. 自然光治愈 Natural Light Healing
**说明**：黄金时刻、居家真实感、温暖松弛。
**英文模板**：
```
Candid natural light portrait of {subject}, golden hour, warm glow, cozy home setting, authentic emotion, 35mm lens, f/1.8, soft bokeh --ar 3:4
```

## 6. 街头抓拍 Street Candid
**说明**：城市背景、环境光、纪实瞬间。
**英文模板**：
```
Street photography candid portrait of {subject}, urban background, available light, frozen moment, 35mm lens, f/4, documentary style --ar 3:4
```

## 7. 黑白纪实 B&W Documentary
**说明**：高反差、颗粒、诚实表情， timeless。
**英文模板**：
```
Black and white documentary portrait of {subject}, strong contrast, grain, honest expression, 50mm lens, f/2.8, timeless --ar 3:4
```

## 8. 赛博朋克 Cyberpunk Neon
**说明**：雨夜霓虹、皮肤反光、未来感。
**英文模板**：
```
Cyberpunk neon portrait of {subject}, rainy night street, colorful neon reflections on skin, futuristic, 85mm lens, f/1.4, bokeh lights --ar 2:3
```

---

## 9. 法天象地·二重曝光 Fa Tian Xiang Di (Double Exposure)
**说明**：用户上传任意人像，前台保留真实完整人物（正常比例、清晰不透明），身后浮现同一人的巨型半透明神明虚影，顶天立地。适用于「法相撑天」的玄幻/国风创意人像。通用版：不指定性别/外貌，靠 `{reference}` 套用户照片。
**英文模板（图生图，上传人像后直接用）**：
```
Double exposure photography: in the lower center foreground, an EXACT photorealistic reproduction of the person from the reference photo, identical face and likeness preserved, same hairstyle, same clothing as in the source, natural skin texture with pores, candid unedited photograph look, full body reconstructed below the visible part with plausible natural clothing, feet visible, fully opaque, sharp focus, real ambient lighting matching the source photo; behind and towering above them, a colossal full-body translucent ethereal deity figure of the same person in a "Fa Tian Xiang Di" manifestation — complete head, torso, arms, and legs visible, semi-transparent, glowing golden celestial rim light, ornate divine robes, radiant halo, rising from earth to sky, merging with storm clouds and distant mountain silhouettes. The real person occupies the bottom 20% of the frame and must look like a real photograph, the giant phantom fills the upper 80% and may be idealized. 35mm lens, f/4, candid photo realism for foreground, cinematic xianxia fantasy for background, HDR, subtle film grain --ar 16:9
```
**追加负向词（接通用负向词）**：
```
porcelain skin, overly smooth skin, plastic skin, airbrushed, doll-like, beauty filter, smoothed face, changed hairstyle, different face
```
**画幅**：16:9（电影感）/ 2:3 或 9:16（竖屏冲击）
**注意**：① 最佳用正面全身照；半身照时模型会自动补全下身。② 前台「身份漂移」时：降低重绘强度（Denoising 0.35–0.45），或用工具「人物一致性 / Face ID / 局部重绘只画背景」锁定。③ 要前台 100% 不跑脸，用分阶段合成：先生成「空前景+巨神背景」，再把原图人物抠出贴回前景并加金色 rim light。

## 通用负向词（Negative Prompt）
```
cartoon, anime, illustration, painting, 3d render, deformed hands, extra fingers, blurred, low quality, watermark, text, logo
```

## 参数速查
| 风格 | 推荐镜头 | 光圈 | 画幅 |
|---|---|---|---|
| 日系清新 / 自然光治愈 | 35mm | f/1.8–2.0 | 3:4 |
| 时尚大片 / 赛博朋克 | 85mm | f/1.4–4 | 2:3 |
| 复古胶片 / 黑白纪实 | 50mm | f/2.8 | 3:4 |
| 街头抓拍 | 35mm | f/4 | 3:4 |
| 法天象地·二重曝光 | 35mm | f/4 | 16:9 |
