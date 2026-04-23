# PETTI · 宠格测试

> 15 道题，找到你的本命宠物。
> 你以为你在测试，其实是一只老动物在观察你。

一个中文小动物性格测试网站 · 纯静态，单页 SPA · 受 [SBTI](https://sbti.unun.dev) 与 [DogTI](https://dogti.pages.dev/) 启发。

## 核心机制

- **15 道问题**，每题 3 个选项，场景化设计
- **4 个维度**（社交电量 / 行动驱动 / 决策思维 / 生活节奏）生成 4 维向量
- **24 种预设动物**签名向量，欧氏距离匹配最近的那一只
- 输出：动物图片 + slogan + 性格标签 + 动物视角人格解读

## 技术栈

- 原生 HTML + CSS + JavaScript，零依赖
- Google Fonts 加载 LXGW WenKai TC / Noto Serif SC
- Mobile-first 响应式（max-width 480px 居中）
- 可部署到任意静态托管（Cloudflare Pages / GitHub Pages / Vercel）

## 本地运行

```bash
python3 -m http.server 8765
# 访问 http://localhost:8765
```

## 文件结构

```
petti/
├── index.html           # 结构
├── styles.css           # 样式
├── app.js               # 逻辑
├── data/
│   ├── questions.json   # 15 道题
│   └── pets.json        # 24 种动物档案
├── images/              # 24 张动物图片
└── docs/                # 设计文档
```

## 修改内容

- **问题**：编辑 `data/questions.json`
- **动物档案**：编辑 `data/pets.json`，可调整 `vector`、`slogan`、`tags`、`interpretation`
- **配色**：`styles.css` 顶部 `:root` CSS 变量
