# 专业摄影提示词六维框架（核心引擎）

把"高级感、有质感、大片感"这类形容词，翻译成摄影师真正能控制、AI 也能精确执行的东西。
任何一张专业照片，都能拆成下面六个维度。打光维度由「四层打光公式」驱动，是质感的命门。

> 用法：先定题材（静物/人像/风光/微距/人文），再从六维逐条填空，最后按"组装规则"拼成英文提示词丢给生图模型。
> 配 `still_life_prompts.md` / `portrait_prompts.md` / `landscape_prompts.md` / `humanity_macro_prompts.md` 分题材取模板。

---

## 维度一 · 构图 Composition

决定视线往哪走、主体站哪。

| 中文 | 英文关键词 | 适用 |
|---|---|---|
| 三分法 | rule of thirds | 通用 |
| 引导线 | leading lines | 风光/建筑/道路 |
| 留白 | negative space | 极简/产品/人像 |
| 框架式构图 | framing / frame within frame | 人文/窗/门洞 |
| 对称构图 | symmetrical composition | 建筑/倒影 |
| 对角线 | diagonal composition | 动态/产品 |
| 黄金分割 | golden ratio | 人像/艺术 |
| 前景兴趣点 | foreground interest | 风光/层次 |
| 中心构图 | centered composition | 产品/静物主体 |

## 维度二 · 主体与姿势站位 Subject & Pose / Positioning

**主体锚定（所有题材必写）**：清楚交代"是什么、什么材质、什么颜色、什么角度"。
别写"一瓶精华"，写"30ml 琥珀色磨砂玻璃精华瓶、45度俯拍"。

**人像姿势站位（portrait 用）**：
- 站姿 relaxed standing / 倚靠 leaning against wall / 坐姿 seated / 侧身 three-quarter turn
- 回眸 looking back over shoulder / 低头 looking down / 眼神朝光 eye toward light
- 手部动作 hand on face / hands in pockets / holding prop

**产品摆放（still life 用）**：45度俯拍 45-degree top-down / 平视微俯 eye-level slightly above / 顶拍 flat lay / 间距 spacing。

**层次站位（风光/人文用）**：前景 foreground / 中景 midground / 背景 background 三层拉开纵深。

## 维度三 · 打光光线 Lighting —— 四层打光公式（命门）

> 高级感不来自形容词，来自光位和材质词。你写"高级感"，AI 理解成默认死光；你写"左上主光加右下方补光加底部反光"，AI 才知道这东西该怎么被看见。

**第一层 · 主体锚定光**：光打在谁身上、从哪来。写清主光方向。
**第二层 · 材质反光词（最关键的命门）**：拉开质感的核心。
- 玻璃 glass：translucent, edge highlight, internal refraction
- 金属 metal：cool mirror reflection, brushed texture, specular
- 织物 fabric：matte, soft drape, natural fold shadow
- 皮肤 skin：soft subsurface, visible pores, natural texture
- 水/液体 liquid：oil sheen, condensation droplet, steam
- 食物 food：appetizing glisten, caramelized edge, crumb texture

**第三层 · 三点布光**：主光 key + 补光 fill + 轮廓光 rim。
英文直写：`left-top key light, soft fill from lower right, rim light from front`。
**第四层 · 背景与景深**：别写纯白，写渐变+投影+虚化。
`light gray gradient background, soft natural shadow under subject, background slightly blurred`。

**常用光源词（按情绪选）**：
golden hour（暖、治愈）/ window light（柔、居家）/ softbox（棚拍柔光）/ rim light（勾边）/ backlight（逆光发丝光）/ overcast（柔光平光）/ neon（赛博）/ candlelight（暖、私密）/ studio strobe（时尚硬光）/ raking light（微距纹理，侧掠光）。

**打光修饰语（控制光质，越具体越专业）**：
- 柔光类：`softbox`（棚拍柔光）/ `beauty dish`（美妆人像专用，柔中带对比）/ `octabox`（大面积柔光）/ `large softbox reflection` / `soft fill lighting`
- 硬光/利落类：`hard directional light` / `Rembrandt lighting`（经典人像三角光）/ `crisp edge lighting` / `precise specular highlights`
- 环境类：`natural window light` / `overcast natural` / `bounce light`（反光板补光）/ `scrim`（柔光屏）

**阴影控制（商业产品图命门，别只写「柔和阴影」）**：
- `contact shadow directly beneath`（接触阴影，产品落地感）
- `soft drop shadow falling to [方向]`（定向柔投影，带纵深）
- `dramatic cast shadow with defined edges`（硬边投射，高级/编辑感）
- `subtle mirror reflection beneath product`（镜面倒影，玻璃/亚克力/抛光面）
- `no shadow, isolated product`（无影悬浮，用于抠图合成）
- 方向必须与主光一致：`consistent with [lighting direction]`。

## 维度四 · 搭配道具 Props & Styling

