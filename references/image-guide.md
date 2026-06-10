# 图片处理规范 — MOON明月

> 确保所有图片符合品牌暖色调，不破坏整体氛围。

---

## 图片圆角

| 图片类型 | 圆角值 | 说明 |
|---------|--------|------|
| 内容插图 | `border-radius: 8px` | 常规内容图片 |
| 卡片内图片 | `border-radius: 10px` | 卡片/组件内的图片 |
| 头像/图标 | `border-radius: 50%` | 圆形裁切 |
| 全出血大图 | `border-radius: 0` | 通栏大图，无圆角 |

---

## 图片阴影

```css
.img-shadow {
  box-shadow: 0 4px 20px rgba(93, 78, 71, 0.06);
}
.img-shadow-strong {
  box-shadow: 0 8px 32px rgba(93, 78, 71, 0.1);
}
```

---

## 图片滤镜（关键！）

冷色调图片必须叠暖色滤镜，保持品牌温度：

```css
.img-warm-filter {
  filter: sepia(8%) saturate(92%) brightness(102%);
}
```

**效果**：
- `sepia(8%)` — 轻微暖调，不夸张
- `saturate(92%)` — 略微降低饱和度，更克制
- `brightness(102%)` — 微提亮，保持通透

**禁忌**：
- ❌ 不要 `sepia(30%+)` — 会变成老照片
- ❌ 不要 `grayscale()` — 与品牌温暖感冲突
- ❌ 不要 `hue-rotate()` — 会改变品牌色

---

## 图片比例

| 场景 | 推荐比例 | 用途 |
|------|---------|------|
| 横图 | 16:9 | 文章配图、banner |
| 竖图 | 3:4 | 小红书图文、卡片 |
| 方形 | 1:1 | 头像、图标、缩略图 |
| 宽幅 | 21:9 | 全出血大图、Hero背景 |

---

## 图片加载

```html
<img src="..." alt="描述文字" loading="lazy" decoding="async">
```

- `loading="lazy"` — 懒加载，提升首屏速度
- `decoding="async"` — 异步解码，不阻塞渲染
- `alt` 必须填写 — 无障碍+SEO

---

## 图片占位规范

无图片时，使用 CSS 渐变占位，不突兀：

```css
.img-placeholder {
  background: linear-gradient(135deg, #E8C4B0 0%, #EFEAE2 50%, #F4F1ED 100%);
  display: flex;
  align-items: center;
  justify-content: center;
}
```

---

## 图片与文字间距

```css
.img-with-caption {
  margin-bottom: 12px;
}
.img-caption {
  font-size: 0.75rem;
  color: #8A8178;
  text-align: center;
  margin-top: 12px;
}
```

---

## 响应式图片

```css
img {
  max-width: 100%;
  height: auto;
  display: block;
}
```

---

## 图片禁忌

- ❌ 冷色调图片不叠滤镜直接使用
- ❌ 高饱和荧光色图片
- ❌ 低分辨率模糊图片
- ❌ 带水印/Logo杂乱的图片
- ❌ 与内容无关的装饰图
