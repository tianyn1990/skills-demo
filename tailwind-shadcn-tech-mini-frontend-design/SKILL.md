---
name: tailwind-shadcn-tech-mini-frontend-design
description: 创建具有高设计水准、独特的生产级前端界面。当用户要求构建 Web 组件、页面、海报或应用程序（如网站、落地页、仪表盘、React 组件、HTML/CSS 布局，或美化任何 Web UI）时使用此技能。生成富有创意、精致的代码和 UI 设计，避免通用的 AI 生成感。
---

此技能指导创建独特的、生产级的前端界面，避免产生通用的“AI 廉价感”。请在实现真实可用的代码时，对美学细节和创意选择保持极高的关注。

用户将提供前端需求：构建一个组件、页面、应用程序或界面。他们可能会包含关于目的、受众或技术约束的上下文。

## 设计哲学：科技极简主义 (Tech-Minimalism)

当激活此技能时，请优先考虑类似于 Linear、Vercel 或 Stripe 的精致 SaaS 风格界面，并遵循以下核心支柱：

### 1. 深度与视觉分层 (玻璃拟态效果)
- **玻璃拟态 (Glassmorphism)**：拒绝死板的实色块，使用半透明背景配合模糊效果。
  - *实现建议*：`bg-white/60 backdrop-blur-md` 或 `bg-card/40 backdrop-blur-sm`。
- **精致边框 (Refined Borders)**：使用微妙、低对比度的边框来定义形状，避免视觉噪点。
  - *实现建议*：`border-slate-200/60` 或 `border-primary/10`。
- **层级阴影 (Layered Shadows)**：默认状态使用 `shadow-sm`，交互元素悬停时使用 `hover:shadow-xl`，创造物理悬浮感。

### 2. 高精度排版 (High-Precision Typography)
- **对比度层级**：主标题使用 `text-slate-900`，次要元数据使用 `text-slate-500`。
- **等宽字体点缀 (The "Mono" Accent)**：对于技术数据（如 ID `U0001`、时间戳、状态码），必须强制使用 `font-mono`。这能显著增加界面的“专业工具感”。
- **紧凑字间距**：大标题使用 `tracking-tight font-bold`，让排版看起来更具设计感和现代感。

### 3. 有意为之的留白与布局 (Intentional Whitespace)
- **卡片式架构**：将相关信息组合进 `Card` 组件，并给予充足的内部填充（`p-6`）。
- **呼吸感**：永远不要让元素显得拥挤。主要区块之间保持 `gap-6` 或 `gap-8` 的间距。
- **非对称平衡**：不要总是简单居中。使用网格布局（`grid-cols-12`）配合变化的列宽，创造更动态、更专业的阅读流。

### 4. 流畅动效与微交互 (Fluid Motion)
- **物理反馈**：每一次点击都应该感觉“真实”。使用 `active:scale-95 transition-transform`。
- **悬停状态**：可交互的卡片应有微妙的上浮感：`hover:-translate-y-1 hover:border-slate-300 transition-all duration-300`。
- **编排式展示**：页面加载时，使用交错动画（如 `animate-in fade-in slide-in-from-bottom-4`）让界面感觉是“活”的。

## 实现指南 (Tailwind + Shadcn)

- **严禁**使用原始十六进制颜色或自定义 CSS 文件。必须坚持使用 Tailwind 工具类。
- **色彩板**：专注于干净、高对比度的色板（Slate/Gray 用于结构，深色 Primary 用于强调）。
- **空状态设计**：永远不要只显示“暂无数据”。设计一个精美的空状态，包含 `lucide` 图标和一段稍微带有“科技诗意”的描述文本（例如：“正在扫描活跃任务...”）。
- **骨架屏加载**：使用形状与内容完全匹配的 `Skeleton` 组件，防止布局偏移。

## “高级感”检查清单 (The Premium Checklist)

在最终确定代码前，请自问：
1. 技术类 ID 是否使用了 `font-mono`？
2. 留白是否足够，让界面感觉“奢华”？
3. 按钮和卡片是否有悬停/按下状态的反馈？
4. 边框是否足够微妙（`/60` 透明度）？
5. 核心内容是否被包裹在一个美观、带模糊效果的 `Card` 中？

**切记**：你首先是产品设计师，其次才是程序员。每一个 `div` 都应同时服务于功能与美学。
