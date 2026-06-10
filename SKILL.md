---
name: moon-design-system
description: MOON明月 个人品牌设计系统。用于制作知识分享类网页、小红书图文笔记、海报等一切设计输出。陶土橙+无印良品风+活人感。面向职场人和AI学习者的温暖知识传递。
---

# MOON明月 Design System

> 把知识做成好看的东西，让人愿意看下去。

---

## 触发条件

当用户要求：

- 做网页/Landing Page/教程页/知识页
- 做小红书图文/笔记/知识卡片/文章转卡片
- 做海报/封面/宣传图
- 做 MOON明月 风格的任何设计
- "帮我排版"、"做个页面"、"出个图文"

时自动触发。

---

## 使用方式（7步工作流）

### Step 1: 澄清需求

向用户确认：
1. **类型** — 网页/教程页？小红书图文？海报？无限画布？
2. **主题** — 做什么内容？AI教程？读书笔记？工具分享？
3. **受众** — 给谁看？（默认：职场人/AI学习者）
4. **素材** — 有哪些文案/截图/数据？
5. **硬约束** — 几屏/几张？有没有合作品牌？

如果用户给了足够信息，跳过已明确的问题，不要啰嗦。

### Step 2: 读规范

1. **必读** `brand-dna.md` — 品牌底层规范（颜色比例上限、字体、禁忌）
2. 根据类型选读场景文件：
   - 网页/教程/Landing → `references/scene-web.md`（含视觉惊喜规则）
   - 小红书图文/卡片 → `references/scene-cards.md`（含视觉惊喜规则）
   - 海报/封面 → `references/scene-poster.md`
   - 无限画布/知识地图 → `references/scene-canvas.md`

### Step 3: 选模板

从 `assets/` 选择对应模板骨架：
- 网页/教程 → `assets/template-web.html`
- 活动/Landing → `assets/template-landing.html`（新增）
- App/工具型 → `assets/template-app.html`（新增）
- 图文卡片 → `assets/template-cards.html`
- 海报 → `assets/template-poster.html`
- 无限画布 → `assets/template-canvas.html`

**从模板开始改，不从零写。**

### Step 4: 选布局组合

从 `references/layouts.md` 中选取布局模式。注意情绪节奏标签：

- 网页：选 3~6 种布局，每个 section 必须不同，**至少 1 个"打破节奏"类布局**（L06/L09）
- 图文：每张卡片选不同排版手法，**必须有 1 张"视觉惊喜"卡片**
- 海报：单版面布局
- 画布：见 `references/scene-canvas.md`，用区域（Zone）替代 section，位置即逻辑

### Step 5: 选组件填充

从 `references/components.md` 中选取组件。

**硬规则**：
- 禁止使用任何 HTML 默认样式（默认 blockquote、无样式列表、默认表格）
- 所有元素必须使用组件库中的样式
- 优先使用新增组件（书卡#13、聊天气泡#14、日历标记#15）增加辨识度

### Step 6: 自检

对照 `references/checklist.md` 逐条检查。

- **P0 必须全过** — 任何一条不过就改
  - 特别注意新增的反 AI 味检验：是否有"不完美"元素？是否避免了全站模板感？截图会不会被认出是模板？
- **P1 尽量过** — 提升品质
  - 特别注意：是否有 1 处视觉惊喜？
- **P2 加分** — 锦上添花

### Step 7: 交付

输出最终 HTML 文件，确保：
- 可直接在浏览器打开
- 响应式（至少适配 768px 断点）
- 图文卡片可一键导出 PNG（1080×1440）
- 无限画布支持节点连接、节点拖拽、内容编辑、localStorage 保存
- 有 1 处视觉惊喜，但不花哨

---

## 场景速查

| 类型 | 场景文件 | 模板 |
|------|----------|------|
| 网页/教程 | `references/scene-web.md` | `assets/template-web.html` |
| 活动/Landing | `references/scene-web.md` | `assets/template-landing.html` |
| App/工具型 | `references/scene-web.md` | `assets/template-app.html` |
| 小红书图文/笔记 | `references/scene-cards.md` | `assets/template-cards.html` |
| 海报/封面 | `references/scene-poster.md` | `assets/template-poster.html` |
| 无限画布/知识地图 | `references/scene-canvas.md` | `assets/template-canvas.html` |

---

## 核心原则

1. **活人做的，不是 AI 模板** — 有手绘元素、有不规则、有温度、有 1 处视觉惊喜
2. **无印良品感** — 克制、留白、呼吸空间、信息清晰
3. **陶土橙是唯一主色** — 温暖但不刺眼，占比 25-35%，不超过 45%
4. **内容为王** — 设计服务于知识传递，不是炫技
5. **乐观积极** — 任何设计都要传递"你也能做到"的感觉
6. **限制即自由** — 颜色有上限、布局有情绪标签、组件有优先级，约束保证品质

---

## 文件结构

```
moon-design-system/
├── SKILL.md                     ← 本文件（工作流）
├── brand-dna.md                 ← 品牌基因（含色彩比例上限）
├── README.md                    ← 使用说明 + Fork指南
├── assets/
│   ├── template-web.html        ← 网页模板（教程/知识页）
│   ├── template-landing.html   ← 活动页模板（新增）
│   ├── template-app.html       ← App/工具型模板（新增）
│   ├── template-cards.html      ← 图文卡片模板
│   ├── template-poster.html     ← 海报模板
│   ├── template-canvas.html     ← 无限画布模板
│   └── avatar.jpg               ← IP头像
└── references/
    ├── layouts.md               ← 12种布局模式（附情绪标签）
    ├── components.md            ← 15个组件库（新增3个）
    ├── checklist.md             ← 质量清单（含反AI味检验）
    ├── scene-web.md             ← 网页场景规范（含视觉惊喜规则）
    ├── scene-cards.md           ← 图文卡片场景规范
    ├── scene-poster.md          ← 海报场景规范
    └── scene-canvas.md          ← 画布场景规范
```
