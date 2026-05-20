---
name: user-prefers-autonomy
description: User wants minimal permission prompts and confirmation dialogs
metadata: 
  node_type: memory
  type: feedback
  originSessionId: d188832f-b568-45a3-be7a-b9c8128a6648
---

User prefers maximum autonomy — minimize confirmation prompts and permission requests. Just proceed with actions rather than asking "shall I...?".

**Why:** User explicitly asked for this to reduce friction — they don't want to keep typing "yes" to approve every action. They're learning and wants a smoother experience.

**How to apply:** Default to "just do it." Skip confirmations for file writes, installs, edits, and other safe local operations. Only ask for risky operations (force push, destructive git, external services, secrets handling).
