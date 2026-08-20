# Style Specification

## Core visual identity

The target is a naive mixed-media children's drawing, not a polished illustration pretending to be childish.

Priority order:
1. Childlike spontaneity.
2. Recognizable source identity.
3. White-paper minimalism.
4. Mixed crayon/marker/pencil/pastel/watercolor texture.
5. Cute, warm storybook mood.

## Line language

Use:
- bold black marker/crayon outlines in selected contours;
- uneven pressure and imperfect joins;
- thin shaky lines for secondary details;
- occasional doubled or overshot lines;
- simple shapes rather than accurate contour tracing.

Avoid:
- smooth Bézier-like contours;
- clean vector geometry;
- uniform line weight;
- precise perspective construction.

## Color language

Use:
- source-derived dominant colors;
- slightly muted or softened saturation where useful;
- scribbled crayon fill with visible paper gaps;
- uneven coverage;
- small color spill outside outlines;
- subtle pastel and watercolor softness.

Avoid:
- perfect gradients;
- glossy highlights;
- rich cinematic color grading;
- realistic material rendering.

## Shape and anatomy

Prefer:
- circles, ovals, beans, triangles, boxes, and simple curved blobs;
- oversized or undersized features;
- asymmetry;
- shortened limbs or simplified paws/hands;
- nontechnical perspective.

The image must remain legible enough to identify the subject, but it should not look traced.

## Background

Default to white paper only. A faint paper grain is desirable. Keep large blank regions.

Only add simple background marks when the user explicitly requests a setting. Even then, reduce the setting to a few naive lines or shapes.

## Similarity calibration

Default: 60–70% conceptual recognition, 30–40% naive reinterpretation.

Preserve:
- overall pose;
- facing direction;
- broad silhouette;
- major color blocking;
- 2–5 identifying details.

Simplify or distort:
- exact anatomy;
- small textures;
- precise perspective;
- fine edges;
- secondary objects.

## Quality-control failure modes

Too polished:
- reduce precision;
- add broken/scribbly edges;
- simplify shapes;
- expose paper gaps.

Too realistic:
- flatten light;
- remove realistic shadows and material detail;
- enlarge/simplify features;
- reduce texture fidelity.

Too generic / lost identity:
- restore 2–5 source-specific visual anchors;
- correct dominant color placement;
- restore pose/gaze direction.

Too messy / unreadable:
- simplify the number of marks;
- strengthen the main silhouette;
- keep the background empty.
