# 组件库 — MOON明月（完整版）

> 所有组件继承 brand-dna.md。禁止使用 HTML 默认样式。

---

## 使用频率标签

| 标签 | 含义 | 使用建议 |
|------|------|---------|
| **🔴 高频** | 几乎每次都会用到 | 优先选择，默认包含 |
| **🟡 中频** | 根据内容类型选择 | 按需挑选，丰富页面 |
| **🟢 低频** | 特定场景才用 | 明确需要时才使用 |

---

## 基础组件（原有12个）

### 1. 信息卡片（Info Card）🔴 高频

**用途**：展示关键信息组、功能点、核心价值。

```css
.info-card {
  background: #EFEAE2;
  border-left: 3px solid #bc4528;
  border-radius: 0 10px 10px 0;
  padding: 28px 24px;
}
.info-card h4 {
  font-size: 1rem;
  font-weight: 700;
  color: #bc4528;
  margin: 0 0 14px;
}
.info-card ul { list-style: none; padding: 0; margin: 0; }
.info-card li {
  font-size: 0.85rem;
  color: #5D4E47;
  line-height: 1.9;
  padding-left: 14px;
  position: relative;
  margin-bottom: 6px;
}
.info-card li::before {
  content: '·';
  position: absolute;
  left: 0;
  color: #bc4528;
  font-weight: 700;
}
```

---

### 2. 步骤编号（Step Indicator）🔴 高频

**用途**：教程步骤、流程引导。

```css
.step-indicator {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  position: relative;
}
.step-indicator::before {
  content: '';
  position: absolute;
  left: -44px;
  top: 8px;
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: #bc4528;
  border: 3px solid #F4F1ED;
}
.step-num {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 2.5rem;
  font-weight: 200;
  color: rgba(188, 69, 40, 0.3);
  line-height: 1;
  flex-shrink: 0;
  min-width: 48px;
}
.step-content h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #5D4E47;
  margin: 0 0 6px;
}
.step-content p {
  font-size: 0.95rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0;
}
```

---

### 3. 引用块（Quote Block）🔴 高频

**用途**：金句、关键观点、用户反馈。

```css
.moon-quote {
  background: rgba(188, 69, 40, 0.05);
  border-left: 3px solid #bc4528;
  border-radius: 0 8px 8px 0;
  padding: 20px 24px;
  margin: 24px 0;
  max-width: 600px;
}
.moon-quote p {
  font-size: 1.05rem;
  color: #5D4E47;
  line-height: 1.8;
  margin: 0;
  font-style: normal;
}
```

---

### 4. 代码面板（Code Panel）🟡 中频

**用途**：代码展示、命令行、技术内容。

```css
.code-panel {
  background: #3D342F;
  border-radius: 12px;
  overflow: hidden;
  margin: 24px 0;
  max-width: 650px;
}
.code-header {
  display: flex;
  align-items: center;
  gap: 6px;
  padding: 12px 16px;
  background: rgba(0,0,0,0.15);
}
.dot { width: 10px; height: 10px; border-radius: 50%; }
.dot.red { background: #E84A5F; }
.dot.yellow { background: #F4D758; }
.dot.green { background: #4ade80; }
.code-title { margin-left: 8px; font-size: 0.75rem; color: #8A8178; }
.code-panel pre {
  padding: 20px;
  margin: 0;
  overflow-x: auto;
}
.code-panel code {
  font-family: 'ui-monospace, Consolas', 'ui-monospace, Consolas', monospace;
  font-size: 0.85rem;
  color: #F4F1ED;
  line-height: 1.7;
}
```

---

### 5. 提示条（Tip Bar）🔴 高频

**用途**：Tips、注意事项、补充说明。

