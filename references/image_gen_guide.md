# 生图调用指南（摄影写实图）

本技能功能 1 通过生图工具（ImageGen / 平台生图能力）生成逼真摄影图像。以下为调用要点。
**必须先读 `pro_prompt_framework.md`**：所有提示词都按六维框架（构图/主体站位/打光/道具/色调/技术）组装，打光维度强制用四层打光公式。

## 0. 模型感知（先读，避免白忙）

> ★ **本技能推荐首选引擎：腾讯混元 Hy Image 3.5 preview**（2026-09-22 发布，已接入 WorkBuddy / 元宝 / ima / Miora / WorkRally / OnSolo）。在 WorkBuddy 环境调用生图即走此模型。相比 Agnes/Flux 类，它的最大优势：**文字渲染准**（商业海报/产品标签/封面上的字不再乱码缺笔）、**多轮对话连续改图**（基于历史上下文局部编辑，不用每次重生成）、**最高 2K 输出**、**免费/低成本路径多**。下文分引擎策略中把它作为首选参考。

### 免费与低成本路径（Hy Image 3.5 preview）
- **免费**：元宝 APP（「创作」页，人像编辑/智能P图/旅游规划图/知识信息图）、ima copilot（发出生图指令，把知识库变图/网页/PPT）、WorkBuddy（已含，作为办公工作台生图引擎）。
- **限时免费**：Miora / WorkRally / OnSolo 专业影视/创意工具两周免费（OnSolo 新用户注册送 110 张）。
- **付费低成本**：腾讯云 TokenHub API 0.15 元/2K 图，仅对输出图收费，13 款主流模型中单张 2K 成本最低。
- **排除/负向词策略**：chat 格式，直接用自然语言指令排除（"不要文字/不要模糊"），多轮编辑时直接说"把 XX 去掉"即可；若引擎暴露负向字段，可少量加通用质量负向（见第 6 节）。无需像 Flux 那样把负向翻成正向描述。
- **对摄影技能的价值**：文字渲染强 → 解决商业海报/产品标签/封面文字痛点（Agnes 弱项）；多轮编辑 → 天然适配单变量迭代（改一处接着上一轮）；2K → 直接出可发布成品。

不同生图引擎对「负向词、画幅参数、色彩偏置」的支持差异巨大。写之前先确认你用的是什么引擎，否则按错方法写会直接白给。

- **Hy Image 3.5 preview（推荐首选）**：见上方 blockquote 与「免费与低成本路径」。chat 多轮格式，自然语言排除即可，无需传统负向词字段。
- **Flux 类（含多数开源/平台部署，如 Agnes 底层若为 Flux）**：**不支持原生负向词**。别写 `negative_prompt`，把「不要什么」翻成正向描述（例如不要 `no text`，改写 `clean surface, no text overlay`）。且 Flux 默认偏**青橙电影色**，想去掉要靠后期 LUT，提示词难根除。
- **Midjourney**：用 `--no 文本,模糊` 排除，不支持长列表加权；色彩标签（teal and orange）在 MJ 上反而好用。
- **DALL·E / GPT 生图**：无独立负向字段，必须在主提示词里间接排除（"a clear image without any text or blur"）。
- **SDXL**：少量精准负向词即可，长列表反拖垮。
- **通用最稳策略**：无论什么引擎，**先把「要什么」写具体**，负向词只当兜底，别指望它解决结构问题。

## 1. 额度提醒（必须）
生成前明确告知用户：**生图每张约消耗 5–10 credits**。用户确认后再调用。

## 2. 与六维框架 + 四层打光公式联动（核心）
- 写提示词前，先按六维框架逐维填空；打光维度必须落到四层：
  - L1 主体锚定光：`left-top key light`（光从哪来）
  - L2 材质反光词（命门）：glass translucent / metallic reflection / matte drape / oil sheen / skin pores
  - L3 三点布光：`left-top key light, soft fill from lower right, rim light from front`
  - L4 背景景深：`light gray gradient background, soft shadow under subject, background slightly blurred`
- **铁律**：绝不用"高级感/质感好/科技感"等形容词代替具体光位和材质词。形容词 = 样板间死光。
- 万能填空生成器见 `pro_prompt_framework.md` 末尾，可直接套。

