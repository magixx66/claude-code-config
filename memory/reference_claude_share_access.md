---
name: claude-share-access
description: 如何访问 claude.ai/share 链接 — SeleniumBase UC 模式绕过 Cloudflare bot 检测
metadata: 
  node_type: memory
  type: reference
  originSessionId: 2590ebdf-e48c-400f-aa5f-df68c04140ef
---

访问 claude.ai/share 链接的方法：

1. curl/requests 能拿到 HTML 但只是 React SPA 空壳（`<div id="root"></div>`），对话数据由 JS 动态加载
2. Playwright 会被 Cloudflare bot 检测拦截（"Performing security verification"）
3. **SeleniumBase UC 模式** 能绕过 Cloudflare，JS 正常执行后提取内容

**How to apply:** 用户发来 claude.ai/share 链接时，用 `C:\Users\zqs05\fetch_claude_share.py` 脚本抓取：
```
python fetch_claude_share.py "https://claude.ai/share/<UUID>"
```
结果保存到 `claude_shares/<标题_短ID>/` 目录，包含 raw.html、conversation.txt、metadata.txt。