```css
.tip-bar {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  background: rgba(188, 69, 40, 0.05);
  border-radius: 8px;
  padding: 14px 18px;
  max-width: 600px;
  margin: 20px 0;
}
.tip-icon { font-size: 1rem; flex-shrink: 0; }
.tip-text {
  font-size: 0.85rem;
  color: #bc4528;
  line-height: 1.6;
}
```

---

### 6. 标签组（Tag Group）🟡 中频

**用途**：功能标签、关键词、技术栈。

```css
.tag-group { display: flex; gap: 8px; flex-wrap: wrap; }
.moon-tag {
  font-size: 0.75rem;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 4px 12px;
  border-radius: 4px;
  letter-spacing: 0.02em;
  font-weight: 500;
}
```

---

### 7. 对比表格（Comparison Table）🟡 中频

**用途**：方案对比、工具对比、Before/After。

```css
.moon-table {
  width: 100%;
  max-width: 650px;
  border-collapse: collapse;
  font-size: 0.85rem;
}
.moon-table th {
  font-weight: 600;
  color: #bc4528;
  padding: 12px 16px;
  text-align: left;
  border-bottom: 2px solid #bc4528;
  font-size: 0.8rem;
  letter-spacing: 0.04em;
}
.moon-table td {
  padding: 12px 16px;
  color: #5D4E47;
  border-bottom: 1px solid #EFEAE2;
  line-height: 1.6;
}
.moon-table td:first-child {
  color: #bc4528;
  font-weight: 500;
  font-size: 0.8rem;
}
```

---

### 8. 截图展示框（Screenshot Frame）🟡 中频

**用途**：产品截图、操作演示、界面展示。

```css
.screenshot-frame {
  background: #EFEAE2;
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 2px 16px rgba(93, 78, 71, 0.06);
  max-width: 700px;
  margin: 24px auto;
}
.screenshot-frame img {
  width: 100%;
  border-radius: 8px;
  display: block;
}
.screenshot-caption {
  font-size: 0.75rem;
  color: #8A8178;
  text-align: center;
  margin-top: 12px;
}
```

---

### 9. CTA 按钮（Call to Action）🔴 高频

**用途**：行动引导、链接跳转。

```css
.cta-primary {
  display: inline-block;
  padding: 14px 32px;
  background: #bc4528;
  color: #F4F1ED;
  border-radius: 10px;
  font-weight: 600;
  font-size: 0.95rem;
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
}
.cta-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(188, 69, 40, 0.25);
}
.cta-secondary {
  display: inline-block;
  padding: 12px 28px;
  background: transparent;
  color: #bc4528;
  border: 2px solid #bc4528;
  border-radius: 10px;
  font-weight: 600;
  font-size: 0.9rem;
  text-decoration: none;
  transition: all 0.2s;
}
.cta-secondary:hover {
  background: rgba(188, 69, 40, 0.05);
}
```

---

### 10. 品牌署名块（Brand Footer）🔴 高频

**用途**：页面结尾、卡片署名。

```css
.brand-footer {
  background: #bc4528;
  border-radius: 12px;
  padding: 16px 24px;
  display: flex;
  align-items: center;
  gap: 14px;
  max-width: 400px;
}
.brand-footer .avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  border: 2px solid rgba(255,255,255,0.3);
}
.brand-name {
  display: block;
  color: #F4F1ED;
  font-weight: 600;
  font-size: 0.9rem;
}
.brand-tags {
  display: block;
  color: rgba(244, 241, 237, 0.6);
  font-size: 0.75rem;
  margin-top: 2px;
}
```

---

### 11. 手绘下划线（Handdrawn Underline）🔴 高频

**用途**：关键词强调、CTA 装饰。

```css
.underline-hand {
  position: relative;
  display: inline-block;
}
.underline-hand::after {
  content: '';
  position: absolute;
  left: -2px;
  right: -2px;
  bottom: -4px;
  height: 8px;
  background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='80' height='12'%3E%3Cpath d='M2 8Q20 3 40 7T78 5' stroke='%23C65C3D' stroke-width='2.5' fill='none' stroke-linecap='round'/%3E%3C/svg%3E") repeat-x;
  background-size: auto 100%;
}
```

