# Intake and chapter choices

Use one compact intake after inspecting the available material. Questions that require files cannot be satisfied by a multiple-choice answer; after the audit, request the exact missing files or mapping directly.

## Chapter-structure question

Suggested UI question:

> 本次汇报采用哪套章标题？如果选择自定义，请按顺序填写全部章标题。

Options:

- **研究汇报（推荐）** — 研究问题 / 数值模型或研究方法 / 模型或方法验证 / 结果与讨论 / 总结
- **IMRaD 期刊结构** — 引言 / 方法 / 结果 / 讨论 / 结论
- **实验研究结构** — 研究背景 / 实验装置与方法 / 结果 / 机理讨论 / 结论

Use the free-form answer for journal-specific or custom titles. A numerical study may rename “研究方法” to “数值模型”; an experimental study may replace “模型验证” with “实验验证” or “装置标定”. Do not force every deck into five chapters if the user provides a stronger structure.

## Branding question

Apply [local defaults and saved layout references](local-layout-references.md) and explicit current user choices first. Ask the following only when branding is still unresolved, such as a requested logo without an authorized matching asset. Do not ask the user to reconfirm an already resolved institution or text-only treatment.

Suggested UI question when needed:

> 本次 PPT 的学校或机构标识如何处理？

Options:

- **使用本次材料中的机构（推荐）** — Use the current files only after confirming the institution name and authorized logo.
- **使用我提供的新 Logo** — Wait for the logo and institution name before final authoring.
- **不使用机构 Logo** — Use a clean text header or no institution mark.

Never infer the user's institution from a template filename, a previous task, a color scheme, or an unrelated author affiliation. When multiple affiliations appear, ask which one owns the presentation.

## Scope question

Ask presentation duration or target slide count only when missing. Use duration to size the story; do not pad to a page target. A practical starting point is roughly one content slide per minute after the opening, but evidence density and audience determine the final count.

## Brief lock

Save:

```json
{
  "purpose": "group meeting | research update | paper reading | defense | conference",
  "audience": "",
  "duration_minutes": null,
  "chapter_titles": [],
  "institution_name": "",
  "logo_policy": "current-material | user-provided | none",
  "production_mode": "imagegen_then_editable",
  "requested_deliverables": ["pptx"],
  "language": "zh-CN",
  "visible_source_policy": "user-owned-hidden | visible | mixed"
}
```

Default to `imagegen_then_editable` without asking the user to choose a production method. `requested_deliverables` records the user's actual scope (`pptx`, `preview`, or both); working evidence/QA files remain internal. Set `production_mode` to `native_only` only for an explicit user override, and record its reason. Missing ImageGen access is a capability blocker, not an implicit override.
