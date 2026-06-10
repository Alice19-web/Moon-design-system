# 布局模式库 — MOON明月

> 12 种经过验证的布局。每次做设计从这里选，不自由发挥。

---

## L01 · Hero 双栏不对称

**情绪标签**：开场 · 建立信任 · 温和引入
**适用**：首屏、产品介绍、教程入口

```css
.hero-split {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  align-items: center;
  gap: clamp(32px, 4vw, 64px);
  padding: clamp(60px, 10vh, 120px) clamp(24px, 4vw, 48px);
  max-width: 1100px;
  margin: 0 auto;
}
@media (max-width: 768px) {
  .hero-split { grid-template-columns: 1fr; }
}
```

**使用提示**：左文右图或左图右文，文字区左对齐，不要全居中。留白 ≥ 40%。

---

## L02 · Hero 单栏居中

**情绪标签**：开场 · 极简冲击 · 一击即中
**适用**：活动页首屏、极简标题页、金句开场

```css
.hero-center {
  text-align: center;
  padding: clamp(80px, 14vh, 160px) clamp(24px, 4vw, 48px);
  max-width: 800px;
  margin: 0 auto;
}
.hero-center h1 {
  font-size: clamp(2.4rem, 6vw, 4.5rem);
  font-weight: 800;
  color: #5D4E47;
  line-height: 1.3;
  margin-bottom: 0.5em;
}
```

**使用提示**：文字要极其精炼，大标题 + 一句话副标题 + CTA 即可。不要堆信息。

---

## L03 · Sticky 侧栏 + 滚动内容

**情绪标签**：正文 · 长文阅读 · 导航陪伴
**适用**：长教程、多步骤内容、知识点展开

```css
.layout-sticky {
  display: grid;
  grid-template-columns: 0.3fr 1fr;
  gap: clamp(40px, 5vw, 80px);
  max-width: 1100px;
  margin: 0 auto;
  padding: 60px 24px;
  align-items: start;
}
.sticky-nav {
  position: sticky;
  top: 80px;
}
@media (max-width: 768px) {
  .layout-sticky { grid-template-columns: 1fr; }
  .sticky-nav { position: static; }
}
```

**使用提示**：侧栏只放导航锚点，不要放过多内容。正文区保持 65ch 最佳行宽。

---

## L04 · 三等分卡片网格

**情绪标签**：正文 · 信息概览 · 并列展示
**适用**：核心价值展示、功能列表、要点概览

```css
.card-grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: clamp(20px, 2.5vw, 32px);
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 24px;
}
@media (max-width: 768px) {
  .card-grid-3 { grid-template-columns: 1fr; }
}
```

**使用提示**：连续使用不超过 1 次。如果前面用过网格，下一个 section 必须换布局。

---

## L05 · 纵向步骤流程线

**情绪标签**：正文 · 流程引导 · 渐进展开
**适用**：安装教程、操作步骤、学习路径

```css
.steps-vertical {
  display: flex;
  flex-direction: column;
  gap: clamp(32px, 4vw, 56px);
  padding-left: 56px;
  position: relative;
  max-width: 720px;
  margin: 0 auto;
}
.steps-vertical::before {
  content: '';
  position: absolute;
  left: 20px;
  top: 40px;
  bottom: 40px;
  width: 2px;
  border-left: 2px dashed #E8C4B0;
}
.step-item {
  position: relative;
}
.step-item::before {
  content: '';
  position: absolute;
  left: -44px;
  top: 8px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #bc4528;
}
```

---

## L06 · 全宽深色面板

**情绪标签**：节奏 · 打破沉闷 · ⚡ 视觉惊喜
**适用**：金句引用、核心观点、代码展示（打破奶白底的节奏）

```css
.dark-panel {
  background: #3D342F;
  color: #F4F1ED;
  padding: clamp(60px, 8vh, 120px) clamp(24px, 4vw, 48px);
  margin: clamp(40px, 6vh, 80px) 0;
}
.dark-panel h2 {
  color: #E8C4B0;
}
.dark-panel .highlight {
  color: #bc4528;
}
```

**使用提示**：全页最多 1 处。深色面板前后必须有足够留白（≥ 80px），形成呼吸感。

---

## L07 · 横向步骤连接线

**情绪标签**：正文 · 流程概览 · 横向推进
**适用**：3-5 步流程横排、对比展示

```css
.steps-horizontal {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 16px;
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 24px;
  position: relative;
}
.steps-horizontal::before {
  content: '';
  position: absolute;
  top: 56px;
  left: 10%;
  right: 10%;
  height: 2px;
  background: linear-gradient(to right, #E8C4B0, #bc4528, #E8C4B0);
}
.step-h-item {
  text-align: center;
  flex: 1;
  position: relative;
  z-index: 1;
}
```

---