---

### 12. 分隔线（Section Divider）🔴 高频

**用途**：内容块之间的呼吸间隔。

```css
.moon-divider {
  width: 48px;
  height: 2px;
  background: #bc4528;
  opacity: 0.3;
  margin: 48px 0;
}
.moon-divider.wide {
  width: 120px;
  opacity: 0.15;
}
```

---

## 扩展组件（新增18个）

### 13. 书卡 / 读书笔记卡（Book Card）🟡 中频

**用途**：读书笔记、知识卡片、推荐书单。

```css
.book-card {
  display: flex;
  background: #FAF7F2;
  border-radius: 0 12px 12px 0;
  overflow: hidden;
  max-width: 560px;
  box-shadow: 0 2px 12px rgba(93, 78, 71, 0.04);
}
.book-spine {
  width: 6px;
  background: #bc4528;
  flex-shrink: 0;
}
.book-content {
  padding: 24px 28px;
}
.book-tag {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 3px 10px;
  border-radius: 4px;
  margin-bottom: 10px;
  letter-spacing: 0.04em;
}
.book-title {
  font-size: 1.1rem;
  font-weight: 700;
  color: #5D4E47;
  margin: 0 0 10px;
  line-height: 1.4;
}
.book-excerpt {
  font-size: 0.9rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0 0 12px;
}
.book-meta {
  font-size: 0.75rem;
  color: #8A8178;
  font-style: normal;
}
```

---

### 14. 聊天气泡（Chat Bubble）🟢 低频

**用途**：对话式教程、Q&A、模拟对话场景。

```css
.chat-bubble-group {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 600px;
  margin: 24px 0;
}
.chat-bubble {
  display: flex;
  gap: 12px;
  align-items: flex-start;
}
.chat-bubble.sender {
  flex-direction: row;
}
.chat-bubble.receiver {
  flex-direction: row-reverse;
  align-self: flex-end;
}
.chat-avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: #EFEAE2;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1rem;
  flex-shrink: 0;
}
.chat-bubble.sender .chat-avatar {
  background: rgba(188, 69, 40, 0.1);
}
.chat-body {
  background: #EFEAE2;
  border-radius: 14px;
  padding: 14px 18px;
  max-width: 420px;
}
.chat-bubble.sender .chat-body {
  background: rgba(188, 69, 40, 0.06);
  border-bottom-left-radius: 4px;
}
.chat-bubble.receiver .chat-body {
  background: #EFEAE2;
  border-bottom-right-radius: 4px;
}
.chat-body p {
  font-size: 0.9rem;
  color: #5D4E47;
  line-height: 1.6;
  margin: 0;
}
```

---

### 15. 日历时间标记（Calendar Mark）🟡 中频

**用途**：里程碑、计划表、教程排期、事件时间线。

```css
.calendar-mark {
  display: flex;
  align-items: center;
  gap: 18px;
  background: #FAF7F2;
  border-radius: 12px;
  padding: 18px 22px;
  max-width: 480px;
  box-shadow: 0 2px 10px rgba(93, 78, 71, 0.04);
}
.cal-date {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #bc4528;
  border-radius: 10px;
  padding: 10px 14px;
  min-width: 56px;
  color: #F4F1ED;
}
.cal-month {
  font-size: 0.65rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  opacity: 0.85;
}
.cal-day {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 1.4rem;
  font-weight: 700;
  line-height: 1;
}
.cal-event h4 {
  font-size: 0.95rem;
  font-weight: 700;
  color: #5D4E47;
  margin: 0 0 4px;
}
.cal-event p {
  font-size: 0.8rem;
  color: #8A8178;
  line-height: 1.5;
  margin: 0;
}
```

---

### 16. 手风琴折叠面板（Accordion）🟡 中频

