---
name: ppt-template-generator
description: Create reusable, editable PowerPoint template decks with a coherent visual system, representative slide layouts, and usage guidance. Use when the user wants a new PPT/PPTX template, slide style system, branded presentation starter, or reusable deck skeleton rather than a one-off content presentation.
---

# PPT Template Generator

Create a polished `.pptx` template deck that another person can reuse without rebuilding its visual language. This skill supplements the available presentation-authoring workflow; follow that workflow for implementation, rendering, inspection, and delivery.

## Interpret the request

Distinguish a reusable template from a one-off presentation. A template demonstrates layouts, hierarchy, components, and editable placeholders. It should not invent a full business story or fill the deck with generic corporate prose.

Use supplied brand files, reference decks, colors, fonts, and layout constraints before any defaults. Treat a supplied presentation as a visual reference only when the user asks to follow its design.

Proceed without questions when reasonable defaults will produce a useful first version. Ask only when a missing decision would materially change the result, such as an unknown mandatory brand font or a required aspect ratio.

## Choose a direction

Translate the request into a compact design brief covering:

- intended audience and recurring use case
- visual tone and image direction
- slide ratio and likely viewing environment
- palette, typography, grid, spacing, and corner treatment
- logo, footer, confidentiality, date, and page-number rules
- expected chart, table, diagram, and image needs

When the user gives little direction, use the neutral business defaults in [references/template-spec.md](references/template-spec.md). Do not present multiple near-identical visual directions unless the user asks for options.

## Build the template system

Create a focused set of representative layouts rather than padding the deck with variations. Read [references/template-spec.md](references/template-spec.md) for the default layout catalog and acceptance criteria, then tailor the set to the user's use case.

Make every layout visibly part of one system:

- consistent title positions, margins, alignment anchors, and spacing rhythm
- a restrained color hierarchy with accessible contrast
- stable typography roles for deck title, slide title, section label, body, caption, and data labels
- consistent chart, table, icon, image-crop, and footer treatment
- deliberate variation in composition so pages do not look cloned

Use native, editable slide objects for text, tables, charts, and requested diagrams. Preserve logos and supplied artwork as original image assets. Use image search or image generation for illustrative imagery when needed; do not create decorative visuals from programmatic shapes.

If the authoring API supports theme or master-layout controls, use them. Otherwise create a normal `.pptx` starter deck whose example slides are safe to duplicate, and state that it is a reusable starter deck rather than claiming unsupported PowerPoint Slide Master behavior. Create `.potx` only when the user explicitly requests it and the available tooling can verify it.

## Use honest placeholder content

Use short, realistic placeholder copy that demonstrates hierarchy without distracting from the template. Label fictional metrics or sample data clearly. Avoid lorem ipsum, unsupported claims, buzzwords, and long instructional paragraphs on the slides.

Include a compact guidance page when it helps users understand fonts, colors, spacing, image treatment, and duplication rules. Keep creation notes out of ordinary content layouts.

## Validate before delivery

Render the completed deck and inspect both the full-deck overview and representative slides at readable size. Fix:

- clipping, overflow, collisions, or off-canvas objects
- inconsistent margins, title anchors, spacing, or footer placement
- weak contrast and illegible text
- stretched images, awkward crops, and low-resolution assets
- chart or table styles that diverge from the visual system
- layouts that are redundant, impractical, or difficult to edit

Confirm that the deck opens, the requested slide ratio and layout coverage are correct, placeholders remain editable, and sample slides can be duplicated without hidden dependencies. Deliver only the final template deck and any preview the user requested.