## L08 · 中轴时间线交错

**情绪标签**：正文 · 对比/历程 · 时间叙事
**适用**：里程碑展示、内容对比、Before/After

```css
.timeline-center {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 0;
}
.timeline-center::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 2px;
  background: rgba(188, 69, 40, 0.2);
}
.tl-item {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  margin-bottom: 48px;
}
.tl-item:nth-child(even) {
  direction: rtl;
}
@media (max-width: 768px) {
  .timeline-center::before { left: 20px; }
  .tl-item { grid-template-columns: 1fr; padding-left: 48px; direction: ltr; }
}
```

---

## L09 · 大引用 / Pull Quote

**情绪标签**：节奏 · 金句停顿 · ⚡ 视觉惊喜
**适用**：金句、核心观点、段落间的节奏变化

```css
.pull-quote {
  text-align: center;
  padding: clamp(60px, 8vh, 100px) clamp(24px, 4vw, 48px);
  max-width: 700px;
  margin: 0 auto;
  position: relative;
}
.pull-quote::before {
  content: '"';
  font-size: clamp(4rem, 10vw, 8rem);
  color: rgba(188, 69, 40, 0.15);
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  line-height: 1;
  font-family: Georgia, serif;
}
.pull-quote p {
  font-size: clamp(1.3rem, 3vw, 1.8rem);
  color: #5D4E47;
  line-height: 1.8;
  font-weight: 500;
}
```

**使用提示**：引用文字不超过 2 行。前后留白要充足，让它"悬停"在页面中。

---

## L10 · 品牌色满底面板

**情绪标签**：结尾 · CTA收束 · 品牌收束
**适用**：CTA 区、结尾总结、重要公告

```css
.brand-panel {
  background: #bc4528;
  color: #F4F1ED;
  padding: clamp(48px, 6vh, 80px) clamp(24px, 4vw, 48px);
  border-radius: 16px;
  max-width: 900px;
  margin: 48px auto;
  text-align: center;
}
.brand-panel h2 {
  font-size: clamp(1.5rem, 3.5vw, 2.2rem);
  margin-bottom: 0.5em;
}
.brand-panel .btn-white {
  display: inline-block;
  padding: 12px 28px;
  background: #F4F1ED;
  color: #bc4528;
  border-radius: 8px;
  font-weight: 600;
  margin-top: 1em;
}
```

**使用提示**：放在页面末尾或倒数第二屏。文字要精简，CTA 明确。

---

## L11 · 两栏对称

**情绪标签**：正文 · 对比/并列 · 清晰对照
**适用**：对比（好/坏）、并列要点、Before/After

```css
.split-compare {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(24px, 3vw, 40px);
  max-width: 1000px;
  margin: 0 auto;
  padding: 40px 24px;
}
@media (max-width: 768px) {
  .split-compare { grid-template-columns: 1fr; }
}
```

---

## L12 · Tab 切换单栏

**情绪标签**：正文 · 分类展示 · 空间节省
**适用**：分类内容展示、多主题切换

```css
.tab-layout {
  max-width: 800px;
  margin: 0 auto;
  padding: 40px 24px;
}
.tab-nav {
  display: flex;
  gap: 0;
  border-bottom: 2px solid #EFEAE2;
  margin-bottom: 32px;
}
.tab-btn {
  padding: 12px 24px;
  border: none;
  background: transparent;
  font-size: 0.9rem;
  color: #8A8178;
  cursor: pointer;
  border-bottom: 2px solid transparent;
  margin-bottom: -2px;
  transition: all 0.2s;
}
.tab-btn.active {
  color: #bc4528;
  border-bottom-color: #bc4528;
  font-weight: 600;
}
```

---

## 使用规则

1. **每个 section 必须选不同的布局** — 避免单调
2. **首屏必须用 L01 或 L02** — 有冲击力
3. **至少一处用 L06 或 L09** — 打破节奏（⚡ 视觉惊喜）
4. **结尾用 L10** — 品牌色收束
5. **不要超过 6 种布局** — 太多反而混乱
6. **连续 2 个 section 不能同为"信息概览"类**（L04/L11/L12）— 必须交替情绪节奏

---

## 情绪节奏参考组合

### 短页面（3-4 section）
```
L01 开场建立信任 → L05 正文流程引导 → L09 节奏金句停顿 → L10 结尾品牌收束
```

### 中页面（5-6 section）
```
L01 开场建立信任 → L04 信息概览 → L06 节奏打破沉闷 → L03 长文阅读 → L09 节奏金句停顿 → L10 结尾品牌收束
```

### 长页面（7+ section）
```
L02 极简冲击 → L04 信息概览 → L05 流程引导 → L06 打破沉闷 → L08 时间历程 → L09 金句停顿 → L11 对比说明 → L10 品牌收束
```
