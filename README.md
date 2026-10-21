# Lany Avatar Skill

同一个 Lany 小生，多种视觉媒介。用 `$lany-avatar` 精修现有头像，或按风格名、编号生成一张候选。

当前默认身份入口仍是像素版；自然手绘是另一套内置参考。其他图片是风格样例，不代表用户已确认它们为新的默认头像。

本仓库独立打包 `lany-avatar` 技能，包含 10 类风格、12 张示例图及其规则；不包含 `lany-skills` 的其他技能或生成任务历史。

## 安装到 Codex

仓库名是 `lany-avatar-skill`，技能调用名仍是 `$lany-avatar`。本仓库根目录就是技能目录，无须再寻找嵌套的同名文件夹。

在 Codex 中发送：

```text
使用 $skill-installer，从 https://github.com/LanyXiaosheng/lany-avatar-skill 的 master 分支安装仓库根目录技能，安装名称使用 lany-avatar。
```

安装成功后，在下一轮通过 `$lany-avatar` 调用。已有同名技能时，应先备份并对比，再更新指定目录；不要静默覆盖自己的修改。不要把 Git 仓库的 `.git` 目录复制进技能安装目录。

## 快速使用

```text
使用 $lany-avatar，保留当前人物身份，风格 cel-anime，只生成一张头像。
使用 $lany-avatar，选择 07 简洁 3D 表情头像，睁眼自然挥手，不要合十。
使用 $lany-avatar，风格 storybook-3d，生成约三头身的全身小生。
```

只需精修当前图时，不必指定风格；直接附图说明要改的细节。默认一版，只有明确要求多风格或多版才增加输出。

风格编号是本技能的目录索引，不是命令行参数。画幅默认正方形；动作、表情、背景色和输出数量均以本次请求为准。

## 风格速查

