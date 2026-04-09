## Global Claude.md

## 用户背景
- 金融专业本硕，热爱利用新技术提升工作生活体验
- 擅长于学习，懂一些Python编程语言、AI大模型技术
- 对于信息来源和准确性要求很高

## 信息来源

用户常关注以下平台和账号，获取金融/宏观/投资信息：

### 微信公众号
- 培风客
- 华尔街见闻
- 地平线全球策略
- 猫笔刀
- E起来养基
- 表舅是养基大户

### X（Twitter）
- 获取海外金融圈实时动态和宏观观点

### YouTube
- 获取视频类金融分析内容

### Bilibili
- 获取视频类金融分析内容

## 核心行为规则

- **先规划再动手**：任务开始前输出目标、步骤、工具选择，等用户确认后再执行
- **需求模糊时追问到底**：不猜测，不假设，不在模糊状态下开始工作
- **每步验证**：配置修改、安装、删除等操作完成后，立即用命令验证结果，不等用户报错
- **方向错了立即停**：发现当前路径不通，停下汇报，不要在错误方向上继续尝试
- **陌生操作先看文档**：所有不熟悉的操作，先查阅官方文档/说明，严格按官方指引操作，不猜测、不臆断

## 工具与环境

- 提到 npm 包/library 时，先确认是 Claude Code skill、MCP server 还是 CLI 工具
- 遇到 CAPTCHA/反爬/登录墙：立即告知用户，不要静默重试
- 下载任务：先验证文件存在且可访问，再声称成功
- 只要任务有API可以参考，永远参考API文档，以避免不必要的错误
- **文档/文件生成：必须使用对应 skill，不得手动拼接或调用非 skill 工具**
  - Word (.docx) → `docx` skill
  - PowerPoint (.pptx) → `pptx` skill
  - Excel (.xlsx) → `xlsx` skill
  - PDF → `pdf` skill
  - 视频/字幕 → `youtube-transcript-cn` skill
  - 其他文件类型优先查找已有 skill，无对应 skill 时再说明

## 已安装 Skills（按功能分类）

### 核心能力
| Skill | 用途 |
|-------|------|
| `superpowers` | 超级能力集合（brainstorm/verification/execute-plan等） |
| `find-skills` | 搜索安装新 skill |
| `skill-creator` | 创建自定义 skill |
| `make-plan` | 生成结构化实施计划 |

### 飞书集成（Lark）
`lark-base` `lark-calendar` `lark-contact` `lark-doc` `lark-drive` `lark-event` `lark-im` `lark-mail` `lark-minutes` `lark-openapi-explorer` `lark-shared` `lark-sheets` `lark-skill-maker` `lark-task` `lark-vc` `lark-whiteboard` `lark-wiki` `lark-workflow-meeting-summary` `lark-workflow-standup-report`

### 文档生成
`docx` `pptx` `xlsx` `pdf`

### 金融研究
`stock-research-executor` `academic-search` `youtube-transcript-cn` `x-twitter-scraper` `exa-web-search-free` `web-access` `notebooklm`

### 浏览器/搜索
`agent-browser` `google-search-browser-use`

### 前端/开发
`frontend-design` `do` `smart-explore` `summarize`

### PUA 模式（高压驱动）
`pua` `pua-en` `pua-ja` `pua-loop` `mama` `pro` `p10` `p7` `p9` `shot` `yes` `timeline-report`

### 其他
`homework-assistant`

## 已安装 Plugins

| Plugin | 用途 | 状态 |
|--------|------|------|
| `superpowers` | 超级能力扩展 | ✔ enabled |
| `github` | GitHub 集成 | ✔ enabled |
| `code-review` | 代码审查 | ✔ enabled |
| `claude-md-management` | MD 文件管理（含 `revise-claude-md`、`claude-md-improver` skill）| ✔ enabled |
| `playwright` | 浏览器自动化 | ✔ enabled |
| `claude-mem` | 记忆管理 | ✘ disabled |

## Plugins 与 Skills 核心区别
- **Plugins**（claude.com/plugins）：通过 `~/.claude/settings.json` → `enabledPlugins` 安装，格式 `name@claude-plugins-official`
- **Skills**：通过 `npx skills add <package>` 安装，用 `Skill` 工具调用
- **MCP Servers**：通过 `settings.json` → `mcpServers` 配置，当前有 `tradingview`

## 沟通偏好

- 说错方向会被立即打断，不需要留情面
- 不要冗长解释，给结论和依据
- 用 skill 封装重复任务