**用途**：底层逻辑、FAQ、可折叠的内容区。点击展开，再次点击折叠。

```css
.accordion-group {
  max-width: 800px;
  margin: 0 auto;
}
.accordion-item {
  border-bottom: 1px solid rgba(93, 78, 71, 0.1);
  overflow: hidden;
}
.accordion-trigger {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 24px 0;
  background: none;
  border: none;
  cursor: pointer;
  font-family: 'Arial Unicode', 'Noto Sans SC', sans-serif;
  font-size: 1.15rem;
  font-weight: 700;
  color: #5D4E47;
  transition: color 0.2s;
  text-align: left;
}
.accordion-trigger:hover {
  color: #bc4528;
}
.accordion-trigger .acc-title {
  display: flex;
  align-items: center;
  gap: 14px;
}
.accordion-trigger .acc-icon {
  font-size: 1.4rem;
}
.accordion-icon {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 1.3rem;
  font-weight: 300;
  color: #bc4528;
  transition: transform 0.2s;
  flex-shrink: 0;
  width: 28px;
  text-align: center;
}
.accordion-panel {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s ease, padding 0.4s ease;
  padding: 0 0 0 38px;
}
.accordion-item.active .accordion-panel {
  max-height: 400px;
  padding: 0 0 28px 38px;
}
.accordion-panel p {
  color: #8A8178;
  font-size: 0.95rem;
  line-height: 1.9;
  margin: 0;
  max-width: 65ch;
}
```

---

### 17. 增强步骤卡片（Step Card）🟡 中频

**用途**：六步法等流程展示，比纵向步骤更适合移动端，识别性更强。

```css
.step-card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 24px;
}
.step-card {
  background: #FAF7F2;
  border-radius: 14px;
  padding: 36px 28px;
  position: relative;
  overflow: hidden;
  transition: transform 0.2s, box-shadow 0.2s;
}
.step-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(93, 78, 71, 0.08);
}
.step-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: #bc4528;
  opacity: 0.25;
  transition: opacity 0.2s;
}
.step-card:hover::before {
  opacity: 0.6;
}
.step-card-num {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 3.2rem;
  font-weight: 200;
  color: rgba(188, 69, 40, 0.12);
  line-height: 1;
  margin-bottom: 14px;
}
.step-card h4 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 12px;
}
.step-card p {
  font-size: 0.9rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0;
}
```

---

### 18. 大卡片（Feature Card）🟡 中频

**用途**：思维升级四阶段等需要强识别性的内容。

```css
.feature-card-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 24px;
}
.feature-card {
  background: #FAF7F2;
  border-radius: 14px;
  padding: 40px 28px;
  text-align: center;
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  border-top: 4px solid transparent;
  position: relative;
  overflow: hidden;
}
.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 32px rgba(93, 78, 71, 0.1);
  border-top-color: #bc4528;
}
.feature-card .fc-icon {
  font-size: 2.4rem;
  margin-bottom: 16px;
  display: block;
}
.feature-card .fc-num {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 12px;
}
.feature-card h4 {
  font-size: 1.15rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 14px;
}
.feature-card p {
  font-size: 0.88rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0;
}
```

---

### 19. 增强时间线（Timeline Enhanced）🟡 中频

**用途**：成长路径、历程展示，内容更丰富，有配图位。

