---
name: demo-builder-style-guidelines
description: |
  Shared visual style guidance for Scout and Cowork demo-builder packages. Load before creating
  Word, Excel, PowerPoint, Page, image, or styled demo artifacts so every file in one demo uses a
  consistent, professional enterprise design system.
metadata:
  version: "1.0.0"
---

## Purpose

Use this support skill before creating or styling any document, workbook, presentation, Page,
image, diagram, template, or other visual artifact for Scout or Cowork demo-builder packages.

The guidance is based on general design, accessibility, and Microsoft Office authoring techniques:
consistent themes, readable sans-serif fonts, sufficient contrast, meaningful slide titles, alt
text, intentional reading order, and reusable PowerPoint masters/layouts. Do not copy any company's
actual brand system, proprietary template, or house style.

## Required demo style system

Before creating the first visual artifact, define one demo-specific style system and apply it to all
files in the package.

The style system must include:

1. **Color palette:** Choose at least three complementary colors that look professional against a
   white background. Include one primary color, one secondary color, and one accent color. Add one
   neutral dark text color and one light background or divider color when useful.
2. **Color use:** Use the same colors across Word, Excel, PowerPoint, Pages, Markdown exports, CSV
   companion notes, diagrams, charts, and images. Use color to reinforce hierarchy, not as the only
   way to communicate meaning.
3. **Typography:** Use readable sans-serif fonts or Office-safe font families. Keep body text in a
   readable range, normally 10-12 pt for documents and workbooks, 18 pt or larger for slide body
   text, and larger sizes for headings. Avoid novelty, condensed, script, decorative, or tiny fonts.
4. **Layout system:** Define consistent title treatments, heading levels, margins, spacing, table
   styles, chart colors, callout styles, banner treatment, header/footer treatment, and icon/image
   style.
5. **Enterprise tone:** Make the design corporate, clean, and professional without being sparse.
   Use styled banners, headers, tables, section dividers, and callouts where they improve scanning.
   Avoid plain default styling, clutter, novelty visuals, or excessive decoration.

## Artifact-specific rules

### Word and Pages

- Use a styled title area or banner, clear headings, section headers, table styles, and subtle
  dividers.
- Include enough visual structure that the document looks like an enterprise-ready business artifact
  rather than a plain text export.
- Keep paragraphs short, use tables for structured comparisons, and use callouts for decisions,
  risks, or next steps.
- Use consistent header/footer treatment where appropriate, including unobtrusive
  `Classification: Public` placement.

### Excel

- Style every worksheet, including secondary and lookup sheets.
- Use a title row, filled header band, readable column widths, frozen headers, table formatting,
  consistent number/date formats, and palette-aligned charts or summaries.
- Use conditional formatting sparingly and never rely on color alone; pair color with labels,
  statuses, icons, or text.

### PowerPoint

- Use PowerPoint themes, slide masters, or reusable layouts so every slide shares the same palette,
  typography, spacing, title treatment, and footer treatment.
- Use AI-generated images or the PowerPoint stock/library image experience when imagery is needed.
  Images must be public-safe, business-appropriate, and consistent with the demo's invented
  scenario. Do not use customer images, copyrighted source images, or confidential screenshots.
- Give every slide a unique title, check reading order, add alt text for meaningful visuals, and
  maintain sufficient contrast.
- Use banners, section headers, styled tables, and clean data visuals. Do not leave slides as plain
  bullets unless the content genuinely calls for it.

### Diagrams and visual exports

- Use the same palette and typography treatment as the rest of the package.
- Prefer simple hierarchy, clear labels, high contrast, and enough whitespace to read quickly.
- Export images or media into the branch-appropriate `demo/sample-data/` location when they are part
  of the runnable demo.

## Validation checklist

Before publishing or reporting completion:

1. Confirm one palette with at least three complementary colors is documented or consistently
   inferable from the artifacts.
2. Confirm all documents for the same demo use the same colors, typography, headings, table style,
   and visual treatment.
3. Confirm Word/Page outputs include styled banners, headers, sections, tables, or callouts where
   useful and are not plain default documents.
4. Confirm Excel worksheets are all styled and readable.
5. Confirm PowerPoint uses a shared theme/master/layout approach and uses AI images or PowerPoint
   library images only when imagery is needed.
6. Confirm text contrast is sufficient, color is not the only signal, slide titles are unique, and
   meaningful visuals have alt text.
7. Confirm the final design feels enterprise-ready: professional, clean, and sufficiently rich
   without looking sparse or ornamental.
