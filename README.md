# Claude Config

Claude Code 全局配置文件备份。

## 文件说明

| 文件 | 说明 |
|------|------|
| `CLAUDE.md` | 全局指令配置（用户背景、信息来源、行为规则等） |
| `settings.json` | Claude Code 运行时配置（需替换 token） |

## 使用方法

1. **克隆此仓库**
2. **配置 `settings.json`**：将 `YOUR_ANTHROPIC_TOKEN_HERE` 替换为你的实际 `ANTHROPIC_AUTH_TOKEN`
3. **复制到 `~/.claude/`**：
   ```bash
   cp CLAUDE.md ~/.claude/
   cp settings.json ~/.claude/
   ```

## 注意事项

- `settings.json` 中的 `ANTHROPIC_AUTH_TOKEN` **必须替换**为你的实际 token，否则无法使用
- `settings.local.json` 为本地扩展权限配置，未包含在此仓库中