```css
.timeline-enhanced {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 0;
}
.timeline-enhanced::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 2px;
  background: rgba(188, 69, 40, 0.2);
}
.tl-e-item {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  margin-bottom: 48px;
  align-items: center;
  position: relative;
}
.tl-e-item:nth-child(even) {
  direction: rtl;
}
.tl-e-item:nth-child(even) > * {
  direction: ltr;
}
.tl-e-dot {
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: #bc4528;
  border: 4px solid #F4F1ED;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
  box-shadow: 0 0 0 4px rgba(188, 69, 40, 0.1);
}
.tl-e-card {
  background: #FAF7F2;
  border-radius: 14px;
  padding: 32px 28px;
  border-left: 4px solid #bc4528;
  transition: transform 0.2s;
}
.tl-e-card:hover {
  transform: translateX(4px);
}
.tl-e-item:nth-child(even) .tl-e-card {
  border-left: none;
  border-right: 4px solid #bc4528;
}
.tl-e-item:nth-child(even) .tl-e-card:hover {
  transform: translateX(-4px);
}
.tl-e-icon {
  font-size: 2rem;
  margin-bottom: 12px;
  display: block;
}
.tl-e-card h4 {
  font-size: 1.2rem;
  margin-bottom: 10px;
  color: #5D4E47;
}
.tl-e-card p {
  font-size: 0.92rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0 0 10px;
}
.tl-e-card .tl-e-detail {
  font-size: 0.85rem;
  color: #bc4528;
  font-weight: 500;
  margin-top: 8px;
}
```

---

### 20. 杂志裁切卡片（Magazine Clip Card）🟡 中频

**用途**：重点文章推荐、深度内容、专题展示。不规则留白营造杂志感。

```css
.magazine-card {
  background: #FAF7F2;
  border-radius: 0 16px 16px 0;
  padding: 40px 36px 36px 40px;
  max-width: 520px;
  position: relative;
  overflow: hidden;
  border-left: 4px solid #bc4528;
  transition: transform 0.25s, box-shadow 0.25s;
}
.magazine-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(93, 78, 71, 0.08);
}
.magazine-card::before {
  content: '';
  position: absolute;
  top: -20px;
  right: -20px;
  width: 80px;
  height: 80px;
  background: rgba(188, 69, 40, 0.06);
  border-radius: 50%;
}
.mag-tag {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 4px 12px;
  border-radius: 4px;
  letter-spacing: 0.04em;
  margin-bottom: 16px;
  position: relative;
  z-index: 1;
}
.mag-title {
  font-size: 1.4rem;
  font-weight: 800;
  color: #5D4E47;
  line-height: 1.4;
  margin-bottom: 14px;
  position: relative;
  z-index: 1;
}
.mag-excerpt {
  font-size: 0.95rem;
  color: #8A8178;
  line-height: 1.8;
  margin-bottom: 24px;
  position: relative;
  z-index: 1;
}
.mag-meta {
  display: flex;
  gap: 16px;
  font-size: 0.75rem;
  color: #8A8178;
  font-family: 'Arial Unicode', sans-serif;
  position: relative;
  z-index: 1;
}
.mag-date {
  color: #bc4528;
  font-weight: 600;
}
```

---

### 21. 工具推荐卡片（Tool Card）🟡 中频

**用途**：软件/工具/资源推荐。图标+标题+标签+描述+链接。

```css
.tool-card {
  display: flex;
  align-items: center;
  gap: 20px;
  background: #FAF7F2;
  border-radius: 12px;
  padding: 24px 28px;
  max-width: 600px;
  transition: transform 0.2s, box-shadow 0.2s;
  border: 1px solid rgba(93, 78, 71, 0.04);
}
.tool-card:hover {
  transform: translateX(4px);
  box-shadow: 0 6px 20px rgba(93, 78, 71, 0.06);
}
.tool-icon {
  width: 52px;
  height: 52px;
  border-radius: 12px;
  background: #EFEAE2;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  flex-shrink: 0;
  transition: background 0.2s;
}
.tool-card:hover .tool-icon {
  background: rgba(188, 69, 40, 0.1);
}
.tool-body {
  flex: 1;
}
.tool-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 6px;
}
.tool-name {
  font-size: 1.05rem;
  font-weight: 700;
  color: #5D4E47;
}
.tool-tag {
  font-size: 0.65rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 2px 8px;
  border-radius: 4px;
}
.tool-desc {
  font-size: 0.85rem;
  color: #8A8178;
  line-height: 1.6;
  margin-bottom: 8px;
}
.tool-link {
  font-size: 0.8rem;
  color: #bc4528;
  font-weight: 600;
  text-decoration: none;
}
```

