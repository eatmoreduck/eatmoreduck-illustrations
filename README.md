# Eatmoreduck Illustrations

> 把中文文章里的判断、流程、状态和隐喻，变成一张张白底、手绘、怪诞但清爽的正文配图。
>
> 16:9 横版 | 多吃鸭 IP | 纯白手绘 | 少量红橙蓝中文批注 | Codex Skill

---

## 这个仓库是什么

Eatmoreduck Illustrations 是一个 Codex Skill，用来指导 AI Agent 为中文文章、帖子、博客、Notion 文档和方法论内容生成正文配图。

它不是通用插画 prompt，也不是 PPT 信息图模板。它的核心目标是：先理解文章里的认知锚点，再把其中一个判断、流程、结构、状态或隐喻，变成一张有记忆点的 16:9 手绘解释图。

默认视觉 IP 是“多吃鸭”：一只 Fluent Emoji 风格的鸭子——扁嘴朝右、圆润饱满、轮廓略不规则带手绘感，黑色圆点眼睛、表情空呆冷静。它的核心动作围绕“吃 / 消化 / 吞吐”展开（呼应名字“多吃鸭”），是一个正在认真参与系统运转的荒诞工作者。多吃鸭不是吉祥物，不是贴纸，也不是站在角落里的装饰物。

一句话：**让 AI 不只是“配一张图”，而是把文章里的一个关键认知动作画出来。**

---

## 适合谁用

特别适合：

- 写中文文章，需要正文配图和文章插图的人
- 做知识型内容、方法论内容、AI 工作流内容的人
- 想把抽象判断画成具体隐喻的人
- 想要一种比 PPT 信息图更轻、更怪、更有个人识别度的配图风格的人
- 用 Codex 做内容生产，希望稳定复用一套视觉语言的人

不适合：

- 想要商业插画、品牌 KV 或精致扁平插画的人
- 想要传统 PPT 信息图、复杂架构图或流程图的人
- 想要儿童卡通、可爱 IP、表情包风格的人
- 想把大量正文、长段解释或完整课程页塞进一张图里的人
- 需要严格可编辑矢量源文件的人

---

## 它会产出什么

默认输出：

- 16:9 横版正文配图
- 一篇文章的 4-8 张 shot list
- 每张图的主题、核心意思、结构类型、多吃鸭动作和中文标注建议
- 最终 PNG 图片，保存到 workspace 的 `assets/<article-slug>-illustrations/`

默认不输出：

- PPTX / PDF / Keynote
- SVG / HTML / Canvas 可编辑图
- 商业海报或封面 KV
- 大段文字型信息图

---

## 视觉风格

这个 skill 默认使用“多吃鸭怪诞正文配图”风格：

- 纯白背景，不要纸纹、米色、阴影、渐变
- 黑色手绘线稿，细线，轻微抖动
- 大量留白，主体只占画面约 40%-60%
- 少量红色、橙色、蓝色中文手写批注
- 一张图只表达一个核心动作、结构、状态或隐喻
- 多吃鸭必须参与核心动作（吃 / 消化 / 吞吐），不能只是装饰
- 怪诞、有创意、清爽，但不幼稚、不卖萌

---

## 三个颜色变体

多吃鸭有 3 个颜色变体，外形一致、仅配色不同，供你挑选最合适的风格：

| 变体 | 取值 | 身体 | 扁嘴 / 脚蹼 | 说明 |
|---|---|---|---|---|
| A（默认） | `dark` | `#212121` 深灰实心 | 白色扁嘴 | 与 favicon 一致，白底对比最强 |
| B | `mixed` | `#212121` 深灰实心 | 橙色扁嘴 + 橙色脚蹼 | 主体保对比，加鸭子色彩信号 |
| C | `yellow` | `#FFD23F` 黄色实心 + 黑色细描边 | 橙色扁嘴 + 橙色脚蹼 | 经典小黄鸭，暖色明快 |

调用时指定变体即可，未指定默认 `dark`。

---

## 示例效果

> 注：以下示例图来自原始 Ian Xiaohei Illustrations 风格样片，仅作风格校准（线条密度、留白、颜色克制），不代表多吃鸭最终形象。使用时应该从当前文章重新发明隐喻，不要照抄旧案例的物件和构图。

### 两个断点

![两个断点](examples/images/01-two-breakpoints.png)

### 按目的分拣

