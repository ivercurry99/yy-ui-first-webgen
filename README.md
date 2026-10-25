<svg width="1200" height="300" viewBox="0 0 1200 300" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="yy-ui-first-webgen">
  <style>
    .t { font-family: -apple-system, "Segoe UI", "Microsoft YaHei", sans-serif; }
  </style>
  <rect width="1200" height="300" fill="#0f172a"/>
  <rect x="60" y="60" width="420" height="180" rx="12" fill="#1e293b"/>
  <rect x="90" y="90" width="160" height="14" rx="7" fill="#38bdf8"/>
  <rect x="90" y="120" width="340" height="10" rx="5" fill="#334155"/>
  <rect x="90" y="140" width="300" height="10" rx="5" fill="#334155"/>
  <rect x="90" y="170" width="110" height="30" rx="8" fill="#f97316"/>
  <text x="520" y="130" class="t" font-size="44" font-weight="700" fill="#f1f5f9">yy-ui-first-webgen</text>
  <text x="520" y="175" class="t" font-size="24" fill="#94a3b8">先定视觉，再写代码 —— UI 先行的高还原开发流程</text>
  <text x="520" y="215" class="t" font-size="20" fill="#64748b">需求 → UI 提示词 → 效果图锁定 → 拆素材 → 高还原 → 对比验收</text>
</svg>

# yy-ui-first-webgen

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](SKILL.md)
[![Platform](https://img.shields.io/badge/platform-WorkBuddy%20%7C%20Claude%20Code%20%7C%20通用%20Agent-lightgrey.svg)](SKILL.md)

## 这是什么

一个 **Agent 技能**：让 AI 做"网页/前端项目"时不再一上来就乱写代码，而是走一套 **UI 先行的高还原流程**。解决的核心痛点：

> 「帮我写一个高级的网站」→ AI 自由发挥 → 你自己也不知道页面该长什么样 → 无限返工（"再高级一点""卡片换一下""Banner 再有设计感一点"）→ 项目越来越乱。

## 对我有什么用

- ✅ **返工次数大幅下降**：写第一行代码前，需求、页面结构、UI 视觉三件事全部锁死
- ✅ **还原度高**：复杂视觉素材单独拆分交给开发直接调用，而不是让 CSS 硬画
- ✅ **出问题能定位**：静态还原 → 响应式 → 动效三层分离，不混着开发
- ✅ **任何模型能跑**：无图像生成能力时自动降级为文字版设计规格书，流程不中断

## 工作流程

```
阶段 A 产品经理    需求 + 页面结构单（用户确认）
    ↓
阶段 B UI 设计师   具体化 UI 提示词 → 效果图 → 多轮修正 → 锁定
    ↓
阶段 C 素材拆分    CSS 能画的不拆；主体图/3D/纹理必拆，一素材一文件
    ↓
阶段 D 高还原开发  UI 图 + 素材清单 + 开发要求 → 按模块拆任务
    ↓
阶段 E 对比验收    7 项清单逐项核对（布局/字体/图片/留白/卡片/颜色/移动端）
```

核心纪律：修正指令必须量化（"Banner 缩小 15%"而不是"再像一点"）。

## 安装

```bash
# WorkBuddy / Claude Code（skills CLI）
npx skills add ivercurry99/yy-ui-first-webgen

# 或手动：把本仓库克隆到你的技能目录
git clone https://github.com/ivercurry99/yy-ui-first-webgen.git <你的技能目录>/yy-ui-first-webgen
```

## 触发方式

对 Agent 说：

- 「帮我做个网站，UI 先行」
- 「做个页面，要高还原设计稿」
- 「先出 UI 效果图，确认后再开发」

## 文件结构

```
├── SKILL.md                                  # 技能主流程（5 阶段）
└── references/
    ├── ui-prompt-template.md                 # UI 提示词模板 + 修正指令写法
    └── assets-and-degradation.md             # 素材拆分标准 + 降级方案
```

## License

[MIT](LICENSE) © ivercurry99
