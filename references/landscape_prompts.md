# 风景风光摄影提示词库（六维框架升级版）

每个风格按 `pro_prompt_framework.md` 六维拆解：构图 / 主体站位（前景中景背景层次）/ 打光 / 色调 / 道具（大气元素）/ 技术。
英文模板已按四层打光思路写清光位与色调，可直接抄。
生图前提醒用户 ImageGen / 生图工具约消耗 5–10 credits/张。

---

## 1. 高山云海 Mountain Sea of Clouds
- **构图**：前景山尖 + 中景云海 + 背景远峰，三层纵深
- **打光**：soft morning mist 柔光，晨光从一侧
- **色调**：冷调清透、低饱和
- **大气**：流动云雾、丁达尔光
```
Photorealistic landscape of {location}, foreground peak, midground endless sea of clouds, background distant ranges, soft morning mist, divine light rays, dramatic depth, 24mm wide lens, f/8, high dynamic range, cinematic --ar 16:9
```

## 2. 海岸日落 Coastal Sunset
- **构图**：三分法、地平线在下三分之一，岩石作前景剪影
- **打光**：golden hour 暖光，海面反光
- **色调**：暖金、长曝丝滑
- **大气**：丝滑水面、霞光
```
Photorealistic coastal sunset at {location}, golden sky reflection on calm sea, rock silhouette in foreground, long exposure silky water, 16mm lens, f/11, warm tones, golden hour --ar 3:2
```

## 3. 城市夜景 City Night
- **构图**：广角全景、车流作引导线
- **打光**：blue hour 蓝调时刻，霓虹补光
- **色调**：青蓝 + 霓虹彩点
- **大气**：光轨、薄雾
```
Photorealistic city night panorama of {location}, light trails on highways as leading lines, neon glow, blue hour, 24mm lens, f/8, long exposure, sharp --ar 16:9
```

## 4. 极简雪景 Minimal Snow
- **构图**：大量留白、单一小主体（孤树）打破空白
- **打光**：soft overcast 平光，无强阴影
- **色调**：高调、冷白
- **大气**：飘雪、静谧
```
Photorealistic minimalist snow scene at {location}, vast white field, tiny lone tree as single subject, soft overcast light, negative space, 35mm lens, f/5.6, high key, serene --ar 3:2
```

## 5. 秋色森林 Autumn Forest
- **构图**：林木作引导线向纵深，光束从林冠
- **打光**：sun rays through trees 侧逆光
- **色调**：金黄红叶、暖调
- **大气**：落叶、光尘
```
Photorealistic autumn forest at {location}, golden and red foliage, sun rays through trees, fallen leaves, volumetric light, 35mm lens, f/4, warm color grading --ar 3:2
```

## 6. 田园晨雾 Pastoral Morning Mist
- **构图**：中景农舍 + 前景田野 + 背景丘陵
- **打光**：gentle soft light 晨光
- **色调**：清新低饱和绿
- **大气**：薄雾、炊烟
```
Photorealistic pastoral morning mist at {location}, green fields foreground, distant farmhouse midground, soft fog, gentle light, 24mm lens, f/8, peaceful --ar 3:2
```

## 7. 星空银河 Starry Galaxy
- **构图**：地景剪影作前景框，银河拱桥居中
- **打光**：自然星光照，无人工光
- **色调**：深蓝黑、冷
- **大气**：清晰星点、气辉
```
Photorealistic night sky above {location}, Milky Way arch centered, clear stars, dark foreground silhouette, airglow, 14mm lens, f/2.8, long exposure, low noise --ar 16:9
```

## 8. 沙漠驼影 Desert Camel
- **构图**：沙丘曲线作引导线，驼影作中景
- **打光**：golden hour 逆光长投影
- **色调**：暖橙渐变
- **大气**：热浪、沙尘
```
Photorealistic desert at {location}, rolling sand dune curves as leading lines, camel silhouette at golden hour with long shadow, 35mm lens, f/8, warm gradient, cinematic --ar 3:2
```

---

## 通用负向词（Negative Prompt）
```
cartoon, anime, illustration, painting, 3d render, oversaturated, blurry, low quality, watermark, text, logo, people crowd
```

## 参数速查
| 风格 | 镜头 | 光圈 | 画幅 |
|---|---|---|---|
| 高山云海 / 田园晨雾 | 24mm | f/8 | 16:9 / 3:2 |
| 海岸日落 / 秋色森林 | 16–35mm | f/4–11 | 3:2 |
| 城市夜景 | 24mm | f/8 | 16:9 |
| 极简雪景 | 35mm | f/5.6 | 3:2 |
| 星空银河 | 14mm | f/2.8 | 16:9 |
| 沙漠驼影 | 35mm | f/8 | 3:2 |
