# ppt-designer-plugin

个人 ZCode 插件仓库：**ppt-designer** —— 一个遵循专业 PPT 公司五阶段工作流的演示文稿制作子智能体，外加 5 种风格的设计系统技能。

> 方法论源自社区分享的 PPT Agent 工作流：需求调研 → 资料搜集 → 金字塔大纲（数字便利贴）→ 策划稿（版面规划）→ 设计稿（整页 SVG / 便当网格卡片式布局）。

## 仓库结构

```
├── .claude-plugin/
│   └── marketplace.json      # 市场清单（把本仓库变成一个可添加的"插件市场"）
└── ppt-designer/             # 插件本体（目录名 = 插件名）
    ├── .zcode-plugin/
    │   └── plugin.json       # 插件清单
    ├── agents/
    │   └── ppt-designer.md   # ppt-designer 子智能体
    └── skills/
        ├── ppt-style-tech-keynote/   # 科技发布会风
        ├── ppt-style-consulting/     # 商务咨询风
        ├── ppt-style-editorial/      # 杂志编辑风
        ├── ppt-style-fresh-minimal/  # 清新极简风
        └── ppt-style-new-chinese/    # 新中式风
```

## 在其他电脑安装

1. 打开 ZCode → **设置 → 插件管理 → 发现** 页，点 **+** 添加市场；
2. 输入本仓库地址：`https://github.com/liyu34/ppt-designer-plugin`；
3. 在列表中找到 **ppt-designer**，点安装；
4. 重启会话后即可使用（私有仓库需该电脑已登录有权限的 GitHub 凭据）。

## 使用方式

- 直接对话："帮我做一份 XX 主题的 PPT"（自动触发 ppt-designer）；
- 或派发时指定子智能体 `ppt-designer`，简报格式：`主题 / 受众 / 场景 / 页数 / 风格 / 模式（clarify | execute | auto）`。

### 5 种内置风格

| 风格 | 技能 | 适用 |
|---|---|---|
| 科技发布会风 | `ppt-style-tech-keynote` | 产品发布、AI/硬件、技术分享 |
| 商务咨询风 | `ppt-style-consulting` | 工作汇报、商业计划、行业分析 |
| 杂志编辑风 | `ppt-style-editorial` | 品牌介绍、创意提案、人物故事 |
| 清新极简风 | `ppt-style-fresh-minimal` | 教学、知识分享、个人展示 |
| 新中式风 | `ppt-style-new-chinese` | 文旅、非遗、茶酒、国风、节日 |

### 产出物

每份 PPT 在 `ppt-output/<项目slug>/` 下交付四件套：`outline.json`（大纲）、`plan.md`（逐页策划稿）、`slides/*.svg`（设计稿）、`preview.html`（浏览器预览）。SVG 可直接拖入 Office 2016+ 使用，完全可编辑、无限缩放。

## 更新

修改插件内容后：提交并推送本仓库 → ZCode 插件管理页刷新市场 → 更新插件版本号（plugin.json 与 marketplace.json 中的 `version`）。
