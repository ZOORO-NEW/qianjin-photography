# 静物 / 商业产品摄影提示词库（四层打光公式驱动）

商业产品图是带货自媒体最高频的刚需。翻车几乎不在模型，在没告诉 AI 光从哪来、表面该怎么反光。
本库所有模板都用 `pro_prompt_framework.md` 的「四层打光公式」驱动，可直接抄，也可当填空模板改。

> 生图前提醒用户 ImageGen / 生图工具约消耗 5–10 credits/张。

---

## 通用四层打光公式（填空模板）

```
[第一层 主体锚定]：{什么产品、什么材质、什么颜色、什么角度}
[第二层 材质反光词（命门）]：{玻璃通透/金属冷反光/织物哑光/液面油脂光泽…}
[第三层 三点布光]：left-top key light, soft fill from lower right, rim light from front
[第四层 背景景深]：{浅灰/深灰/木纹}渐变背景, 主体底部柔和/锐利投影, 背景轻微虚化
+ 8k product photography quality
```

**翻车版 vs 锁定版（必看）**
- 翻车：「一张高清的电商护肤品产品图，白底，高级感」→ 死光、假、塑料味
- 锁定：「30ml 琥珀色磨砂玻璃精华瓶，45度俯拍。玻璃通透、瓶口边缘高光、内部液体轻微折射。左上45度主光塑造立体感，右下方弱补光压暗部，前方轮廓光勾边。浅灰渐变背景，瓶底柔和自然投影，背景轻微虚化。8k产品摄影质感。」

📌 产品图是打光的艺术，不是分辨率的艺术。换布光公式比换模型更管用。

---

## 1. 美妆护肤 Cosmetics & Skincare

**材质关键词**：glass translucent / frosted matte / pump dispenser / edge highlight / internal refraction
**布光**：左主光勾通透，右补光压死黑，前方轮廓光描瓶沿；浅灰渐变背景 + 底部柔和投影。

```
30ml amber frosted glass serum bottle, fine matte texture on body, 45-degree top-down view.
Glass translucent, bright edge highlight on cap, slight internal liquid refraction.
Left-top key light shaping volume, soft fill from lower right lifting shadows, front rim light outlining the bottle edge.
Light gray gradient background, soft natural shadow under bottle, background slightly blurred.
Muted warm tones, clean beauty look.
105mm macro lens, f/5.6, photorealistic, sharp focus, 8k product photography --ar 1:1
```

## 2. 食品饮品 Food & Beverage

**材质关键词**：oil sheen / condensation droplet / steam / caramelized edge / appetizing glisten
**布光**：暖调主光勾食欲（食物靠"能吃"活着），侧光描轮廓，木纹/大理石台面，蒸汽或水珠提质感。

```
350ml matte ceramic coffee cup, warm off-white body, fine matte surface, eye-level slightly above.
Coffee surface with delicate oil sheen, a ring of light brown crema on the rim, one condensation droplet on the wall.
Warm key light from upper left for appetite, soft fill from lower right, front rim light tracing the cup edge.
Light wood grain tabletop, soft natural shadow under cup, background slightly blurred.
Warm tones, cozy mood.
85mm lens, f/4, photorealistic, sharp focus, 8k food photography --ar 1:1
```

## 3. 3C 数码 Tech & Gadgets

**材质关键词**：cool mirror reflection / brushed metal texture / matte black plastic / specular edge
**布光**：冷调反光 + 拉丝纹理；深灰背景配锐利投影；边缘轮廓光勾科技感（科技感靠冷色和对比，不靠"科技感"三字）。

```
Single in-ear Bluetooth earbud, matte black plastic with metal mesh, cool mirror reflection on surface, visible brushed texture, 45-degree top-down.
Left-top key light shaping volume, soft fill from lower right killing dead black, front edge rim light outlining the bud silhouette.
Dark gray gradient background, sharp shadow under earbud, background blurred.
Cool tones, tech aesthetic.
100mm macro lens, f/5.6, photorealistic, sharp focus, 8k product photography --ar 1:1
```

## 4. 服饰穿搭 Apparel & Fabric

**材质关键词**：matte drape / soft fold shadow / natural wrinkles / fabric texture
**布光**：柔光平光（服装怕硬光炸出噪点），浅色背景微虚化，自然褶皱阴影出垂坠感。

```
Folded linen shirt in beige, soft matte drape, natural fold shadows, flat lay top view.
Matte fabric texture, gentle wrinkles, no harsh highlight.
Soft even window light from left, light fill, subtle rim from front.
Pale background, soft shadow beneath, background slightly blurred.
Muted light tones, minimalist.
50mm lens, f/4, photorealistic, sharp focus, 8k fashion photography --ar 1:1
```

## 5. 珠宝腕表 Jewelry & Watches

**材质关键词**：diamond sparkle / polished metal / specular glint / reflective bezel
**布光**：多点微光制造火彩，黑/深背景让金属跳出来，极高锐度，微距。

```
Luxury wristwatch, polished stainless steel case, reflective bezel, subtle diamond sparkle on indices, 45-degree view.
Specular glints on metal, crisp reflection, no blown highlights.
Two-point key light from upper left and right, black velvet background, tiny sharp shadow.
High contrast, luxurious mood.
100mm macro lens, f/8, photorealistic, ultra sharp, 8k jewelry photography --ar 1:1
```

## 6. 家居好物 Home & Lifestyle

**材质关键词**：wood grain / ceramic matte / soft textile / natural material
**布光**：自然窗光，暖调，生活化台面（木桌/亚麻），浅景深突出单品。

```
Ceramic vase with dried pampas, matte off-white glaze, soft textile behind, eye-level.
Natural matte ceramic, gentle shape, no glare.
Soft window light from left, warm fill, faint rim.
Light wood tabletop, soft shadow, background blurred with bokeh.
Warm muted tones, cozy lifestyle.
50mm lens, f/2.8, photorealistic, sharp focus, 8k interior photography --ar 3:4
```

---

## 场景模板速查（4 类高频）

| 品类 | 第二层材质词 | 第三层光 | 第四层背景 |
|---|---|---|---|
| 美妆护肤 | 玻璃通透/边缘高光/液体折射 | 浅灰渐变+底部投影 | 浅灰渐变 |
| 食品饮品 | 暖光/水珠/蒸汽/油脂光泽 | 侧光勾食欲 | 木纹/大理石 |
| 3C数码 | 冷调镜面反光/拉丝纹理 | 深灰+锐利投影 | 深灰渐变 |
| 服饰穿搭 | 哑光垂坠/自然褶皱阴影 | 柔光平光 | 浅色微虚化 |

## 三步套用
1. 先写清"这是什么、什么材质、什么角度"，别跳步。
2. 补材质反光词和三点布光，这两层决定质感。
3. 背景写渐变+投影+虚化，别用纯白。

📌 记住：你糊弄 AI 一句"高级感"，AI 就糊弄你一张样板间。
