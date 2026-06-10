# Scene: 网页 / 教程页 / Landing Page

> MOON明月最核心的输出场景。知识分享的主战场。

---

## 定位

- 用于：AI教程、工具介绍、读书笔记、知识科普、个人项目展示
- 受众：职场人、AI学习者、想上手实操的人
- 目标：让人看完觉得"我也能做到"，然后真的去做

---

## 结构推荐

一个典型的知识分享网页应包含：

```
Hero 首屏（标题 + 一句话定位 + CTA）
  ↓
核心价值 / 你能学到什么（2-4 个要点）
  ↓
正文内容区（步骤/知识/对比/案例）
  ↓
引用/金句/总结（打破节奏）
  ↓
尾部 CTA + 品牌署名
```

可根据内容长度增减 section，但**每个 section 必须用不同布局**。

---

## 模板选择

根据页面用途选择对应模板骨架：

| 页面类型 | 模板文件 | 特点 |
|---------|---------|------|
| **教程/知识页** | `template-web.html` | 信息清晰、步骤明确、阅读友好 |
| **活动页/Landing** | `template-landing.html`（新增） | 视觉冲击、节奏感强、CTA 突出 |
| **App/工具型** | `template-app.html`（新增） | 功能优先、交互感、截图展示 |

**默认使用 `template-web.html`，除非用户明确要求活动推广或工具展示。**

---

## 布局选择原则

从 `layouts.md` 中选 3~6 种，遵循：

1. **首屏**用 Hero 布局（双栏不对称 / 全屏居中 / 单栏纵向）— 建立信任
2. **内容区**交替使用不同布局（卡片网格 → 步骤流程 → 时间线）— 保持新鲜
3. **至少一处**打破节奏（深色面板 / Pull Quote / 大装饰文字）— ⚡ 视觉惊喜
4. **结尾**用品牌 footer 色块收束 — 品牌收束

### 视觉惊喜 Section 硬规则（新增）

> **每个页面中，必须有且仅有 1 个"视觉惊喜" section。**

可选形式：
- **大装饰数字**（低透明度 `rgba(188,69,40,0.08)` 做背景，如 "01" 占半屏）
- **图片溢出容器**（某张图片突破卡片边界 20-40px，增加动感）
- **手绘下划线夸张用法**（标题下方手绘线加粗/加长，或连续两条）
- **深色面板打破节奏**（全宽 `#3D342F` 底，前后留白 ≥ 80px）
- **Pull Quote 大引用**（超大引号 + 居中精炼文字，前后留白充足）

**限制**：
- 不能多：超过 1 处会变成"花哨"
- 不能没有：没有会变成"平淡/模板感"
- 位置：建议在页面中段（第 3-4 个 section），打破前半段的阅读疲劳

---

## 核心规范

### 尺寸

- 内容最大宽度：`max-width: 880px`（阅读型）/ `1100px`（展示型）
- 居中排列：`margin: 0 auto`
- section 间距：`clamp(80px, 10vh, 140px)`
- 内部元素间距：`clamp(24px, 3vw, 48px)`

### 首屏 Hero

- 标题必须大且有力：`clamp(2.4rem, 6vw, 4.5rem)`
- 一句话副标题说明"这是什么 / 你能得到什么"
- 可选 CTA 按钮（陶土橙底白字）
- 留白 ≥ 40%
- **首屏不允许出现超过 3 个元素**（标题 + 副标题 + CTA 足矣）

### CTA 按钮

```css
.cta-btn {
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
.cta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(188, 69, 40, 0.25);
}
```

### 正文排版

- 行高：1.8 ~ 2.0
- 段落间距：`margin-bottom: 1.5em`
- 正文宽度：不超过 65ch（阅读最佳行宽）
- 关键词用陶土橙色标注或手绘下划线强调

### 动效

- 仅用简单入场动效：fade-in + slide-up
- 使用 IntersectionObserver 触发
- stagger 延迟：每个子元素 +80ms
- **不要 bounce、不要 elastic、不要 3D**

```css
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

---

## 禁忌（网页特有）

- ❌ 全页面居中排版（无印良品是左对齐为主的）
- ❌ 所有 section 都是"标题+三个卡片"的重复
- ❌ 没有节奏变化（深浅交替 / 宽窄变化都没有）
- ❌ 首屏标题太小（< 2rem）
- ❌ 没有任何装饰元素（纯文本堆砌）
- ❌ 图片太多太杂（宁可少用，用就要精选）
- ❌ 没有视觉惊喜 section（从头到尾平淡无奇）
- ❌ 视觉惊喜超过 1 处（花哨）

---

## 技术要求

- 单文件 HTML（`<style>` 内置，`<script>` 内置）
- 字体用 Google Fonts CDN 加载
- 图片用实际 URL 或 base64（确保离线可用）
- 响应式：768px 断点
- 可选：打印友好 `@media print`
