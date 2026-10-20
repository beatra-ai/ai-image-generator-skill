# AI Image Generator Skill

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

> 👉 See also [AI Video Generator Skill](https://github.com/beatra-ai/ai-video-generator-skill)

Generate, compose, and edit product images, brand visuals, posters, social graphics, illustrations, and photo variations, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Generate, compose, and edit product images, brand visuals, posters, social graphics, illustrations, and photo variations. |
| **Models** | Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5 |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="A sunlit summer photo of a fictional sage-green ceramic pour-over coffee set, then the same image edited into a snowy winter evening with lamplight while the set and its layout stay in place. AI-generated with Beatra."></p>

*A sunlit summer photo of a fictional sage-green ceramic pour-over coffee set, then the same image edited into a snowy winter evening with lamplight while the set and its layout stay in place. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-image-generation-studio`](skills/ai-image-generation-studio) | [SKILL.md](skills/ai-image-generation-studio/SKILL.md) | 0.2.3 |

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
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-image-generation-studio skill from https://github.com/beatra-ai/ai-image-generator-skill (folder skills/ai-image-generation-studio), then follow its SKILL.md to connect my Beatra account.
```

## Examples

<p align="center"><img src="assets/demo-2.webp" width="800" alt="The generated pour-over set used as a reference for a new composition: a square overhead flat lay on linen with beans, a paper filter and a brass scoop. AI-generated with Beatra."></p>

*The generated pour-over set used as a reference for a new composition: a square overhead flat lay on linen with beans, a paper filter and a brass scoop. AI-generated with Beatra.*

Ask your agent:

```text
Use ./pourover-set.png as the product reference and compose a square overhead flat lay on natural linen for a social post: the dripper, carafe, mug of coffee and sugar bowl with scattered beans, a paper filter and a brass scoop. Keep the set's shapes and glaze colors recognizable.
```

Prompt:

```text
New composition for a square social media post. Image 1 is the product reference: the sage-green ceramic pour-over dripper, the glass carafe, the sage-green mug and the speckled cream sugar bowl. Keep their shapes, glaze colors, speckled texture and proportions recognizable. Arrange them as a top-down overhead flat lay on a textured natural linen tablecloth: the dripper lying beside the carafe, the mug filled with black coffee seen from directly above, the sugar bowl, a small scattered line of whole coffee beans, a folded unbleached paper filter, and a brass coffee scoop. Soft even daylight from the upper left with gentle short shadows, calm balanced spacing between objects with breathing room around the edges, muted sage, cream, linen and warm brown palette, photoreal editorial product photography. No people, no hands, no text, no logos, no labels, no watermarks.
```

## Technical Specifications & Output Limits

As of 2026-10-18. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Text to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): Wan Image 2.7 Pro (up to 4 images per request); GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); PNG; up to 4 images per request; canvas up to 4.2 MP
  - 4.2 MP (2K tier): Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro (up to 4 images per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image to video** — 9 models (Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Text to image 10; Image to image 10; Image editing 6; Image to video 9 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5) (as of 2026-10-18), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

## How it compares

| | Beatra (this skill) | [ZeroLu/Ultimate-AI-Media-Generator-Skill](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill) | [wuyoscar/GPT-Image2-Skill](https://github.com/wuyoscar/GPT-Image2-Skill) | [black-forest-labs/skills](https://github.com/black-forest-labs/skills) |
| --- | --- | --- | --- | --- |
| Account or key needed | A Beatra account; no model provider keys | A CyberBara API key, stored in ~/.config/cyberbara/api_key ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L68-L76)) | Your own OPENAI_API_KEY ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/README.md#L338)) | A BFL API key ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L160-L166)) |
| Models | Text to image 10; Image to image 10; Image editing 6; Image to video 9 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5) | CyberBara image models: Nano Banana 2, Nano Banana 2 Lite, Nano Banana Pro, GPT Image 2, Midjourney v7, Seedream 5 Pro ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L176-L181)) | OpenAI GPT Image 2, GPT Image 2.5 Flare and Sunburst ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/README.md#L154-L160)) | FLUX.2 and FLUX.1 models ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L127-L137)) |
| Before spending | Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate | `quote` CLI command returns `estimated_credits` and `can_afford` before submission ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L105-L115)) | Asks before switching models or adding outputs; confirms the model only when unclear; suggests low-quality drafts first ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/README.md#L162-L164)) | Lists per-model prices, e.g. FLUX.2 [klein] from $0.014/image, [pro] from $0.03/MP; [dev] free for non-commercial use ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L127-L135)) |
| Agents | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw | OpenClaw, Claude Code, Codex, Claude Cowork, Cursor, Antigravity ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L31-L36)) | Claude Code, Codex, OpenClaw, Hermes Agent ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/README.md#L39)) | Coding agents (skills follow the agentskills.io spec); also a Claude Code plugin ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L16-L68)) |
| Install | `npx skills add beatra-ai/ai-image-generator-skill` | `npx skills add ZeroLu/Ultimate-AI-Media-Generator-Skill --all` ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/README.md#L60)) | Claude Code plugin marketplace, or Codex's skill installer ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/README.md#L219-L229)) | `npx skills add black-forest-labs/skills` ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/README.md#L29)) |
| License | MIT-0 | MIT ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/blob/f28e58f2b9814b2056417377c46f34fd35219702/LICENSE)) | MIT ([source](https://github.com/wuyoscar/GPT-Image2-Skill/blob/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f/LICENSE)) | MIT ([source](https://github.com/black-forest-labs/skills/blob/8907d515b0ac270a988ec7a239add81ee13d6cba/LICENSE)) |
| Last updated | Updated with every release (v0.2.3) | 2026-09-08 ([source](https://github.com/ZeroLu/Ultimate-AI-Media-Generator-Skill/commit/f28e58f2b9814b2056417377c46f34fd35219702)) | 2026-09-30 ([source](https://github.com/wuyoscar/GPT-Image2-Skill/commit/9f8aa1a44a4a5c0f5a5d6e45eed564b3e2d5b87f)) | 2026-08-26 ([source](https://github.com/black-forest-labs/skills/commit/8907d515b0ac270a988ec7a239add81ee13d6cba)) |

Facts checked on 2026-10-16. Corrections: open an issue in [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/issues).

## What you get

- **Direction before generation** — Define the message, subject, composition, style, light, color, destination, and must-keeps before creating.
- **Start from the source that matters** — Use a written brief, one to four ordered reference images, or one base image while keeping your chosen starting point clear.
- **Review before another version** — Inspect the generated image, then choose one focused edit, new composition, or new generation.

## Use cases

- **Create product images** — Place a supplied product into a new scene or generate a new product concept, then check shape, color, label, and destination fit.
- **Build ad and brand visuals** — Turn one message, palette, and audience into a campaign image or brand-led visual draft.
- **Make social graphics and posters** — Plan one image around the channel, orientation, room for text, and message.
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

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update ai-image-generation-studio` or `gh skill update ai-image-generation-studio`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai
- Docs — https://docs.beatra.ai
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
