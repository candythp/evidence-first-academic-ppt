# Evidence-First Academic PPT

A Codex skill for creating editable, source-grounded academic PowerPoint decks from user-provided papers, reports, figures, images, and data.

The default visual direction is a restrained deep-blue academic style: numbered top navigation, conclusion-first slide hierarchy, real scientific figures as the evidence layer, explicit panel/parameter mapping, adaptive interpretation layouts, and a data band beneath the evidence area.

## What makes it different

- The user chooses the chapter structure before authoring.
- The workflow blocks final-deck generation when only text or only images are supplied.
- Every scientific image and conclusion is traced to the user's current materials.
- Institution name and logo are confirmed for each task; historical branding is never reused automatically.
- Two or three layout candidates are shown before the full deck is produced.
- The selected candidate becomes a visual grammar, while each slide receives its own evidence-driven layout plan.
- Research-problem chapters are derived from the source introduction, engineering background, literature status, and stated research gaps.
- Process diagrams may be rebuilt as editable native shapes when the source description fully specifies the logic.
- The final PPTX keeps slide structure, labels, arrows, and explanatory text editable.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/candythp/evidence-first-academic-ppt.git "$HOME/.codex/skills/evidence-first-academic-ppt"
```

Restart Codex if the skill list does not refresh automatically.

## Use

Invoke `$evidence-first-academic-ppt` and attach the complete paper or report together with its figures or data files. The skill first audits the materials and asks you to choose the chapter structure and institution branding. It then presents layout candidates, records the selection, plans every slide, and produces only the requested scope: preview, editable PPTX, or both.

## Evidence policy

AI image generation is used only to explore layout. It must not redraw scientific evidence, invent curves, infer exact values from pixels, or add unsupported conclusions.

## License

MIT
