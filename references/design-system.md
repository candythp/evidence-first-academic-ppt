# Design system

## Default visual language

- 16:9 white canvas with a restrained deep-blue academic palette.
- Thin top navigation: current chapter centered or clearly highlighted; current institution logo at the upper right only when authorized.
- Left-aligned section title below navigation.
- Light-gray conclusion band directly below the title; short qualitative conclusion with selective blue emphasis.
- Scientific figures dominate the body. Preserve axes, color bars, legends, scale bars, and panel labels.
- Use arrow-list markers for parallel observations. Use numbered markers only for a true sequence or ordered method.
- Place fixed conditions and key values near the evidence. Use a shared band below the figure only when several panels share conditions, units, cases, or a quantitative summary.
- Use one sans-serif family that supports the deck language. Avoid decorative fonts, gradients, shadows, and unnecessary icons.
- When the selected style uses numbered top navigation, keep the active chapter as a dark-blue tab and use a two-level title hierarchy: small subsection/chapter label plus a large slide-specific title.

## Result layouts

Choose according to figure geometry:

All result layouts use the same reading hierarchy: page-level conclusion, readable evidence, then evidence-specific explanation adjacent to the figure group it interprets. The location of the explanation may change; its relationship to the evidence may not.

### Figure right, explanation left

Use for one wide or tall evidence group. The left column contains up to three arrow bullets: morphology, concentration or field distribution, and overall response. Put shared data beneath the figure on the right only when it helps the audience decode the comparison.

### Figure first, explanation below

Use for dense multi-panel figures. Put the figure group at maximum readable size, then use a compact arrow row or local explanation box below it. Add a parameter band only when the panels cannot be decoded from their own labels.

### Comparison split

Use for two conditions or methods with comparable figures. Align their plot areas, put the comparison claim in one shared conclusion band, and attach a local explanation to each side when the two evidence groups support different sub-findings.

### Parallel evidence row

Use for two or three figures with equal argumentative weight. Place them horizontally at the largest readable size. Put a short evidence-specific conclusion above or below each figure and use one shared conditions band only when needed. Do not force these slides into an explanation-left/figure-right split.

### Native process reconstruction

Use for calculation procedures, solver loops, model coupling, and technical routes. Rebuild the flow with editable boxes and arrows from the source description when the embedded flowchart is too narrow, small, or visually weak. Preserve the source sequence, branches, loops, and termination criteria. A process slide may use the full body width and does not need an arrow-list column.

### Density rule

Estimate the useful occupied area after reserving navigation, title, conclusion band, and any necessary condition labels. If the scientific evidence occupies less than roughly two thirds of the remaining body, enlarge it, change the arrangement, or convert source-described relationships into native diagrams. Do not reserve an empty bottom band or fill space with decorative shapes.

## Sequence-level composition

Decide layouts across the deck as a sequence, not page by page in isolation. A coherent deck can alternate among:

- engineering-system map for the research problem;
- research-gap list paired with a technical-route figure;
- three equal evidence columns for comparable plots;
- analysis-left / figure-grid-right for one dense multi-variable result;
- figure-left / engineering-decision-right for implications;
- asymmetric dashboard when one result is primary and two are supporting;
- timeline above parallel response plots for staged operating events;
- native full-width process flow for algorithms.

Keep the visual grammar consistent while changing the body geometry. Repetition should reflect repeated scientific structure, not convenience.

The chosen preview defines the visual baseline, not a rigid slide template. Adapt widths and positions to the evidence while preserving information hierarchy.

## Image-first consistency

Apply this visual system to ImageGen candidates and every full-deck layout image before editable reconstruction. Record common header groups, canvas, typography, and palette in `design_spec.md`; inspect the generated sequence for branding/navigation drift. After image review, reuse actual native header-seed objects across reconstructed pages, allowing only recorded active-chapter/page variants. Retain original scientific figures independently rather than extracting generated plots. See [ImageGen-to-editable workflow](imagegen-to-editable.md).

## Branding

Apply the institution default and layout-reference boundaries in [local defaults and saved layout references](local-layout-references.md), unless the current user specifies another institution or no institution. Deep blue is a visual default, not proof of an official school color. Use logos and official colors only from authorized matching assets or explicit current user instructions. Do not recolor a logo unless an official monochrome asset is supplied.
