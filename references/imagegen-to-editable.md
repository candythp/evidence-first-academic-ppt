# ImageGen layout images to editable academic PowerPoint

This is the default production route, not an optional illustration step. Current user materials and verified slide payloads determine the scientific content; reviewed ImageGen layouts determine the composition.

## 1. Prepare exact content before generation

After the material audit, brief lock, and evidence map, write `slide_payloads.json` with one stable slide ID per outline page. Include chapter, title, exact conclusion, local explanations, parameters/units, figure asset IDs, citations, and notes. Record each asset's source file/location, SHA-256, panel mapping, and any safe blank-margin trim or panel separation. Never infer new chart data from a raster figure.

Create `design_spec.md` and `layout_plan.md`. Specify the 16:9 canvas, shared-header groups, institution, typography, palette, title/conclusion hierarchy, body arrangements, and figure boxes. Use the saved school decks only for image/conclusion placement; the installed institution default remains 西安交通大学 unless overridden.

## 2. Generate representative candidates with ImageGen

Read the installed imagegen skill and use its actual generation/editing interface. Generate two or three candidates for representative evidence slides using the same payload and asset identities. Save actual returned files or supported image references; a prompt or invented image path is not proof of generation. Preserve model/tool metadata only when exposed.

Prompt pattern, adapted to the actual page:

> Design one 16:9 Chinese academic presentation layout. Use a restrained deep-blue palette, white background, numbered chapter navigation, left-aligned title, and a light-gray conclusion band. Institution: 西安交通大学, text only unless the supplied matching logo is authorized. Exact title: [verified title]. Exact conclusion: [verified conclusion]. Arrange [figure count, aspect ratios, and assigned boxes] with adjacent interpretation text [verified wording]. Use reserved plain figure slots labeled with asset IDs; do not draw plots, simulate scientific images, invent numeric values, or add research claims. Preserve the supplied visual grammar and vary body geometry to fit the evidence.

For edits or style references, supply actual available images using the tool's supported reference mechanism. If original figures are included in a generation call, treat generated versions as layout proxies, never original evidence. Show exact-source composites when supported; otherwise label the candidate as layout-only and identify the original figure mapping beside it. Collect the style choice once; explicit selection already given for this task is sufficient.

## 3. Generate and review every page

Apply the selected visual grammar to every planned slide, including covers, section pages, processes, and conclusions. Each page needs a real ImageGen-produced layout image before its final editable reconstruction. Do not generate a few examples and fill the rest directly in PowerPoint.

Maintain `imagegen_manifest.json`, recording one entry per page:

| Field | Purpose |
|---|---|
| `slide_id`, `slide_number` | Stable identity and outline order |
| `payload_path`, `payload_sha256` | Exact verified content authority |
| `generated_image`, `generated_image_sha256` | Actual ImageGen output |
| `tool`, `model_if_exposed`, `prompt`, `reference_images` | Truthful generation provenance |
| `layout_reference`, `layout_reference_sha256` | Frozen reviewed reconstruction reference |
| `original_assets` | IDs, paths, SHA-256, placement boxes, panel mappings |
| `header_group`, `style_selection_id` | Common visual grammar |
| `corrections`, `review_status` | Text reconciliation, asset replacement, acceptance |

Use normalized boxes `[x, y, width, height]` relative to the 16:9 canvas; record actual image dimensions. Normalize composition to 16:9 without stretching evidence. Keep raw generation images immutable. Reconcile wording, numbers, units, and formulas against the payload rather than trusting OCR or generated glyphs. Regenerate defective layout regions or document exact native-text corrections when the layout itself is sound. Never invent unreadable wording.

For evidence-complete previews, place original scientific assets in the reviewed boxes using supported composition/rendering tools. Keep that composite separate from the raw ImageGen image and record the method. Deterministic composition is permitted after genuine ImageGen generation; it does not substitute for that generation. If exact composition is unavailable, retain a layout-only reference with explicit original-asset placements, then insert original figures during editable reconstruction. Do not present generated figure proxies as completed scientific previews.

Inspect the full image sequence for factual correctness, chapter/branding drift, density, figure size, local explanations, and repeated body grids. Correct affected pages and freeze reviewed references before final reconstruction. Original evidence and payloads override layout-image discrepancies, with corrections recorded.

## 4. Reconstruct isolated editable pages

