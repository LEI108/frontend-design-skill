# frontend-design

[English](README.md) | 简体中文

`frontend-design` 是一个用于构建生产级前端界面的 Codex skill，强调明确的视觉表达与可落地的工程质量。

它面向的是真实前端工作，而不只是视觉稿或概念图：既要符合产品、技术栈和代码库，也要有经过设计的整体感。

## 适用内容

- 新建营销页或编辑型页面
- 需要清晰层级和精致度的产品界面
- 需要在不破坏现有设计系统的前提下做优化的既有产品
- 需要具备可复用性、一致性和可维护性的共享组件
- React、Vue 或原生 HTML/CSS/JS 的前端工作

## 核心目标

- 有明确设计方向，而不是平均化的通用 UI
- 当已有设计语言存在时，优先保持系统一致性
- 可访问性、响应式和可用性
- 可维护的结构、命名和样式架构
- 对动效和视觉效果保持性能意识

## 目录结构

- `SKILL.md`：主要触发与执行说明
- `references/index.md`：辅助文件的导航中心
- `agents/openai.yaml`：技能列表和默认提示词的界面元数据
- `references/*.md`：关于架构、框架模式、可访问性、动效、性能和审查的专门说明

## 推荐阅读顺序

- 先看 `references/design-contexts.md`，判断界面应该有多大胆或多克制。
- 再阅读与技术栈匹配的框架指南：`react.md`、`vue.md` 或 `vanilla-web.md`。
- 当任务涉及结构或复用时，再看 `project-architecture.md`、`component-and-utils.md`、`naming-conventions.md` 和 `style-architecture.md`。
- 交付前再补读 `accessibility.md`、`motion-performance.md`、`performance-optimization.md` 和 `review-checklist.md`。

## 说明

- 这个 skill 的目标是产出真正可用的前端代码，而不只是视觉概念。
- 当项目里已经有既有产品或设计系统时，默认优先保留，除非用户明确要求重设计。
- 按需加载参考文件，不要默认一次性读完所有内容。
