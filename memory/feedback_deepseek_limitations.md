---
name: deepseek-image-limitation
description: DeepSeek V4 PRO不支持图片识别，需用easyocr或切Claude模型替代
metadata: 
  node_type: memory
  type: feedback
  originSessionId: d0d863ef-3945-43f6-a05b-4bf850482237
---

DeepSeek V4 PRO 不支持多模态（图片识别），所有图片返回 "Unsupported Image"。

**Why:** 模型层面限制。Claude 支持图片识别但需要切换模型，切换会导致对话历史丢失。

**How to apply:**
- 需要识别图片时，用 Python easyocr 提取图片文字（pip install easyocr）
- 需要看图排版/色彩时，要求用户用语言描述
- 如需高质量图像识别，建议用户手动切换 Claude 模型（CC Switch）并新建对话
- 不要尝试 GUI 自动化切换模型（不靠谱且会丢对话）
