# Technical Book Writer Skill

一个用于撰写科技类书籍的 Agent Skill，目标是在“专业严谨”和“入门可读”之间取得平衡。

## What It Does
- 以专业技术作者视角组织并撰写科技类书稿。
- 先生成严谨目录，再按章节展开正文。
- 支持目录到章节的锚点跳转。
- 对入门级内容采用“直觉 -> 定义 -> 示例”的表达方式。

## Skill Location
- `skills/technical-book-writer/SKILL.md`

## Core Requirements
- 科技内容要准确、术语统一、论证清晰。
- 目录与正文标题必须一一对应。
- 目录建议至少 3 级结构：卷/篇 -> 章 -> 节。
- 每章末尾给出小结和下一章衔接。

## Quick Usage
可直接给 Agent 这样的指令：

```text
请使用 technical-book-writer skill，写一本《给工程师的分布式系统入门》。
读者是 1-3 年经验后端工程师。
要求：先输出完整目录（可跳转），再写前两章正文。
```

## Output Shape
1. 书籍定位（书名、读者、目标）
2. 全书目录（带锚点跳转）
3. 分章正文（锚点与目录一致）
4. 全书总结（核心观点、实践建议、延伸阅读）

## Anchor Example

```md
- [第1章 研究背景](#ch1)
  - [1.1 问题定义](#ch1-1)

## <a id="ch1"></a>第1章 研究背景
### <a id="ch1-1"></a>1.1 问题定义
```

## Notes
- 当前仓库以 skill 为中心，`README.md` 用于快速说明用途与使用方式。
- 详细规则请以 `skills/technical-book-writer/SKILL.md` 为准。
