# AI Image Generator Skill

English | [简体中文](./README.zh-CN.md)

Generate, compose, and edit product images, brand visuals, posters, social graphics, illustrations, and photo variations, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Generate, compose, and edit product images, brand visuals, posters, social graphics, illustrations, and photo variations. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-image-generation-studio`](skills/ai-image-generation-studio) | [SKILL.md](skills/ai-image-generation-studio/SKILL.md) | 0.1.3 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-image-generation-studio). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/ai-image-generator-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/ai-image-generator-skill ai-image-generation-studio
```

Or clone this repository and copy `skills/ai-image-generation-studio` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-image-generation-studio skill from https://github.com/beatra-ai/ai-image-generator-skill (folder skills/ai-image-generation-studio), then follow its SKILL.md to connect my Beatra account.
```

## What you get

- **Direction before generation** — Define the message, subject, composition, style, light, color, destination, and must-keeps before creating.
- **Start from the source that matters** — Use a written brief, one to four ordered reference images, or one base image while keeping your chosen starting point clear.
- **Review before another version** — Inspect the generated image, then choose one focused edit, new composition, or new generation.

## Use cases

- **Create product images** — Place a supplied product into a new scene or generate a new product concept, then check shape, color, label, and destination fit.
- **Build ad and brand visuals** — Turn one message, palette, and audience into a campaign image or brand-led visual draft.
- **Make social graphics and posters** — Plan one image around the chosen channel, orientation, safe space, and message.
- **Develop illustrations and concepts** — Explore a named visual style for an illustration, cover, scene, or concept image.
- **Change a photo or background** — Use an existing image as the base and focus the requested change on an object, region, background, or overall treatment, then inspect the whole result.
- **Compose from reference images** — Use ordered product, subject, style, or scene references to guide a new image, then check what carried through.

## FAQ

### What can AI Image Generation Studio make?

It can create product images, ad creative, brand visuals, posters, social graphics, illustrations, concept art, photo variations, and background changes from text, references, or an existing base image.

### Can it use my own photos or product images?

Yes. One to four supplied images can guide a new composition, or the first supplied image can remain the base for an edit. Generated details still need review.

### Can it change only part of an image?

Yes. A focused edit targets a defined area of an existing base image, then reviews the whole result for subject, composition, text, and destination fit.

### Which image models does it use?

It matches the image goal, reference materials, canvas, output count, and creative controls with current models, and keeps a named model when it fits those inputs.

### Can it keep a series consistent?

It reuses the selected direction, wording, reference images, subject cues, style, logo placement, and text plan across the series, then reviews each result for visual consistency.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.
