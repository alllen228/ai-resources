# AI 教程资源库

展示每天自动采集的 B站 AI 教程资源。

## 访问方式

**方式一：直接打开**
```bash
# 在浏览器地址栏输入
file:///home/yingjie/.openclaw/www/index.html
```

**方式二：本地服务器**
```bash
cd ~/.openclaw/www
python3 -m http.server 8080
# 然后访问 http://localhost:8080
```

## 功能

- 🌙 **主题切换**：点击右上角 🌙/☀️ 按钮
- 📅 **日期分组**：按采集日期显示，可折叠/展开
- 🔍 **实时搜索**：标题和摘要全文搜索
- 🏷️ **分类筛选**：Agent Skills / LangGraph / LangChain / MCP / RAG / Prompt / Cursor / 入门
- 📊 **数据统计**：显示总资源数、采集天数、今日新增
- 📱 **响应式**：支持移动端访问

## 数据更新

### 自动更新
- Cron 任务每天 02:00 自动执行
- 采集 B站 AI 相关视频教程
- 自动同步到网页

### 手动更新
```bash
# 运行采集脚本
bash ~/.openclaw/scripts/video-scraper/nightly-scan.sh

# 运行同步脚本（采集后自动执行）
/home/yingjie/.local/mamba/bin/python3 ~/.openclaw/scripts/video-scraper/sync-webdata.py
```

## 文件结构

```
~/.openclaw/
├── www/
│   ├── index.html      # 网页主文件
│   └── README.md       # 本文件
├── scripts/
│   └── video-scraper/
│       ├── nightly-scan.sh   # 采集脚本
│       └── sync-webdata.py  # 同步脚本
└── workspace/
    └── memory/
        └── video-research/   # 每日采集的 Markdown 文件
            ├── 2026-04-04-ai-agent-resources.md
            └── ...
```

## 数据来源

每日 02:00 自动采集以下内容：
- B站 AI Agent 教程
- B站 LangChain / LangGraph / MCP 教程
- B站 Prompt Engineering / RAG 知识库教程

关键词覆盖：Agent Skills / LangGraph / LangChain / LangChain / MCP / RAG / Prompt / Cursor / Ollama / DeepSeek
