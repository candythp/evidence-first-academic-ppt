# Evidence-First Academic PPT

A Codex skill for creating source-grounded academic PowerPoint decks from user-provided papers, reports, figures, images, and data. By default it generates an ImageGen layout image for every slide, then reconstructs an editable PPTX from reviewed layouts and original research figures.

The default visual direction is a restrained deep-blue academic style: numbered top navigation, conclusion-first slide hierarchy, real scientific figures as the evidence layer, explicit panel/parameter mapping, adaptive interpretation layouts, and local explanations placed beside the evidence they interpret.

## What makes it different

- The user chooses the chapter structure before authoring.
- The workflow blocks final-deck generation when only text or only images are supplied.
- Every scientific image and conclusion is traced to the user's current materials.
- This local installation defaults to 西安交通大学 (Xi'an Jiaotong University), unless the user specifies another institution or no institution. A matching authorized asset is required to include a logo; historical template branding is never reused automatically.
- Two or three ImageGen layout candidates are shown before the full deck is produced; every page then gets an ImageGen-generated layout reference.
- The selected candidate becomes a visual grammar, while each slide receives its own evidence-driven layout plan.
- Result and discussion slides pair one page-level claim with readable evidence and a nearby explanation for each distinct figure group.
- Shared condition/data bands are used when they clarify comparisons rather than reserved as a fixed footer.
- Research-problem chapters are derived from the source introduction, engineering background, literature status, and stated research gaps.
- Process diagrams may be rebuilt as editable native shapes when the source description fully specifies the logic.
- Reconstructed pages reuse native header seeds, receive isolated rendered QA, and merge in outline order, adapting the useful mechanisms of `codeximage-to-editable-ppt-v2-2`.
- The PPTX keeps slide structure, external labels, slide arrows, and explanatory text editable; original scientific figures preserve embedded labels and artwork intact.
- Default delivery is one merged PPTX with embedded notes. Generation images, page decks, manifests, and QA remain internal unless requested.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/candythp/evidence-first-academic-ppt.git "$HOME/.codex/skills/evidence-first-academic-ppt"
```

Restart Codex if the skill list does not refresh automatically.

## Use

Invoke `$evidence-first-academic-ppt` and attach the complete paper or report together with its figures or data files. The skill audits materials, applies the installed institution default, and resolves chapter or branding choices. It generates candidates with ImageGen, records the selection, generates and reviews layouts for every page, and only then reconstructs editable slides. Preview-only requests stop before PPTX construction. A native-only route requires an explicit user choice. See [ImageGen-to-editable workflow](references/imagegen-to-editable.md). The two saved PPTX examples remain image/conclusion layout references; see [local defaults and saved layout references](references/local-layout-references.md).

## Evidence policy

AI image generation designs composition. It must not become the source of scientific evidence, invent curves, infer exact values from pixels, or add unsupported conclusions. Verified payloads determine text, and original figures replace generated proxies in final evidence-complete previews and the PPTX. The academic route preserves scientific pixels and does not claim the unchanged strict V2.1/V2.2 editability contract or validator pass.

## License

MIT
