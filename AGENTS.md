\# 开发指令 · 粉色系个人作品集



\## 项目概述



\- 类型：个人静态作品集网站，展示个人项目、技能与联系方式

\- 技术栈：Astro + Tailwind CSS + TypeScript

\- 部署：Vercel，Git push 自动部署

\- 核心原则：内容与代码分离，数据统一存放于 `src/data/`



\## 目录规范



src/

├── pages/        # 路由页面：index.astro / projects.astro / about.astro

├── components/   # 展示组件：Card.astro / Navbar.astro / Footer.astro

├── layouts/      # BaseLayout.astro（公共 head、导航、页脚）

└── data/

&#x20;   ├── projects.json

&#x20;   └── profile.json



\## 设计要求（浅粉风格）



色板：



| 用途 | 色值 |

|---|---|

| 页面背景 | `#FFF5F7` |

| 卡片背景 | `#FFFFFF` |

| 主色（按钮/链接/高亮） | `#F8A5B8` |

| 主色深（hover/标题强调） | `#E87A96` |

| 正文文字 | `#4A3B40` |

| 描边/分割线 | `#FBD9E2` |



样式细则：



\- 圆角：卡片 `rounded-xl`，按钮 `rounded-full`

\- 阴影：使用极淡粉色阴影，如 `shadow-\[0\_4px\_16px\_rgba(248,165,184,0.25)]`

\- 交互：hover 时卡片轻微上浮 `hover:-translate-y-1 transition`

\- 字体：正文用系统默认无衬线；标题可加粗放大即可

\- 深浅对比要够：正文必须用深灰粉色 `#4A3B40`，禁止在浅背景上放白色或浅粉文字



\## 开发规范



\- 所有文案数据一律写入 `data/\*.json`，组件内禁止硬编码内容

\- 组件只接收 props 渲染，不直接 import 数据源以外的逻辑

\- 图片放 `public/images/`，命名小写中划线：`task-app-cover.png`

\- 提交信息格式：`feat: 新增xx` / `fix: 修复xx` / `style: 调整xx`

\- 每次改动后运行 `npm run build` 确认无报错再提交



\## 注意事项



1\. 配色以粉色为主，但整体面积控制：大面积用近白的粉底，主粉只做点缀，避免视觉疲劳

2\. 响应式优先：手机端单列布局，桌面端最多两列

3\. 外链（demo/GitHub）一律加 `target="\_blank" rel="noopener"`

4\. 暗色模式暂不做，避免配色方案复杂化

5\. 项目较少时（<3 个）隐藏「全部项目」页，首页直接展示

