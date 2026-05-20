---
name: windows-bash-tips
description: Windows bash 环境下常用操作的注意事项和已知坑
metadata: 
  node_type: memory
  type: reference
  originSessionId: 2590ebdf-e48c-400f-aa5f-df68c04140ef
---

## 打开文件夹
- 错误: `explorer .` (bash 的 `.` 不是 Windows 路径)
- 错误: `start .` (start 是 cmd 内置命令)
- 正确: `/c/Windows/explorer.exe "C:\Users\zqs05"` 或 `powershell -Command "Invoke-Item 'C:\path'"`

## 临时文件路径
- bash 的 `/tmp/` 不可用，用 `$HOME/` 或绝对路径 `C:/Users/zqs05/`

## Python
- `python` (非 `python3`)