![按目的分拣](examples/images/02-sort-by-purpose.png)

### 一鱼多吃

![一鱼多吃](examples/images/03-one-fish-many-uses.png)

### 承接路径

![承接路径](examples/images/04-handoff-path.png)

### 信息井

![信息井](examples/images/05-information-well.png)

### 想法压机

![想法压机](examples/images/06-idea-press.png)

### 内容发酵

![内容发酵](examples/images/07-content-fermentation.png)

### 信任桥

![信任桥](examples/images/08-trust-bridge.png)

---

## 安装

克隆仓库：

```bash
git clone https://github.com/eatmoreduck/eatmoreduck-illustrations.git
cd eatmoreduck-illustrations
```

复制 skill 到 Codex skills 目录：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./eatmoreduck-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

安装后，在 Codex 里使用：

```text
Use $eatmoreduck-illustrations 为这篇中文文章设计并生成 5 张多吃鸭怪诞正文配图。
```

---

## 怎么用

### 只做配图规划

```text
Use $eatmoreduck-illustrations 先不要生图。
请分析下面这篇文章哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、主题、核心意思、结构类型、多吃鸭在做什么、建议中文标注词。

<粘贴文章>
```

### 直接生成正文配图

```text
Use $eatmoreduck-illustrations 把下面这篇文章生成 4 张多吃鸭怪诞正文配图。
要求：16:9 横版、纯白背景、黑色手绘线稿、少量红橙蓝中文手写批注。

<粘贴文章>
```

### 指定颜色变体

```text
Use $eatmoreduck-illustrations 用 yellow 变体，把下面这篇文章生成 4 张多吃鸭正文配图。

<粘贴文章>
```

### 为单个概念生成一张图

```text
Use $eatmoreduck-illustrations 为“信任不是喊出来的，而是一块证据一块证据铺过去”生成一张正文配图。
画面要怪诞但清爽，多吃鸭必须承担核心动作（吞 / 嚼 / 吐 / 滤等）。
```

### 去掉图里的标题或错误文字

```text
Use $eatmoreduck-illustrations 帮我编辑这张图，去掉左上角的“流程图”标题，其他内容保持不变。
```

更多示例见 [examples/prompts.md](examples/prompts.md)。

---

## 工作流程

这个 skill 的流程是：

1. 读取文章、Markdown、Notion 内容、截图或用户给的主题
2. 提炼核心观点、认知转折、流程结构和适合视觉化的段落
3. 先输出 shot list：每张图只选一个认知锚点
4. 为每张图选择结构类型：Workflow、系统局部、前后对比、角色状态、概念隐喻、方法分层、地图路线或小漫画分镜
5. 重新发明一个低科技、怪诞但成立的物理隐喻
6. 让多吃鸭承担核心动作（吃 / 消化 / 吞吐主题）
7. 每张图单独调用图像模型生成
8. 按 QA checklist 检查：白底、留白、多吃鸭动作、中文标注、非 PPT 感、非旧案例复刻
9. 保存最终 PNG，并报告用途和路径

---

## 目录结构

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   └── prompts.md
└── eatmoreduck-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── eatmoreduck-ip-dark.md
        ├── eatmoreduck-ip-mixed.md
        ├── eatmoreduck-ip-yellow.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

真正需要安装到 Codex 的是子目录：

```text
eatmoreduck-illustrations/
```

根目录的 README、LICENSE、NOTICE 和 examples 是 GitHub 分享文档。

---

## 注意事项

- 图片里的中文文字越短越稳定。
- 每张图只讲一个核心结构，不要把文章做成说明书。
- 多吃鸭必须承担核心动作；如果去掉多吃鸭画面仍然完全成立，说明多吃鸭太装饰了。
- 示例图只用于校准线条密度、留白、颜色克制和角色参与方式，不要复刻构图。
- AI 图像模型可能出现错字、幻觉标签、风格漂移或多余标题，生成后需要检查。
- 如果中文错字严重，优先减少标注词并重生成。

---

## 致谢

本仓库 fork 自 [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，由 Ian 创作。在原“小黑”IP 和风格 DNA 基础上，替换为“多吃鸭 (eatmoreduck)”IP，并新增三个颜色变体。感谢原作者开放这套优秀的配图方法论。详见 [NOTICE.md](NOTICE.md)。

---

## License

MIT License. See [LICENSE](LICENSE).