Adapt useful mechanisms from the installed `codeximage-to-editable-ppt-v2-2`: immutable page sources, per-page ownership, shared masthead seeds, isolated workers, rendered comparisons, and ordered OpenXML merging. This academic route does not invoke its unchanged strict validator. Do not run its `prepare`, `record`, or `publish` commands against an academic bundle and imply the contracts are interchangeable.

Classify each object by role:

- **Editable text:** navigation, slide titles, page-level claims, interpretation, external panel/parameter labels, citations, page numbers. Wording comes from the payload; position comes from the layout reference.
- **Native structure:** simple backgrounds, bands, panels, tables, slide connectors, and source-grounded process/relationship diagrams.
- **Original scientific asset:** preserve the exact source figure, plot, microscopy image, or coherent panel group as an independent picture, including integrated axes, legends, labels, scale bars, arrows, and trajectories. This is an explicit scientific-fidelity exception to editable text inside every raster object. Do not erase labels or patch scientific pixels. Data-editable charts require supplied data and an explicit request.
- **Independent complex artwork/logo:** use authorized assets with reviewed crops/transparency. Keep arrows, points, and shading together with a complex illustration when separating them damages meaning; external slide connectors remain native.

Raster asset count follows the evidence, including one-figure and no-figure slides. Do not split a coherent figure or add an irrelevant image to meet V2.1's minimum-PNG rule. Each original asset and native object has one owner. Do not duplicate raster labels or connectors underneath editable replacements.

After image review, build and render one native header seed per shared group. Reuse its actual objects, positions, styles, and authorized logo; prose alone does not lock a header. Cover/section variants may have separate groups. Keep body objects clear of the reserved header region. Record allowed page-specific active-navigation changes.

Construct one-page decks in private `page_tasks/<slide_id>/` directories, with source references, assets, build scripts, manifests, renders, and QA. Build manifests alongside objects with stable shape names, representations, source/asset IDs, positions, z-order, decisions, and review status. Never insert the whole layout image as a visible slide, cover its text with boxes, or reconstruct it as screenshot strips.

Sequential reconstruction is valid. When page-agent delegation is authorized and available, assign isolated tasks with this same contract, verified runtime/renderer, payload, frozen header seed, and layout references. Use actual worker slots; additional pages may run in later batches without claiming all pages overlapped. Do not create additional user-visible tasks without explicit authorization. Do not report strict V2.2 concurrency success for serial/batched execution.

If the user explicitly requests original strict V2.2 conversion, read and follow that skill's required references, preflight confirmation, page-worker authorization, complete V2.1 bundles, and unchanged validators. Explain the different treatment of embedded figure labels and resolve scope before using that strict route. This academic adaptation remains the default here.

## 5. Render and accept pages before merge

Render each actual reconstructed PPTX, preferably with Microsoft PowerPoint. Compare with reviewed layout references and original scientific assets, including enlarged charts/formulas. Verify:

1. Editable slide text matches the payload, with no raster-text duplication or unsupported scientific content.
2. Scientific assets preserve source hashes/approved derivatives, complete evidence, panel mapping, and readable axes/legends. Check rendered crops as well as byte identity.
3. Native structure is editable and the shared header follows its seed and recorded variants.
4. No overflow, off-slide shapes, clipping, accidental overlap, duplicate assets, or unreadable font substitution remains.
5. Notes and citations match the final slide and source-supported interpretation.

Record renderer, inspected preview path/hash, representation exceptions, defects, corrections, and actual pass/fail result in `page_tasks/<slide_id>/qa.json`. An `approved` flag is not a substitute for rendering and inspection. If PowerPoint is unavailable, identify the actual faithful renderer and limits; do not claim native PowerPoint QA. If no meaningful renderer is available, report the blocker rather than marking the deck verified.

## 6. Merge and publish requested files

Merge accepted pages in outline order using the installed presentation/OpenXML workflow. Check count/order, canvas, object/media fingerprints, header consistency, original-asset references, and speaker notes. Merge helpers that drop notes or alter themes/fonts require repair and targeted rendering.

Reuse accepted renders after an unchanged structural merge. Rerender affected pages only when a concrete integrity failure, changed appearance, or user request warrants it. Verify the final saved PPTX hash and publish one merged deck. Keep intermediate PNGs, page decks, manifests, timing data, and QA bundles internal unless requested. Preview-only work stops before page-deck construction; preview-plus-PPTX work also publishes the evidence-complete image preview.
