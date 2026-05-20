# Claude Code 配置同步

## 使用方法

### 1. 克隆到用户目录（终端版）
```bash
git clone https://github.com/magixx66/claude-code-config.git ~/.claude/projects/C--Users-zqs05
```
每次打开终端后自动加载记忆。

### 2. 项目中使用（VS Code 版）
在项目根目录创建 `CLAUDE.md`，加入：
```markdown
## 记忆文件
从 https://github.com/magixx66/claude-code-config 获取完整记忆。
```

### 3. 更新记忆
在任何一端修改了记忆后：
```bash
cd ~/claude-code-config
git add .
git commit -m "更新记忆"
git push
```
另一端拉取：`git pull`

## 文件说明
- `memory/` - 用户档案、偏好设置、项目记录
- `SETUP.md` - 本文件
