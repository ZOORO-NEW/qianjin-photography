# 人像摄影提示词库（六维框架升级版）

每个风格按 `pro_prompt_framework.md` 的六维拆解：构图 / 姿势站位 / 打光（四层公式）/ 色调 / 道具 / 技术。
英文模板已嵌入材质反光词与三点布光，可直接抄，也可当填空改。
生图前提醒用户 ImageGen / 生图工具约消耗 5–10 credits/张。

---

## 1. 日系清新 Japanese Fresh
- **姿势站位**：侧身微低头、手自然垂落、眼神朝下，松弛不摆拍
- **构图**：三分法、大量留白、主体偏一侧
- **打光**：柔窗光（维度三 L1-L4：soft window light from left, gentle fill, faint rim, light pastel background blurred）
- **色调**：低饱和米白粉彩，high key
- **道具**：浅色亚麻、绿植一角
```
Japanese fresh portrait of {subject}, three-quarter turn looking down, relaxed hands, soft natural window light from left, gentle fill, faint rim light, light beige and pastel tones, minimalist background with negative space, 35mm lens, f/2.0, high key, subtle film grain, peaceful atmosphere --ar 3:4
```

## 2. 复古胶片 Retro Film
- **姿势站位**：倚墙侧身、回头浅笑、肢体放松
- **构图**：中景、环境入画
- **打光**：透过树叶的斑驳阳光（leaf dappled sunlight），暖褪色
- **色调**：Kodak Portra 400 暖褪、轻微颗粒
- **道具**：老墙、自行车、胶片机
```
Retro film portrait of {subject}, leaning against wall three-quarter turn looking back with slight smile, leaf-dappled sunlight, warm faded tones, Kodak Portra 400 look, slight grain, 1980s mood, 50mm lens, f/2.8 --ar 3:4
```

## 3. 时尚大片 Fashion Editorial
- **姿势站位**：直面镜头、挺肩、锐利眼神，姿态有张力
- **构图**：中心或三分、干净背景
- **打光**：棚拍硬光（studio strobe），强对比、深暗部
- **色调**：高对比、干净
- **道具**：极简、无多余物
```
High fashion editorial portrait of {subject}, facing camera, confident posture, sharp eye contact, studio strobe lighting, dramatic shadow, Vogue style, bold contrast, clean background, 85mm lens, f/4, cinematic --ar 2:3
```

## 4. 暗调情绪 Moody Low-key
- **姿势站位**：低头或侧脸、肢体收拢，沉静
- **构图**：居中、深暗包围
- **打光**：单 rim light 勾边、深背景、主体皮肤 natural subsurface
- **色调**：low key、冷或中性
- **道具**：无，靠光塑形
```
Moody low-key portrait of {subject}, head slightly down, single rim light from behind, deep shadows, dark background, natural skin texture with visible pores, melancholic expression, 85mm lens, f/1.8, cinematic --ar 3:4
```

## 5. 自然光治愈 Natural Light Healing
- **姿势站位**：居家随意坐、捧杯或托腮、真实表情
- **构图**：环境三分、前景虚化
- **打光**：黄金时刻暖光（golden hour），柔 bokeh
- **色调**：暖、cozy
- **道具**：居家一角、杯、书
```
Candid natural light portrait of {subject}, sitting at home holding a cup, golden hour warm glow, authentic relaxed expression, soft bokeh foreground, cozy home setting, 35mm lens, f/1.8, photorealistic --ar 3:4
```

## 6. 街头抓拍 Street Candid
- **姿势站位**：行走中被抓拍、不看镜头、环境融入
- **构图**：环境主导、引导线（街道/橱窗）
- **打光**：available light 环境光
- **色调**：纪实中性
- **道具**：街景、路人虚化
```
Street photography candid portrait of {subject}, walking mid-stride not looking at camera, urban background with leading lines, available light, frozen moment, 35mm lens, f/4, documentary style --ar 3:4
```

## 7. 黑白纪实 B&W Documentary
- **姿势站位**：自然劳作/交谈姿态、诚实表情
- **构图**：中景、环境叙事
- **打光**：自然光、强反差
- **色调**：monochrome、高反差颗粒
- **道具**：工作环境
```
Black and white documentary portrait of {subject}, natural working pose, honest expression, strong contrast, heavy grain, 50mm lens, f/2.8, timeless --ar 3:4
```

## 8. 赛博朋克 Cyberpunk Neon
- **姿势站位**：侧身迎光、冷峻、动态
- **构图**：竖构、霓虹作框
- **打光**：rainy neon 皮肤反光（neon reflections on skin），bokeh lights
- **色调**：冷紫青、高饱和霓虹
- **道具**：雨夜街、霓虹招牌虚化
```
Cyberpunk neon portrait of {subject}, three-quarter turn, rainy night street, colorful neon reflections on skin, futuristic mood, bokeh lights, 85mm lens, f/1.4, cinematic --ar 2:3
```

## 9. 法天象地·二重曝光 Fa Tian Xiang Di (Double Exposure)
**说明**：上传任意人像，前台保留真实完整人物（正常比例、清晰不透明），身后浮现同一人巨型半透明神明虚影。通用版靠 `{reference}` 套用户照片。
```
Double exposure photography: in the lower center foreground, an EXACT photorealistic reproduction of the person from the reference photo, identical face and likeness preserved, same hairstyle, same clothing as in the source, natural skin texture with pores, candid unedited photograph look, full body reconstructed below the visible part with plausible natural clothing, feet visible, fully opaque, sharp focus, real ambient lighting matching the source photo; behind and towering above them, a colossal full-body translucent ethereal deity figure of the same person in a "Fa Tian Xiang Di" manifestation — complete head, torso, arms, and legs visible, semi-transparent, glowing golden celestial rim light, ornate divine robes, radiant halo, rising from earth to sky, merging with storm clouds and distant mountain silhouettes. The real person occupies the bottom 20% of the frame and must look like a real photograph, the giant phantom fills the upper 80% and may be idealized. 35mm lens, f/4, candid photo realism for foreground, cinematic xianxia fantasy for background, HDR, subtle film grain --ar 16:9
```
**追加负向词**：porcelain skin, overly smooth skin, plastic skin, airbrushed, doll-like, beauty filter, smoothed face, changed hairstyle, different face
**注意**：① 最佳正面全身照；半身照模型自动补全下身。② 身份漂移时降重绘强度（Denoising 0.35–0.45）或用局部重绘只画背景。③ 要前台 100% 不跑脸，分阶段合成：先生成空前景+巨神背景，再抠原图人物贴回前景加金色 rim light。

---

## 通用负向词（Negative Prompt）
```
cartoon, anime, illustration, painting, 3d render, deformed hands, extra fingers, blurred, low quality, watermark, text, logo, smoothed plastic skin, beauty filter
```

## 参数速查
| 风格 | 镜头 | 光圈 | 画幅 |
|---|---|---|---|
| 日系清新 / 自然光治愈 | 35mm | f/1.8–2.0 | 3:4 |
| 时尚大片 / 赛博朋克 | 85mm | f/1.4–4 | 2:3 |
| 复古胶片 / 黑白纪实 | 50mm | f/2.8 | 3:4 |
| 街头抓拍 | 35mm | f/4 | 3:4 |
| 暗调情绪 | 85mm | f/1.8 | 3:4 |
| 法天象地·二重曝光 | 35mm | f/4 | 16:9 |
