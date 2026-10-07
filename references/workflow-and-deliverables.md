# Workflow and deliverables

## Working files and delivery files

Use a dedicated internal work directory and keep source files read-only. Maintain:

- `brief_lock.json`, including `production_mode: "imagegen_then_editable"` or the user's explicit override;
- `material_audit.md`, `content_outline.md`, `evidence_map.json`;
- `slide_payloads.json`, `layout_plan.md`, `design_spec.md`, `style_selection.json`;
- `imagegen_manifest.json` and immutable raw generation images;
- reviewed layout references, exact-source composites when available, and a full-deck contact sheet;
- shared-header seeds and private `page_tasks/<slide_id>/` construction/QA bundles for editable-deck work;
- merge integrity report and final saved-file hash.

Create only files needed by the requested scope. Keep internal maps, JSON, scripts, raw images, and page decks out of the delivery folder. Default editable-deck delivery is one merged PPTX with notes embedded. Deliver the full-deck preview or internal reports when the user asks for them or asks for preview plus PPTX.

## Default sequence

1. Audit sources and lock chapters, institution, and production mode.
2. Build the evidence map and exact per-page payloads.
3. Generate representative layout candidates with the actual ImageGen tool and the same source assets.
4. Collect the style choice once; reuse an explicit choice already given for this task.
5. Write the per-page plan and generate an ImageGen layout image for every slide.
6. Review the full image sequence, reconcile text with payloads, map original assets, and freeze reconstruction references.
7. For preview-only work, deliver reviewed evidence-complete previews and stop without creating any PPTX.
8. For editable-deck work, create shared native header seeds and isolated one-page editable reconstructions.
9. Render, compare, and accept each page, preserving original scientific assets and documenting embedded-label exceptions.
10. Merge accepted pages in outline order, verify structure/assets/headers/notes and saved-file hash, then publish requested files.

Read [ImageGen-to-editable workflow](imagegen-to-editable.md) for provenance, original assets, reconstruction, optional page agents, and merge gates. A deterministic native preview without an ImageGen-generated layout for each page does not satisfy the default mode.

Record selected candidate, liked/rejected features, and requested changes. When the user corrects pages, update payloads/evidence mappings if content changed, then the layout plan and style record. Regenerate and reconstruct affected pages; refresh the contact sheet and merged deck. Keep earlier versions internally when comparison is useful.

## Editability contract

Navigation, titles, slide text, conclusion/parameter bands, external panel mapping, slide arrows/connectors, tables, process diagrams, and page numbers are native editable objects. Original scientific figures remain independent image objects, preserving embedded axes, legends, labels, scale bars, and coherent artwork. State this boundary accurately; do not claim all internal figure labels are editable. Charts are data-editable only when rebuilt from supplied data at the user's request.

## QA and reporting

Review generated images and rendered reconstructed pages. Confirm source-supported claims, nearby explanations, correct branding, parameter mapping, original evidence, varied evidence-driven layouts, readable figures, accurate notes, and no historical-template residue. Check generation provenance for every page and actual editability, rather than trusting a convincing screenshot.

Reuse accepted page renders after an unchanged ordered merge; verify count/order, canvas, objects/assets, headers, notes, and final hash. Report only checks actually performed. Name the renderer and material limits. Never claim an unchanged V2.1/V2.2 validator pass for this academic adaptation. Failed gates remain unfinished work.

For preview-only work, publish evidence-complete previews. Clearly label layout-only previews when exact original-asset composition was unavailable; do not claim an evidence-complete preview in that case.
