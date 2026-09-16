# Layout planning

Create `layout_plan.md` after the user selects a visual candidate and before generating the full deck. The selected candidate defines navigation, title hierarchy, conclusion treatment, palette, typography, branding, and information-band styling. It does not force every slide into the same body grid.

## Required row for each slide

Record:

- slide number, chapter, and purpose;
- evidence count and source locations;
- figure aspect ratios and whether a source image contains multiple panels or large blank margins;
- argumentative relationship: sequence, comparison, controlled variable, primary/supporting evidence, or mechanism-to-decision;
- chosen body composition;
- reason the composition fits the evidence;
- panel/parameter mapping and bottom-band contents;
- any source-grounded native diagram to rebuild.

## Research-problem chapter

When the chapter is called “研究问题” or equivalent, build it from the introduction and literature-status sections:

1. Show the engineering system, real operating disturbances, coupled consequences, and the unresolved engineering decision.
2. Summarize the limitations of existing work.
3. Map each limitation to the paper's research response or technical route.

Do not open this chapter by explaining why the author's numerical model is useful. The model belongs after the engineering problem and research gap are clear.

## Body-layout selection

Choose from the evidence rather than from a fixed template:

- **No scientific figure:** use a source-grounded engineering-system map, gap-to-response map, model relationship, or process flow.
- **One dominant figure:** maximize the figure; place up to three arrow explanations beside it or below it according to the aspect ratio.
- **Two comparable figures:** use a balanced comparison split with one shared conclusion, or a primary/supporting asymmetric layout when the evidence is unequal.
- **Three equal figures:** use three parallel columns or rows with short figure-specific conclusions.
- **Three paired-condition figures:** use a Scheme-A layout with three interpretation items on one side and a two-column-by-three-row figure group on the other.
- **Result followed by engineering interpretation:** adjacent slides may intentionally repeat Scheme A when they form one continuous argument; change image height, width, and grouping to fit each slide's evidence.
- **Staged operating event:** place the action timeline above parallel response figures.
- **Algorithm or calculation flow:** use a full-width native process diagram with visible loops, branches, convergence tests, and outputs.

## Figure sizing

Make axes, legends, color bars, scale bars, and condition labels readable at presentation size. Trim blank source margins when this does not remove evidence. Panel groups may be separated or their display boxes may use independently tuned width and height when the user explicitly prefers a compact comparison grid. Preserve every scientific element and do not redraw curves, change data, or omit conditions.

Avoid shrinking all figures to preserve a habitual text column. When the figure count is low, enlarge the evidence or use a source-grounded native diagram. Empty space is acceptable only when it clarifies hierarchy.

## Sequence audit

Review the contact sheet before delivery:

- avoid the same body wireframe on more than two consecutive evidence slides unless the argument genuinely continues;
- avoid repeating a row of identical conclusion cards across the deck;
- check that layout changes follow evidence changes rather than decoration;
- confirm that related slides retain enough visual continuity to be read as one section;
- update `style_selection.json` with explicit user feedback and regenerate affected pages.