---

### 22. 数据洞察块（Insight Block）🟡 中频

**用途**：轻量数据+解读。超大数字+标题+解读文字。

```css
.insight-block {
  display: flex;
  align-items: flex-start;
  gap: 24px;
  background: #FAF7F2;
  border-radius: 14px;
  padding: 32px 28px;
  max-width: 600px;
  border-top: 3px solid #bc4528;
}
.insight-number {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 3rem;
  font-weight: 700;
  color: #bc4528;
  line-height: 1;
  flex-shrink: 0;
  min-width: 80px;
  text-align: center;
}
.insight-unit {
  font-size: 1rem;
  font-weight: 400;
  color: #8A8178;
}
.insight-body h4 {
  font-size: 1.05rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 8px;
}
.insight-body p {
  font-size: 0.9rem;
  color: #8A8178;
  line-height: 1.7;
  margin: 0;
}
```

---

### 23. 项目案例卡片（Case Card）🟡 中频

**用途**：项目展示。问题→解决→结果三步骤。

```css
.case-card {
  background: #FAF7F2;
  border-radius: 14px;
  padding: 32px 28px;
  max-width: 600px;
  transition: transform 0.2s, box-shadow 0.2s;
  border: 1px solid rgba(93, 78, 71, 0.04);
}
.case-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 30px rgba(93, 78, 71, 0.08);
}
.case-tag {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 4px 12px;
  border-radius: 4px;
  margin-bottom: 16px;
  letter-spacing: 0.04em;
}
.case-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 20px;
}
.case-flow {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.case-step {
  display: flex;
  align-items: flex-start;
  gap: 12px;
}
.case-step-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #bc4528;
  margin-top: 8px;
  flex-shrink: 0;
}
.case-step-label {
  font-size: 0.75rem;
  font-weight: 600;
  color: #bc4528;
  letter-spacing: 0.05em;
  margin-bottom: 2px;
}
.case-step-text {
  font-size: 0.9rem;
  color: #5D4E47;
  line-height: 1.6;
}
```

---

### 24. 方法框架图（Framework Grid）🟡 中频

**用途**：2×2 矩阵/简单框架。四宫格卡片。

```css
.framework-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  max-width: 500px;
}
.framework-cell {
  background: #FAF7F2;
  border-radius: 12px;
  padding: 28px 24px;
  text-align: center;
  transition: all 0.2s;
  border: 2px solid transparent;
}
.framework-cell:hover {
  border-color: #bc4528;
  transform: translateY(-3px);
  box-shadow: 0 6px 16px rgba(93, 78, 71, 0.06);
}
.framework-cell .fc-label {
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 8px;
}
.framework-cell .fc-title {
  font-size: 1.1rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 8px;
}
.framework-cell .fc-desc {
  font-size: 0.85rem;
  color: #8A8178;
  line-height: 1.6;
  margin: 0;
}
```

---

### 25. 时间日志卡片（Log Card）🟢 低频

**用途**：某天/某周工作记录。日期分隔线+时间+事项+标签。

```css
.log-card {
  max-width: 600px;
}
.log-date {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 0.8rem;
  font-weight: 600;
  color: #bc4528;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 12px;
}
.log-date::after {
  content: '';
  flex: 1;
  height: 1px;
  background: rgba(188, 69, 40, 0.15);
}
.log-items {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.log-item {
  display: flex;
  align-items: flex-start;
  gap: 16px;
  background: #FAF7F2;
  border-radius: 10px;
  padding: 16px 20px;
  transition: background 0.2s;
}
.log-item:hover {
  background: #EFEAE2;
}
.log-time {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 0.8rem;
  font-weight: 600;
  color: #8A8178;
  flex-shrink: 0;
  min-width: 50px;
  padding-top: 2px;
}
.log-content h4 {
  font-size: 0.95rem;
  font-weight: 700;
  color: #5D4E47;
  margin-bottom: 4px;
}
.log-content p {
  font-size: 0.85rem;
  color: #8A8178;
  line-height: 1.6;
  margin: 0;
}
.log-tag {
  display: inline-block;
  font-size: 0.65rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 2px 8px;
  border-radius: 4px;
  margin-top: 6px;
}
```

