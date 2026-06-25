---
name: premises-public-liability-insurance-skill
description: Build and update premises public liability insurance quote tools and quote sheets for Taiwanese insurance agency workflows. Use when the user asks for 處所公共意外險, 公共意外責任險, public liability quote forms, public-liability quotation webpages, or PDF-ready quote output with insured information, premises details, liability limits, deductibles, and optional endorsements.
---

# Premises Public Liability Insurance Quote Skill

Use this skill to create or revise a premises public liability insurance quote system similar to the existing commercial fire insurance quote tool style.

## Core Workflow

1. Read `references/public-liability-quote-rules.md` before changing fields, wording, or output logic.
2. Start from `assets/premises-public-liability-quote-tool.html` when creating a first-version standalone webpage.
3. Keep public liability tools separate from commercial fire insurance tools and repositories.
4. Use Traditional Chinese UI text.
5. Use fake sample data only. Never preserve real customer names, tax IDs, phone numbers, or addresses from screenshots.
6. Generate a printable output area suitable for browser "Print / Save as PDF".

## Expected Web Tool Shape

- Left side: input form.
- Right side: output quote preview.
- Toolbar order: `帶入範例`, `清空`, `產生報價單`, `列印 / 存成 PDF`.
- Status text: `尚未產生`, then `已產生` or `已清空`.
- Yellow section headers in the output, matching the commercial fire insurance quote style.
- Do not include `續保資料` or `保險期間` unless the user explicitly asks.
- Do not include `建築結構` for public liability insurance.

## Required Inputs

- 被保險人資訊: 公司名稱, 統一編號, 代表人, 電話, 通訊地址.
- 處所資料: 名稱, 處所地址, 坪數, 使用性質, 是否有招牌, 是否有電梯, 烤漆爐數量, 是否有修理廠, 樓層數, 火災受信總機, 消防撒水系統, 室外停車場.
- 報價額度: 每一人體傷, 每一事故體傷, 每一事故財損, 最高賠償限額, 自負額.
- 附加條款: provide default checkbox items and allow custom additions.
- 備註.

## Output Requirements

- Show 被保險人資訊 first.
- Show 公共意外險處所資料 as a table.
- Show 報價額度 as a table.
- Show selected 附加條款.
- Show 備註.
- Format plain numeric amounts with thousands separators when displayed.

## Bundled Resources

- `assets/premises-public-liability-quote-tool.html`: standalone first-version webpage.
- `references/public-liability-quote-rules.md`: field list, default clauses, and formatting rules.
