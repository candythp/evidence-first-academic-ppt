# Workflow and deliverables

## Project files

Create a dedicated output directory and keep source files read-only. Maintain:

- `brief_lock.json`
- `material_audit.md`
- `content_outline.md`
- `evidence_map.json`
- `layout_plan.md`
- `design_spec.md`
- `style_selection.json`
- `previews/candidates/`
- `previews/full-deck/`
- `exports/<presentation>.pptx`
- `exports/full-deck-preview.png`
- `qa/verification.md`

## Preview sequence

1. Audit sources and lock chapters/branding.
2. Build the evidence map and representative-slide copy.
3. Generate two or three layout candidates with identical evidence.
4. Composite the original scientific figures if the generation tool cannot preserve them exactly.
5. Wait for the user's explicit selection.
6. Create `layout_plan.md` for every slide, treating the selected candidate as a visual grammar rather than a repeated wireframe.
7. Generate or reconstruct the full-deck preview using the selected hierarchy and per-slide plan.
8. Inspect the full-deck sequence for repeated body layouts, undersized figures, unsupported claims, and empty areas.
9. Author the editable PPTX only when the user requests it.

Record selected candidate, liked features, rejected features, and requested modifications. Do not infer a long-term preference from silence.

When the user corrects specific pages, update `layout_plan.md` and `style_selection.json` with the explicit reason. Regenerate the affected pages and the contact sheet. Keep earlier previews as versioned files when comparison is useful.

## Editability contract

The following should be native editable objects: navigation, titles, body text, conclusion bands, parameter bands, panel mapping, arrows, connectors, tables, process diagrams, and page numbers. Original scientific figures may remain raster or vector image objects. Charts are data-editable only when rebuilt from user-provided data.

## QA

Render every slide. Verify:

- no overflow, clipping, or overlap;
- chapter title and page number are synchronized;
- current institution and logo treatment are correct;
- conclusion is supported by the displayed evidence;
- every panel parameter is mapped;
- axes, legends, color bars, and scale bars are readable;
- figures are not AI-redrawn;
- adjacent evidence slides do not repeat the same body wireframe without a source-driven reason;
- scientific figures use the largest practical readable size, with blank source margins trimmed when safe;
- speaker notes match the final slide;
- the PPTX package opens and expected native text objects exist.

Report only checks actually performed. If native PowerPoint was not used for rendering, say which renderer was used and avoid claiming native-app fidelity.

For preview-only work, report the rendered preview and QA artifacts and explicitly state that no PPTX was created.