## 3. 提示词语言
- **主提示词用英语**：写实摄影模型对英文摄影术语（lens, aperture, bokeh, golden hour, Kodak Portra）理解最好。
- **可追加中文风格说明**作为注释，但传给模型的 prompt 以英文为主。
- 参考 `still_life_prompts.md` / `portrait_prompts.md` / `landscape_prompts.md` / `humanity_macro_prompts.md` 的英文模板。

## 4. 写实感关键词（建议必带）
- 镜头：`35mm / 50mm / 85mm / 24mm wide / 100mm macro`
- 光圈：`f/1.8 / f/2.8 / f/8`（控制景深）
- 光线：`golden hour / natural window light / rim light / soft overcast / neon`
- 胶片感：`Kodak Portra 400 / film grain / high key`
- 画质：`photorealistic / sharp / high dynamic range / cinematic`

## 5. 画幅参数（--ar）
| 题材 | 画幅 | 说明 |
|---|---|---|
| 人像竖构 | 3:4 或 2:3 | 适配手机竖屏 |
| 风景横构 | 16:9 或 3:2 | 桌面/横屏 |
| 微距 / 方形 | 1:1 | 小红书方图 |
| 城市夜景 | 16:9 | 全景感 |

> 具体模型是否支持 `--ar` 以 ImageGen 实际参数为准；若不支持，用相近比例描述（如 "vertical composition"）。

## 6. 负向词与排除策略（按引擎与题材）
通用质量负向（多数引擎可用）：`cartoon, anime, illustration, painting, 3d render, deformed hands, extra fingers, blurred, low quality, watermark, text, logo, oversaturated`。

⚠️ **Flux 类引擎不支持原生负向词**（见第 0 节）。遇到这类引擎，把下面各题材的「排除项」改写成正向描述（例：人像「不要塑料皮」→ 主提示词写 `visible skin texture, natural pores, realistic skin`）。

**分题材负向词库（供支持负向词的引擎直接抄）**：
- **人像 portrait**：`extra fingers, missing fingers, fused fingers, deformed hands, plastic skin, waxy skin, over-smoothed skin, bad anatomy, asymmetric eyes, oversaturated`
- **产品 product**：`cheap looking, floating product, wrong shadows, messy reflections, harsh glare, distracting background, fingerprints, scratches`
- **风光 landscape**：`people, power lines, urban, buildings, CGI, 3d render, oversaturated, HDR effect, fake looking`
- **通用 general**：`blurry, low quality, jpeg artifacts, watermark, text, deformed, extra limbs`

> 负向词别堆太长（3–6 个精准项 > 一长串），否则画面发灰发平。优先用正向描述解决结构问题。

## 7. 迭代策略
生图不满意时按以下顺序调（优先光和色，其次构图）：
1. **光线不对** → 改 golden hour / rim light / soft overcast，检查四层打光是否写具体。
2. **太假** → 加 `film grain` / `subtle grain` / `photorealistic` 强化，补 L2 材质反光词。
3. **构图乱** → 明确镜头焦段与 `negative space` / `symmetrical` / `rule of thirds`。
4. **主体歪** → 在负向词加 `deformed, extra fingers`（人像）。
5. 仍不行 → 换风格模板或降低复杂度（减少环境元素）。

## 8. 回传规范
生成后必须向用户回传：
- 实际使用的**英文提示词**（含负向词）
- 画幅
- 推荐实拍参数（镜头/光圈/光线），方便用户用真相机复刻

## 9. 单变量迭代与种子一致性
- **单变量迭代法**：每次只改一个维度（光/色/构图/材质）的措辞，其他完全不变，对比出图判断这一处改动有没有效。一次改多处，好了也不知道是哪个改对的。
- **种子 seed**：需要同一主体多张一致（电商套图、系列图）时，固定 seed 再微调提示词，可做 A/B 对比。确定最优组合后把该 seed 钉死，后续复刻用。
- **参数参考**：CFG/引导值 5–8 平衡（过高易过饱和、塑料感）；步数 50–75 保细节；这些仅在引擎暴露参数时调整。
- 详见 `references/ecommerce_batch.md`（套图批量一致性工作流）。

## 10. 产品标签文字可读性
AI 对产品标签、包装上的**可读文字**极易写错（乱码、幻觉字母）。处理原则：
- 需要真实字样（品牌名、成分表）→ **主提示词写「无文字、纯表面」**，生成干净图后，用 Canva/PS 等设计软件后期加字。
- 必须保留标签位置 → 只描述标签的「位置与颜色」，**不要写实际单词**进提示词。
- 反向排除加 `text, watermark, logo, label text`（支持负向词的引擎）。
