---
name: naive-crayon-redraw
description: Transform a user-provided photo or image into a loose, naive 3-year-old-style marker-and-crayon illustration on white paper. Trigger for childlike crayon redraws, ugly-cute doodles, loose marker sketches, naive storybook redraws, and requests to keep the source recognizable but intentionally imperfect. Do not trigger for realistic retouching, anime, 3D, polished vector art, or unrelated illustration styles.
---

# Naive Crayon Redraw

Use this skill to turn a reference image into a deliberately imperfect, charming childlike drawing while preserving the source image's core identity.

## Inputs

Expect:
- One or more user-provided reference images.
- Optional aspect ratio or crop instruction.
- Optional fidelity adjustment such as “more like the original,” “less like the original,” “messier,” or “softer.”
- Optional subject-specific constraints.

If no usable reference image is available, ask the user to provide one before attempting an image edit.

## Default style target

Treat these as the defaults unless the user overrides them:
- Reference similarity: medium — recognizable, but not a faithful copy.
- Childlike clumsiness: high — as if drawn quickly by a 3-year-old.
- Background: clean white paper with subtle paper grain.
- Composition: preserve the source orientation and major framing.
- Mood: playful, cute, warm, airy, innocent, slightly messy.
- Detail level: minimal.

## Workflow

1. Inspect the reference image and identify only the strongest visual anchors:
   - subject type and silhouette;
   - pose, gaze, or gesture;
   - dominant colors and 2–5 identity-defining markings/details;
   - major composition and orientation.

2. Preserve those anchors, but intentionally simplify everything else. The result should feel “a bit similar but not quite,” not like traced line art.

3. Build the drawing language from mixed childlike media:
   - loose marker and crayon;
   - rough black outlines with uneven pressure;
   - occasional thin, wobbly pencil-like lines;
   - scribbly, incomplete coloring with visible strokes;
   - subtle pastel/pencil shading;
   - very light watercolor softness;
   - faint white-paper texture.

4. Intentionally allow:
   - awkward proportions;
   - imperfect perspective;
   - slightly asymmetrical features;
   - simplified anatomy;
   - uneven edges and small drawing mistakes;
   - quick hand-drawn energy.

5. Keep the visual hierarchy simple. Prefer one clear subject and large areas of white space. Do not invent complex scenery unless the user explicitly asks for it.

6. If clothing or accessories are present, retain their recognizable identity but redesign them as simplified picture-book shapes with gentle decorative details. Do not invent clothing for subjects that do not have it.

7. Use the available image generation/editing tool to transform the actual reference image. Do not generate from text alone when a usable reference is present.

8. Preserve the source aspect ratio by default. If the user specifies another ratio, follow it while keeping the subject comfortably framed.

9. After generation, check for style drift. Regenerate or correct if the result becomes too realistic, polished, dimensional, glossy, anatomically accurate, detailed, or cinematic.

## Hard constraints

Avoid:
- photorealism or realistic fur/skin rendering;
- 3D or CGI appearance;
- cinematic lighting;
- glossy or airbrushed surfaces;
- complex cast shadows;
- realistic anatomy;
- hyper-detailed textures;
- polished vector cleanliness;
- dense backgrounds;
- typography or decorative text unless explicitly requested.

The finished image should look quickly drawn by hand on white paper, not professionally rendered to imitate a child.

## Prompt assembly

Use the canonical prompt in `assets/prompt-template.txt` as a base. Replace placeholders with details extracted from the current reference image and user request. Do not copy redundant phrases multiple times.

For subject-specific decisions and style calibration, consult `references/style-spec.md`.

## Fidelity adjustments

When the user says:
- **“更像原图 / more faithful”**: preserve markings, pose, eye direction, color placement, and proportions more carefully; keep the childlike medium unchanged.
- **“更不像 / more naive”**: exaggerate simplification, asymmetry, awkward perspective, and shape reduction; preserve only the subject identity and broad composition.
- **“更乱 / messier”**: increase visible crayon strokes, uneven fill, overlapping lines, and incomplete edges.
- **“更柔和 / softer”**: reduce black-line dominance slightly and increase pale pastel/watercolor softness without becoming polished.

## Output behavior

If image editing is available, execute the image edit rather than only returning a prompt. If image editing is unavailable in the current environment, return the assembled prompt and state that generation was not executed.
