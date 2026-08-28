\# 技术设计



\## 技术栈



\- 框架：Astro（静态生成，SEO 友好）

\- 样式：Tailwind CSS

\- 部署：Vercel / Netlify（Git 推送自动上线）

\- 语言：TypeScript



\##  项目管理



目录结构：



/

├── src/

│   ├── pages/        # 页面路由（index、projects、about）

│   ├── components/   # 可复用组件（卡片、导航栏）

│   └── data/         # 数据源

└── public/           # 静态资源（图片、图标）



\- 每个页面 = `src/pages/` 下一个文件

\- 组件只负责展示，不写死数据



\## 数据管理



单一数据源：所有项目信息存于 `src/data/projects.json`



字段结构：



```json

{

&#x20; "id": "task-app",

&#x20; "title": "任务管理 App",

&#x20; "description": "一句话简介",

&#x20; "tags": \["React", "Firebase"],

&#x20; "image": "/images/task-app.png",

&#x20; "demo": "https://...",

&#x20; "github": "https://github.com/you/repo",

&#x20; "featured": true,

&#x20; "date": "2026-05"

}

更新流程：新增项目 → 只改 JSON → Git 提交 → 自动部署

扩展预留：后期可接 Decap CMS 实现网页端可视化编辑

