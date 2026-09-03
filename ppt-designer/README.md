# ppt-designer 插件

遵循专业五阶段工作流的 PPT 制作子智能体 + 5 种风格设计系统技能。

- 子智能体：`agents/ppt-designer.md`
- 风格技能：`skills/ppt-style-*/SKILL.md`
  - `ppt-style-tech-keynote` 科技发布会风
  - `ppt-style-consulting` 商务咨询风
  - `ppt-style-editorial` 杂志编辑风
  - `ppt-style-fresh-minimal` 清新极简风
  - `ppt-style-new-chinese` 新中式风

工作流：需求调研 → 资料搜集 → 金字塔大纲（数字便利贴确认）→ 策划稿（逐页版式规划）→ 设计稿（Bento Grid 卡片式整页 SVG，viewBox 1280×720，可拖入 Office 2016+）。

## 来源

方法论提炼自 LINUX DO 社区精华帖 **《应该是目前最强的PPT Agent，附上完整思路分享》**（作者 Sandun/三顿，发布于 2026-03-19，「开发调优」分类，精华神帖）：
<https://linux.do/t/topic/1782304>

五阶段工作流、金字塔大纲 JSON 结构、便当网格卡片布局与整页 SVG 规范均源自该帖作者公开分享的思路与提示词；5 种风格设计系统（色彩/字体/页型）为在此基础上原创实现。

安装与使用说明见仓库根目录 [README](../README.md)。
