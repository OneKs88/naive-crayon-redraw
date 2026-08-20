# naive-crayon-redraw

A reusable OpenAI Agent Skill for transforming reference images into intentionally imperfect, childlike marker-and-crayon drawings on white paper.

## Package structure

```text
naive-crayon-redraw/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── prompt-template.txt
└── references/
    └── style-spec.md
```

## Codex installation

### Repository-scoped
Copy the whole folder to:

```text
<repo-root>/.agents/skills/naive-crayon-redraw/
```

This makes the skill available to Codex for that repository.

### User-scoped
Copy the whole folder to:

```text
~/.agents/skills/naive-crayon-redraw/
```

This makes it available across repositories for the current user.

Codex normally detects skill changes automatically. If it does not appear, restart Codex.

## Invocation

In Codex CLI or IDE:

```text
$naive-crayon-redraw 把这张参考图按默认风格重绘，保持原图比例。
```

In ChatGPT surfaces that support standalone skills, select the skill with `@` and attach the reference image.

## Suggested batch-work prompts

```text
$naive-crayon-redraw 批量处理这些照片。统一使用默认白纸背景、3岁儿童蜡笔感；每张保留主体姿势和主要颜色，但不要画得过于相似。
```

```text
$naive-crayon-redraw 这张更像原图一点，重点保留眼睛方向、花纹位置和身体姿势，但线条继续保持幼稚、潦草。
```

```text
$naive-crayon-redraw 这张再幼稚30%，减少细节，让透视和比例更笨拙，背景保持纯白纸。
```