---

### 26. 用户评价卡（Testimonial Card）🟢 低频

**用途**：学员反馈、客户评价、用户故事。温暖真实，不浮夸。

```css
.testimonial-card {
  background: #FAF7F2;
  border-radius: 14px;
  padding: 36px 32px;
  max-width: 400px;
  position: relative;
  border: 1px solid rgba(93, 78, 71, 0.04);
  transition: transform 0.2s;
}
.testimonial-card:hover {
  transform: translateY(-3px);
}
.testimonial-quote {
  font-family: Georgia, serif;
  font-size: 4rem;
  color: rgba(188, 69, 40, 0.15);
  line-height: 1;
  margin-bottom: 8px;
}
.testimonial-text {
  font-size: 1rem;
  color: #5D4E47;
  line-height: 1.9;
  margin-bottom: 24px;
  font-style: normal;
}
.testimonial-author {
  display: flex;
  align-items: center;
  gap: 12px;
}
.testimonial-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #bc4528;
  color: #F4F1ED;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  font-size: 0.9rem;
  font-family: 'Arial Unicode', sans-serif;
}
.testimonial-name {
  font-size: 0.9rem;
  font-weight: 600;
  color: #5D4E47;
}
.testimonial-role {
  font-size: 0.75rem;
  color: #8A8178;
}
```

---

### 27. 资源列表（Resource List）🟡 中频

**用途**：书单/工具清单。编号+标题+描述+标签。

```css
.resource-list {
  max-width: 700px;
  margin: 0 auto;
}
.resource-item {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 20px 24px;
  background: #FAF7F2;
  border-radius: 10px;
  margin-bottom: 12px;
  transition: background 0.2s, transform 0.2s;
  border: 1px solid rgba(93, 78, 71, 0.03);
}
.resource-item:hover {
  background: #EFEAE2;
  transform: translateX(4px);
}
.resource-num {
  font-family: 'Arial Unicode', sans-serif;
  font-size: 1.5rem;
  font-weight: 200;
  color: rgba(188, 69, 40, 0.25);
  line-height: 1;
  min-width: 36px;
  text-align: center;
}
.resource-body {
  flex: 1;
}
.resource-body h4 {
  font-size: 1rem;
  font-weight: 700;
  color: #5D4E47;
  margin: 0 0 4px;
}
.resource-body p {
  font-size: 0.85rem;
  color: #8A8178;
  margin: 0;
  line-height: 1.5;
}
.resource-tag {
  font-size: 0.7rem;
  font-weight: 600;
  color: #bc4528;
  background: rgba(188, 69, 40, 0.08);
  padding: 3px 10px;
  border-radius: 4px;
  flex-shrink: 0;
}
```

---

### 28. 通知公告条（Announcement Bar）🟢 低频

**用途**：重要更新、限时活动。醒目但不刺眼。

```css
.announcement-bar {
  display: flex;
  align-items: center;
  gap: 12px;
  background: rgba(188, 69, 40, 0.06);
  border-left: 3px solid #bc4528;
  border-radius: 0 10px 10px 0;
  padding: 14px 20px;
  max-width: 700px;
  margin: 20px 0;
  font-size: 0.9rem;
}
.ann-icon {
  font-size: 1.1rem;
  flex-shrink: 0;
}
.ann-text {
  color: #5D4E47;
  line-height: 1.5;
  flex: 1;
}
.ann-link {
  color: #bc4528;
  font-weight: 600;
  font-size: 0.85rem;
  text-decoration: none;
  white-space: nowrap;
  flex-shrink: 0;
}
```

