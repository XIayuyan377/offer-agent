# 🌿 Offer 捕手

> AI 驱动的学生求职匹配与简历优化助手 —— 从"盲目海投"到"精准投递"

一个森系清新风格的求职 Web 应用，集成 AI 能力帮助学生完成：
- 📄 简历智能解析 → 候选人画像
- 💼 岗位 JD 智能解析
- 📊 多维度匹配评分 + 优劣势诊断
- ✨ 简历定向优化（3 种模式）
- 💬 AI 面试准备（高频题库 + 回答框架）

---

## 🛠 技术栈

| 层 | 技术 |
|---|---|
| 前端 | React 18 + TypeScript + Vite + Tailwind CSS + Framer Motion |
| 路由 | React Router v6 |
| 图表 | Recharts（雷达图、环形图） |
| 图标 | lucide-react |
| 后端 | Node.js + Express + TypeScript |
| 数据库 | SQLite（better-sqlite3） |
| AI | OpenAI SDK（兼容 DeepSeek / 通义千问 / 智谱 GLM 等） |
| 文件解析 | mammoth（.docx） + pdf-parse（.pdf） |

---

## 📁 项目结构

```
offer-hunter/
├── frontend/               # React 前端
│   ├── src/
│   │   ├── components/     # 公共组件（Navbar、LeafDecor、StepIndicator...）
│   │   ├── pages/          # 页面（HomePage、ResumeInputPage...）
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts
├── backend/                # Express 后端
│   ├── src/
│   │   ├── routes/         # API 路由
│   │   ├── services/       # 业务服务（AI 解析等）
│   │   ├── types/          # 类型定义
│   │   └── index.ts        # 入口
│   ├── package.json
│   └── tsconfig.json
├── shared/                 # 前后端共享类型
└── package.json            # 根脚本
```

---

## 🚀 快速开始

### 1. 安装依赖

```bash
# 根目录
npm run install:all
```

### 2. 配置环境变量

**backend/.env**
```env
PORT=3001
OPENAI_API_KEY=your_api_key_here
OPENAI_BASE_URL=https://api.deepseek.com/v1
OPENAI_MODEL=deepseek-chat
CORS_ORIGIN=http://localhost:5173
```

**frontend/.env**（可选）
```env
VITE_API_BASE_URL=http://localhost:3001/api
```

### 3. 启动开发环境

```bash
npm run dev
```

- 前端：`http://localhost:5173`
- 后端：`http://localhost:3001`

### 4. 生产构建

```bash
npm run build
npm run start
```

---

## 🎨 设计风格

- **主色调**：自然绿 `#22c55e` `#10b981`，奶白背景 `#fefdf8`
- **装饰元素**：月桂叶 SVG、水珠、飞鸟、虚线连接
- **动画**：呼吸 scale、悬浮上浮、滚动渐入、鼠标跟随光标
- **整体感觉**：森系清新、治愈、高级、不幼稚

---

## 📝 License

MIT
