# Evidence-First Academic PPT

A Codex skill for creating editable, source-grounded academic PowerPoint decks from user-provided papers, reports, figures, images, and data.

The default visual direction is a restrained deep-blue academic style: top navigation, conclusion-first slide hierarchy, real scientific figures as the evidence layer, explicit panel/parameter mapping, arrow-list interpretation, and a data band beneath the figure.

## What makes it different

- The user chooses the chapter structure before authoring.
- The workflow blocks final-deck generation when only text or only images are supplied.
- Every scientific image and conclusion is traced to the user's current materials.
- Institution name and logo are confirmed for each task; historical branding is never reused automatically.
- Two or three layout candidates are shown before the full deck is produced.
- The final PPTX keeps slide structure, labels, arrows, and explanatory text editable.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/candythp/evidence-first-academic-ppt.git "$HOME/.codex/skills/evidence-first-academic-ppt"
```

Restart Codex if the skill list does not refresh automatically.

## Use

Invoke `$evidence-first-academic-ppt` and attach the complete paper or report together with its figures or data files. The skill will first audit the materials and ask you to choose the chapter structure and institution branding.

## Evidence policy

AI image generation is used only to explore layout. It must not redraw scientific evidence, invent curves, infer exact values from pixels, or add unsupported conclusions.

## License

MIT
