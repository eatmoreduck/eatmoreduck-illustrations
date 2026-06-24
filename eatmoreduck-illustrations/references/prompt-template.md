# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

注：下面 `{{character}}` 处请替换为 `references/eatmoreduck-ip-rubberduck.md` 里的英文角色描述段。只有当用户明确要求上一版 `mixed` 候选时，才使用 `references/eatmoreduck-ip-mixed.md`。不再使用旧 dark/yellow 颜色变体。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten Chinese annotations. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
{{character}}
The 多吃鸭 (eatmoreduck) must perform the core conceptual action, not decorate the scene. Make it serious, deadpan, and slightly bizarre, not cute, not a toy sticker, not a children's cartoon duck.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：多吃鸭在哪里、正在做什么（吞/嚼/吐/滤等吃主题动作）、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
Black for main line art; the duck (多吃鸭) follows the selected character reference and uses a solid dark-grey or near-black duck body with a short wide flat orange duck bill and orange webbed feet. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Use only the requested short Chinese labels; do not invent long explanatory sentences. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not draw extra ducks inside thumbnails, diagrams, or background details unless explicitly requested; 多吃鸭 should be the only duck character in the image. Do not draw 多吃鸭 as a fish, submarine, torpedo, long capsule, or pill-shaped animal; no fins and no fish tail. Do not give 多吃鸭 fingers, claws, paw pads, cat paws, curled hook hands, split tips, or independent arms; side wings must remain smooth duck wing patches attached to the body. Do not recreate any specific public-art rubber duck, giant water installation, city/water photo scene, or photorealistic toy. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强怪诞感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make 多吃鸭 (eatmoreduck) more central to the conceptual action. 多吃鸭 should be eating/digesting/spitting the materials that explain the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, and not cute.
```