衬托主体的小物与氛围元素，决定"这是不是一个真实场景"而非棚拍样板间。
- 台面 texture surface：linen 亚麻 / marble 大理石 / wood grain 木纹 / concrete 水泥
- 氛围元素：steam 蒸汽 / condensation 水珠 / smoke 烟雾 / petals 花瓣 / books 书
- 规则：道具服务于主体，不抢戏；色调与主体统一。

## 维度五 · 色调色彩 Color & Grade

| 中文 | 英文 | 情绪 |
|---|---|---|
| 低饱和莫兰迪 | muted tones / desaturated | 高级、克制 |
| 暖调 | warm tones | 治愈、食欲 |
| 冷调 | cool tones | 科技、疏离 |
| 青橙调 | teal and orange | 电影感 |
| 高调 | high key | 明亮、清新 |
| 暗调 | low key | 沉静、电影 |
| 黑白 | monochrome / B&W | 纪实、 timeless |
| 胶片色 | Kodak Portra 400 / Fuji Pro 400H / Cinestill 800T | 复古、真实 |

**胶片替代逻辑（维度五的颜色秘诀）**：
别写「暖色调/冷色调」这种泛标签，模型会自己发挥漂移。改用**具体胶片型号**当色彩快捷键，模型对其训练数据有精准认知：
- 想暖、自然肤色 → 写 `shot on Kodak Portra 400`（而非 warm tones）
- 想冷、日系 → 写 `Fuji Pro 400H`（绿调阴影、柔和）
- 想夜景红晕光 → 写 `CineStill 800T`（钨丝平衡、高光 halo 光晕）
- 想高饱和风景 → 写 `Kodak Ektar 100`
- 想复古消费品 → 写 `Kodak Gold 200`
- 想黑白硬调 → 写 `Kodak Tri-X 400`（重颗粒、高反差）

**模拟质感效果（加真实瑕疵，反而更真）**：
`film grain`（颗粒）/ `light leak`（漏光暖斑）/ `halation`（高光泛光，CineStill 标志）/ `vignetting`（暗角）/ `scanned film negative`（扫描负片，自带真实瑕疵）/ `expired film colors`（过期胶片偏色）。

📌 完美画面往往显假，可控的不完美才像真拍的。

## 维度六 · 技术参数 Technical

- **镜头 lens**：14mm（星空）/ 24mm（风光广角）/ 35mm（人文环境）/ 50mm（标准）/ 85mm（人像压缩）/ 100mm macro（微距）/ 105mm（产品）
- **光圈 aperture**：f/1.4–f/2.8（虚化人像）/ f/4–f/5.6（环境人像）/ f/8（风光清晰）/ f/11（长曝丝滑）
- **画质**：photorealistic, sharp focus, high dynamic range, subtle film grain, 8k product photography
- **画幅 --ar**：人像 3:4 / 2:3，风光 16:9 / 3:2，微距/产品 1:1，全景 16:9

---

**可控瑕疵层（专业级真实感的关键，默认加）**：
完美图常显假。在提示词末尾补可控不完美，质感立刻落地：
- 人像：`visible skin texture, natural pores, slight flyaway hairs`
- 织物：`natural fabric wrinkles, visible weave`
- 环境：`subtle dust in light rays, weathered surface, aged texture`

**矛盾指令警告（新手最常翻车）**：
同一句里别又软光又硬阴影、又平光又强对比，模型会卡在中间出平庸图。写完后自查：光质（软/硬）与阴影（柔/锐）是否自洽；材质词与光源是否匹配（玻璃要通透高光，金属要冷反光，织物要哑光）。

## 万能填空式生成器（Universal Builder）

把六维按顺序填空，再拼成英文：

```
[维度二 主体+材质+角度], [姿势/摆放],
[维度一 构图],
[维度三 打光 L1-L4],
[维度四 道具台面],
[维度五 色调胶片],
[维度六 镜头/光圈/画质], --ar [画幅]
```

**填好的范例（静物·精华瓶）**：
> 30ml amber frosted glass serum bottle, 45-degree top-down view,
> rule of thirds with negative space,
> left-top key light shaping volume, soft fill from lower right lifting shadows, front rim light outlining edge, glass translucent with edge highlight and internal liquid refraction,
> light gray gradient surface, soft natural shadow under bottle, background slightly blurred,
> muted warm tones, Kodak Portra 400 look,
> 105mm macro lens, f/5.6, photorealistic, sharp focus, 8k product photography --ar 1:1

**组装规则**：
1. 主提示词用英文，模型对英文摄影术语（lens / aperture / bokeh / golden hour）理解最好。
2. 材质反光词和三点布光必须写具体，这是质感命门，绝不能用"高级感/质感好"代替。
3. 永远带负向词（见 `image_gen_guide.md`）：cartoon, anime, illustration, 3d render, deformed, low quality, watermark, text, oversaturated。
4. 生图不满意，优先调维度三（光）和维度五（色），其次维度一（构图）。
