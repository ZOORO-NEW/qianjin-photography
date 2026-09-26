# 人文 / 微距 / 建筑 / 美食 摄影提示词库（六维框架升级版）

覆盖非人像、非纯风光的常用写实题材。按 `pro_prompt_framework.md` 六维拆解标注。
微距题材用四层打光公式的「微距变体」（侧掠光 raking light 显纹理 + 极浅景深）。
英文模板替换 `{subject}` / `{location}`。生图前提醒用户约消耗 5–10 credits/张。

---

## 一、人文摄影 Humanity

### 1. 市集烟火 Market Life
- **构图**：中景环境、引导线（摊位排布）
- **打光**：warm lantern light 暖灯、蒸汽补氛围
- **色调**：暖、生活化
- **道具**：摊位、食物车、人群虚化
```
Photorealistic street market scene at {location}, bustling stalls, warm lantern light, steam from food carts, candid crowd, 35mm lens, f/2.8, documentary, warm tones --ar 3:2
```

### 2. 老街生活 Old Street Life
- **构图**：框架式（门洞/巷口）框住主体
- **打光**：afternoon side light 午后侧光
- **色调**：nostalgic 褪旧暖
- **道具**：青砖墙、晾晒衣物、自行车
```
Photorealistic narrow old street at {location}, weathered brick walls, hanging laundry, bicycle, afternoon side light, framed composition, 35mm lens, f/4, nostalgic --ar 3:2
```

### 3. 手艺人 Craftsman
- **构图**：中景、聚焦手部动作
- **打光**：warm side light 暖侧光塑手纹（维度三：key from left, fill from right, rim on hands）
- **色调**：暖、故事感
- **道具**：工具、工作台
```
Photorealistic portrait of a craftsman {subject} working, focused hands as subject, warm side light from left, soft fill, rim light on hands showing texture, workshop tools around, 50mm lens, f/2.8, storytelling --ar 3:4
```

### 4. 节庆信仰 Festival & Faith
- **构图**：中景群像、烟雾作前景
- **打光**：candlelight + incense glow 烛光
- **色调**：暖彩、神秘
- **道具**：香火、传统服饰、灯笼
```
Photorealistic local festival at {location}, colorful traditional costumes, incense smoke as foreground, candlelight glow, 35mm lens, f/2.8, cultural atmosphere, warm tones --ar 3:2
```

## 二、微距摄影 Macro（四层打光·微距变体）

> 微距命门：用 raking light（侧掠光）把纹理拉出来 + 极浅景深（f/2.8–f/5.6）只让一点清晰。
> 第二层材质反光词尤其关键：露珠高光、昆虫绒毛、金属锈迹、食物油光。

### 5. 花卉露珠 Flower with Dew
```
Photorealistic macro of a flower with morning dew drops, raking side light revealing petal texture, shallow depth of field with one droplet sharp, bokeh background, 100mm macro lens, f/2.8, crisp detail --ar 1:1
```

### 6. 昆虫微距 Insect Macro
```
Photorealistic macro of {subject} insect on leaf, extreme detail, tiny hairs visible under raking light, shallow DOF, 100mm macro lens, f/4, natural light, tack sharp --ar 1:1
```

### 7. 材质纹理 Texture
```
Photorealistic macro of weathered wood / rusted metal texture, rich tactile detail, raking light across surface showing grain and pits, 100mm macro lens, f/5.6, shallow DOF --ar 1:1
```

### 8. 食物细节 Food Detail
```
Photorealistic macro of {subject} dish, steam rising, crumb texture, soft top light with appetizing glisten, 100mm macro lens, f/2.8, shallow DOF, 8k food photography --ar 1:1
```

## 三、其他场景 Other

### 9. 建筑几何 Architecture Geometry
- **构图**：对称构图、线条引导
- **打光**：蓝天硬光、清晰阴影
- **色调**：干净、高调
```
Photorealistic architectural photography of {location}, symmetrical lines, minimalist facade, blue sky, 24mm lens, f/8, clean composition --ar 3:2
```

### 10. 美食静物 Food Still Life
- **构图**：三分、主体偏置
- **打光**：soft window light 柔窗光（维度三：key from left, fill, rim on plate edge）
- **色调**：warm tone 暖
- **道具**：亚麻布、粗陶盘、木桌
```
Photorealistic food still life of {subject}, soft window light from left, linen background, rustic plate, warm tone, rim light on plate edge, 50mm lens, f/2.8, 8k food photography --ar 1:1
```

---

## 通用负向词（Negative Prompt）
```
cartoon, anime, illustration, painting, 3d render, deformed, blurry, low quality, watermark, text, logo, oversaturated
```

## 参数速查
| 题材 | 镜头 | 光圈 | 画幅 |
|---|---|---|---|
| 人文街拍 | 35mm | f/2.8–4 | 3:2 |
| 手艺人 / 美食静物 | 50mm | f/2.8 | 3:4 / 1:1 |
| 微距 | 100mm 微距 | f/2.8–5.6 | 1:1 |
| 建筑几何 | 24mm | f/8 | 3:2 |