---

### 29. 进度步骤条（Progress Steps）🟢 低频

**用途**：教程进度、完成状态。比数字步骤更直观。

```css
.progress-steps {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0;
  max-width: 700px;
  margin: 0 auto;
  padding: 24px 0;
}
.progress-step {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  position: relative;
  z-index: 2;
}
.progress-dot {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: #EFEAE2;
  color: #8A8178;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Arial Unicode', sans-serif;
  font-size: 0.8rem;
  font-weight: 600;
  border: 2px solid #EFEAE2;
  transition: all 0.3s;
}
.progress-step.completed .progress-dot {
  background: #bc4528;
  color: #F4F1ED;
  border-color: #bc4528;
}
.progress-step.active .progress-dot {
  background: #F4F1ED;
  color: #bc4528;
  border-color: #bc4528;
  box-shadow: 0 0 0 4px rgba(188, 69, 40, 0.1);
}
.progress-label {
  font-size: 0.75rem;
  color: #8A8178;
  font-weight: 500;
  white-space: nowrap;
}
.progress-step.active .progress-label {
  color: #bc4528;
  font-weight: 600;
}
.progress-line {
  width: 60px;
  height: 2px;
  background: #EFEAE2;
  margin: 0 4px;
  position: relative;
  top: -14px;
  transition: background 0.3s;
}
.progress-line.completed {
  background: #bc4528;
}
```

---

### 30. 折叠列表（Expandable List）🟢 低频

**用途**：FAQ、常见问题。原生details标签，无需JS。

```css
.expandable-list {
  max-width: 700px;
  margin: 0 auto;
}
.expandable-item {
  background: #FAF7F2;
  border-radius: 10px;
  margin-bottom: 10px;
  overflow: hidden;
  border: 1px solid rgba(93, 78, 71, 0.04);
}
.expandable-summary {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 18px 22px;
  cursor: pointer;
  font-weight: 600;
  color: #5D4E47;
  font-size: 0.95rem;
  list-style: none;
}
.expandable-summary::-webkit-details-marker {
  display: none;
}
.expandable-summary::after {
  content: '+';
  font-family: 'Arial Unicode', sans-serif;
  font-size: 1.2rem;
  font-weight: 300;
  color: #bc4528;
  margin-left: auto;
}
.expandable-item[open] .expandable-summary::after {
  content: '−';
}
.ex-icon {
  font-size: 1.1rem;
  flex-shrink: 0;
}
.expandable-body {
  padding: 0 22px 20px 48px;
}
.expandable-body p {
  font-size: 0.9rem;
  color: #8A8178;
  line-height: 1.8;
  margin: 0;
}
```

---

## 组件选择速查表

| 场景 | 高频组件 | 中频组件 | 低频组件 |
|------|---------|---------|---------|
| 教程/知识页 | 信息卡、步骤编号、引用块、CTA、品牌署名、手绘下划线、分隔线 | 书卡、时间标记、手风琴、增强步骤卡、大卡片、时间线、杂志卡、工具卡、数据洞察、案例卡、框架图、资源列表 | 聊天气泡、日志卡、评价卡、进度条、公告条、折叠列表 |
| 月度复盘页 | 同上 | 工作总结卡、数据洞察、时间日志、要点提炼卡、Before/After | 价格套餐、产品展示 |
| 读书笔记页 | 同上 | 书卡、杂志卡、读书笔记卡、资源列表 | 其他 |
| 工具推荐页 | 同上 | 工具卡、资源列表、产品展示卡 | 其他 |
| 项目复盘页 | 同上 | 案例卡、Before/After、数据洞察、框架图 | 其他 |
