## 7. 标准记忆格式

每条长期记忆使用 Markdown 格式，并包含以下元数据：

```yaml
---
id: unique-memory-id
type: business
subject: entity-or-topic
scope: global-or-project
created_at: YYYY-MM-DD
updated_at: YYYY-MM-DD
last_verified_at: null
valid_until: null
version: 1
status: active
priority: high
confidence: high
evidence_type: USER_CONFIRMED
source: conversation-reference
tags: []
related: []
supersedes: []
---
```

正文结构：

### 核心记忆

用简洁、准确的语言记录信息。

### 背景与适用条件

保留理解该记忆所需的必要上下文。

### 决策依据或证据

记录用户确认、测试结果或其他证据。

### 来源

记录可获得的对话标题、日期、链接、文件路径或消息位置。

无法获得的来源字段标记为 unknown。



## 9. 记忆存储

建议知识库目录：

```text
AI-Memory/
  INDEX.md
  01_Profile/
  02_Preferences/
  03_Business/
  04_Projects/
  05_Decisions/
  06_Knowledge/
  07_Experience/
  08_Skills/
  09_Tasks/
  10_Corrections/
  90_Sessions/
  99_Archive/
```

按照实际需要创建文件，不为每次蒸馏生成空白分类文件。

每个主题维护一个主要权威记录，其他记录通过关联链接引用。

更新 INDEX.md 时保留已有有效内容。

知识库路径由用户明确指定。

默认不创建、不覆盖、不删除知识库文件。



使用 [记忆模板](../assets/memory-template.md) 或 [项目模板](../assets/project-template.md)。记录创建日期与事实发生日期分别处理；未知事实日期标记 unknown。