| 编号 | 风格 ID | 风格 / 预览 | 常见交付 | 状态 |
| --- | --- | --- | --- | --- |
| 01 | [pixel](references/style-catalog.md#pixel) | [像素](assets/lany-avatar-reference.png) | 头像 | 当前默认身份参考 |
| 02 | [soft-handdrawn](references/style-catalog.md#soft-handdrawn) | [自然手绘](assets/lany-avatar-handdrawn-reference.png) | 头像 | 可选内置参考，非默认 |
| 03 | [cel-anime](references/style-catalog.md#cel-anime) | [赛璐璐动漫](assets/styles/cel-anime.png) | 头像 | 风格试样，待确认 |
| 04 | [designer-vinyl](references/style-catalog.md#designer-vinyl) | [3D 潮玩质感](assets/styles/designer-vinyl.png) | 头像 | 风格试样，待确认 |
| 05 | [screenprint](references/style-catalog.md#screenprint) | [丝网印刷](assets/styles/screenprint.png) | 头像 | 风格试样，待确认 |
| 06 | [storybook-3d](references/style-catalog.md#storybook-3d) | [温暖动画 3D / Q版](assets/styles/storybook-3d.png) | 头像；可明确要求全身 | 头像与全身均为待确认试样 |
| 07 | [emoji-3d](references/style-catalog.md#emoji-3d) | [简洁 3D 表情头像](assets/styles/emoji-3d.png) | 头像 | 挥手修订版，待确认 |
| 08 | [photo-style](references/style-catalog.md#photo-style) | [虚构人物写真风](assets/styles/photo-style.png) | 头像 / 人物肖像 | 虚构角色演绎，非本人照片 |
| 09 | [plush](references/style-catalog.md#plush) | [毛绒玩偶](assets/styles/plush.png) | 完整玩偶 | 玩偶视觉概念，未打样 |
| 10 | [flat-comic](references/style-catalog.md#flat-comic) | [扁平手绘漫画吉祥物](assets/styles/flat-comic.png) | 正面全身确认图 | 漫画入驻探针，待确认 |

下方图片均与各自风格和调用示例相邻，不把图片集中堆到文末。完整的媒介规则见 [风格目录](references/style-catalog.md)。

## 风格画廊

### 01 · 像素（pixel）

延续现有账号辨识度。**当前默认身份参考**；背景：满版主题黄绿。

<img src="assets/lany-avatar-reference.png" alt="像素风格样例" width="280">

```text
使用 $lany-avatar，风格 pixel，保留当前角色和主题色，精修镜框、耳机与发束，只生成一张头像。
```

[精细像素补充试样](assets/styles/pixel-fine.png)。此补充图仍是同一风格下的候选，不另算一种身份。

### 02 · 自然手绘（soft-handdrawn）

自然、柔和的手绘个人形象。**可选内置参考，非默认**；背景：满版雾蓝灰。

<img src="assets/lany-avatar-handdrawn-reference.png" alt="自然手绘风格样例" width="280">

```text
使用 $lany-avatar，风格 soft-handdrawn，自然墨线、雾蓝灰满版背景，不加腮红，只生成一张头像。
```

### 03 · 赛璐璐动漫（cel-anime）

清晰的动漫线条和色块。**风格试样，待确认**；背景：满版主题黄绿。

<img src="assets/styles/cel-anime.png" alt="赛璐璐动漫风格样例" width="280">

```text
使用 $lany-avatar，风格 cel-anime，清楚线条和两级色块阴影，自然闭口浅笑，只生成一张头像。
```

### 04 · 3D 潮玩质感（designer-vinyl）

立体材质、树脂收藏角色的展示。**风格试样，待确认**；背景：满版主题黄绿。

<img src="assets/styles/designer-vinyl.png" alt="3D 潮玩质感风格样例" width="280">

```text
使用 $lany-avatar，风格 designer-vinyl，正常少年比例、柔和哑光三维材质，只生成一张头像。
```

### 05 · 丝网印刷（screenprint）

有印刷颗粒与强图形感的形象。**风格试样，待确认**；背景：满版主题黄绿。

<img src="assets/styles/screenprint.png" alt="丝网印刷风格样例" width="280">

```text
使用 $lany-avatar，风格 screenprint，黑色块面、克制印刷颗粒，不放文字，只生成一张头像。
```

### 06 · 温暖动画 3D / Q版（storybook-3d）

故事感角色、活泼动作与 Q版延展。**头像与全身均为待确认试样**；背景：满版主题黄绿。

<img src="assets/styles/storybook-3d.png" alt="温暖动画 3D / Q版风格样例" width="280">

```text
使用 $lany-avatar，风格 storybook-3d，生成一个约三头身的全身小生，轻扶护目镜，肤色中性，不加腮红。
```

[全身 Q版试样（肤色修订版）](assets/styles/storybook-3d-character.png)。此补充图仍是同一风格下的候选，不另算一种身份。

### 07 · 简洁 3D 表情头像（emoji-3d）

聊天表情感、简洁亲和的三维头像。**挥手修订版，待确认**；背景：满版主题黄绿。

<img src="assets/styles/emoji-3d.png" alt="简洁 3D 表情头像风格样例" width="280">

```text
使用 $lany-avatar，风格 emoji-3d，睁眼、轻微侧头、自然挥手，收简发束和配饰，只生成一张头像。
```

### 08 · 虚构人物写真风（photo-style）

观察现有角色真人化后的摄影观感。**虚构角色演绎，非本人照片**；背景：满版主题黄绿。

<img src="assets/styles/photo-style.png" alt="虚构人物写真风风格样例" width="280">

```text
使用 $lany-avatar，风格 photo-style，把当前虚构小生演绎为成年青年写真风肖像，不当作本人真实照片。
```

### 09 · 毛绒玩偶（plush）

毛绒工艺观感与角色衍生。**玩偶视觉概念，未打样**；背景：满版主题黄绿。

<img src="assets/styles/plush.png" alt="毛绒玩偶风格样例" width="280">

```text
使用 $lany-avatar，风格 plush，生成一只完整毛绒小生，保留布制护目镜、银灰耳机和蓝色小绣标。
```

### 10 · 扁平手绘漫画吉祥物（flat-comic）

漫画信息图的简洁角色基准。**漫画入驻探针，待确认**；背景：满版暖米白。

<img src="assets/styles/flat-comic.png" alt="扁平手绘漫画吉祥物风格样例" width="280">

```text
使用 $lany-avatar，风格 flat-comic，只生成一张暖米白底的正面全身漫画确认图，不继续三视图或表情包。
```

## 固定身份与可变项

- 固定识别点：黑色蓬松短乱发、年轻自然脸型、头顶护目镜、颈挂银灰耳机、黑色连帽衫；已有蓝色小标记只在原图有依据且画幅可见时保留。
- 肤色自然中性浅米，避免橙红偏色、腮红和美颜式尖下巴；不能仅靠放大眼睛表示更可爱。
- 可变：绘画媒介、渲染材质、明确要求的动作表情与构图。风格不是换脸；参考样张中的某个动作也不是该风格的强制动作。
- 本轮明确指定的身份图优先于内置参考；风格样例只控制画法，不自动晋升为身份基准。本人照片用于身份还原时，以本人照片为准。

## 头像、全身形象与正式档案

- 说“头像”时默认头肩构图，检查完整方图以及 48px、96px 圆形裁切。
- 说“全身小人、Q版形象、完整玩偶”时展示完整身体与鞋底；未确认的裤鞋和身体细节须标明推断。
- `designer-vinyl` 是潮玩渲染质感；`storybook-3d` 的 Q版分支强调温暖动画和约三头身，不将两种比例混用。
- `emoji-3d` 是独立头像风格，不等于已经建立三视图和一整套漫画表情动作包。
- 正式漫画 IP DNA、正面确认图、三视图和八张独立表情动作图使用 `$comic-ip-onboarder`。只有各阶段通过用户确认后，才进入最终档案；本画廊的收录不代表通过。
- 文章正文手绘动作场景仍由 `$lany-handdrawn-ip` 等相应插图技能处理；这里负责人物身份、头像与角色试样。

## 精修与输出

已有图先局部编辑，提示词分开说明“保持不变”和“只修改”。例如只改肤色时，不改表情、脸型、动作和服装；用户觉得呆或不好看时，再针对实际可见的问题收简发束、调整视线或配饰。

最终图片须由实际图像生成或编辑工具产生，不能用代码占位图代替。保存最终图、完整提示词和本次 Style DNA，默认输出到项目的 `lany-assets/lany-avatar/<slug>/`；文件重名时另存版本。

本次整理的样例原图实际均为 1254×1254 PNG。曾请求 2048×2048，但工具没有返回该尺寸；没有用插值放大冒充原生高清。后续应报告实际文件尺寸，而不是把“高清”当作已验证结果。

## 候选状态与资源替换

- 默认像素参考：[lany-avatar-reference.png](assets/lany-avatar-reference.png)。
- 可选自然手绘参考：[lany-avatar-handdrawn-reference.png](assets/lany-avatar-handdrawn-reference.png)。
- `assets/styles/` 只收录本账号任务中生成的精选风格样例；未把外部创作者的原始参考截图打包进来。
- 已明确否定的合十版和早期大头公仔版不放进推荐画廊；本次不删除或恢复历史文件。
- 普通生成不替换技能资源，也不改账号头像。明确要求“更换默认资源”时，先备份再替换指定文件；不会自动同步到其他 Lany 技能。
- 写真风是虚构角色的真人化，不是本人照片；毛绒与潮玩是视觉概念，不是已经制造的实物。

## 技能文件

```text
lany-avatar-skill/
├── README.md                         风格预览与使用说明
├── SKILL.md                          运行入口与决策边界
├── agents/openai.yaml                调用入口的显示信息
├── references/
│   ├── style-dna.md                  固定身份与内置参考
│   └── style-catalog.md              编号、媒介规则与样例选择
└── assets/
    ├── lany-avatar-reference.png
    ├── lany-avatar-handdrawn-reference.png
    └── styles/                      精选风格样例与补充图
```

将仓库根目录中的技能文件整体安装到 `skills/lany-avatar/`，保留相对路径，不能只复制 README 而遗漏图片。[Style DNA](references/style-dna.md) 是身份规则，[风格目录](references/style-catalog.md) 是媒介规则；两者分开维护。
