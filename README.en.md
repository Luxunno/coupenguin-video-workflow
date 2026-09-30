<div align="center">

# 🐧 CouPenguin Video Workflow

**Turn an idea into a penguin performance—with an AI agent handling the production workflow.**

Original sketches · Reference remixes · Dance & music clips

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg)](LICENSE)
[![Workflow: GMod](https://img.shields.io/badge/Workflow-Garry%27s_Mod-0284c7.svg)](penguin-video-workflow/SKILL.md)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-8b5cf6.svg)](penguin-video-workflow/SKILL.md)

**English** · [简体中文](README.md)

[Quick start](#quick-start) · [Workflow](#the-workflow) · [Documentation](#documentation) · [Contributing](#contributing)

</div>

---

A reusable agent skill for making **凑企鹅 (CouPenguin)** videos in Garry's Mod. Start with a new idea or adapt a reference video, then work with your agent on the script, resources, characters, animation, voice, cameras, and edit.

**You describe the story and review the performance. The agent handles the production steps.**

> This repository provides a `SKILL.md` workflow, supporting guides, and a location for reusable voice assets. The agent uses your local tools and creates project-specific scripts as needed. The workflow requires a configured production environment; it is not a standalone video renderer. The detailed production guides are currently in Chinese.

## What you can create

| Your idea | What the workflow helps arrange |
| :--- | :--- |
| “A penguin gets caught doing a smug dance.” | Script, characters, animation, reaction timing, and shots |
| “Remake this clip with CouPenguin.” | Reference analysis, character replacement, and a new scene or ending |
| “Make a singing or dancing meme.” | Voice clips, music, movements, sound effects, and editing |
| “Use this voice—or let me record the lines.” | Direct audio use, microphone recording, optional RVC, and synchronization |

The agent searches for resources by meaning, adapts them to the scene, and keeps a lightweight local library for future projects. You do not need to know animation names or Workshop IDs.

## Quick start

### 1. Install the skill

Download this repository and copy the entire **`penguin-video-workflow/`** folder into your agent's skills directory. Refresh skills or start a new session as required by your agent.

Keep `SKILL.md`, `references/`, and `assets/` together so relative paths continue to work.

### 2. Prepare your tools

For GMod production, you need **Steam, Garry's Mod**, and an agent that can operate the local files and tools. Add the following as your project needs them:

| Tool | Purpose |
| :--- | :--- |
| ActMod addon | Browse, preview, and apply existing animations |
| PAC3 | Character appearance, attachments, poses, and animation setup |
| RVC + a voice model | Voice conversion when the source needs a different timbre |
| Microphone / recording tool | Original dialogue, vocal effects, or singing |
| Blender | Modeling, rigging, props, and custom animation |
| FFmpeg / video editor | Audio processing, editing, and export |

Reuse an existing setup where possible. Follow the [environment guide](penguin-video-workflow/references/setup.md) for more detail.

### 3. Describe your video

```text
Use $penguin-video-workflow.

Make a short CouPenguin video:
The penguin says “咕咕嘎嘎,” does two smug little twists,
then suddenly notices someone watching.

Confirm the rough script with me first.
Prefer the local voice pack and match suitable ActMod animations.
Once the scene and shots are ready, let me review the performance in GMod.
```

<details>
<summary><b>Starting from a reference video?</b></summary>

```text
Use $penguin-video-workflow to adapt this reference into a CouPenguin video.

Keep the main joke, but feel free to redesign the setting and ending.
Give me a short script to confirm before production.
```

</details>

## The workflow

**Idea → Script → Resources → Scene & performance → Preview → Edit & export**

1. **Confirm the rough script.** Agree on the characters, story or performance, dialogue, and ending.
2. **Find the resources.** Search local assets and the voice pack first; look for missing resources on voice sites, Steam Workshop, and creator pages.
3. **Build and adapt.** Arrange the scene, props, animation, cameras, and audio timing. Adjust skeleton matching, speed, transitions, and prop contact as needed.
4. **Check one consolidated sample.** Before the GMod review, inspect a low-cost sample and fix obvious animation, clipping, or camera problems.
5. **Review in GMod.** Watch the performance, replay individual shots, and ask for changes in ordinary language. You can also choose ActMod actions or tweak poses yourself.
6. **Record, edit, and deliver.** Finish the audio, footage, subtitles, and effects; deliver the video and editable project.

Dialogue-heavy projects can start with audio. Visual-first projects can be voiced later.

## Voices & reusable assets

The local **高松灯爱音语音包** is available to the workflow, including common “咕咕嘎嘎” clips:

```text
penguin-video-workflow/assets/voice-packs/高松灯爱音语音包/
```

The agent checks the files actually present, previews suitable clips, and adjusts cuts, pauses, volume, and placement. Clips that already have the desired voice can be used directly. **RVC is optional.**

For original lines, import existing audio or record with a microphone, then apply voice conversion when needed.

- [Voice pack guide](penguin-video-workflow/references/voice-pack.md)
- [Audio, recording & RVC](penguin-video-workflow/references/audio-edit.md)
- [Additional voice source](https://apps.125ks.cn/qwyy/gxd2/)

## Animation & resource discovery

Describe a performance such as **“two smug twists,” “step back in surprise,”** or **“wave while holding a plush.”** The agent matches existing resources and handles adaptation.

When an exact asset is unavailable, the workflow supports combining animation clips, making keyframes, adapting props, or arranging original recordings. Alternatives that change the intended joke or story should be discussed with you.

Clearly matching assets go straight into the preview. A small set of playable candidates is useful when the choice would materially change the style or joke.

Used resources are recorded with names, aliases, sources, and uses—for example, **smug / celebration / hip sway** or **surprise / scream / 咕咕嘎嘎**. Future projects reuse them before searching again.

## Documentation

| Guide | Contents |
| :--- | :--- |
| [Skill entry point](penguin-video-workflow/SKILL.md) | Agent workflow and production decisions |
| [Environment setup](penguin-video-workflow/references/setup.md) | Tools and new-machine setup |
| [Resource discovery](penguin-video-workflow/references/discovery.md) | Semantic matching, downloads, and a local asset library |
| [Modeling & import](penguin-video-workflow/references/modeling.md) | Characters, props, materials, rigs, and GMod import |
| [Scene, animation & shots](penguin-video-workflow/references/animation.md) | Performance, animation adaptation, and cameras |
| [Agent production & capture](penguin-video-workflow/references/automation.md) | Project organization, scripts, and recording |
| [Audio & synchronization](penguin-video-workflow/references/audio-edit.md) | Recording, RVC, mixing, and audio/video alignment |
| [Preview & delivery](penguin-video-workflow/references/validation.md) | Sample check, GMod review, and final delivery |
| [References](penguin-video-workflow/references/evidence.md) | Tutorials, practical sources, and technical documentation |

## Repository layout

```text
.
├── README.md                  # 简体中文
├── README.en.md               # English
├── LICENSE
└── penguin-video-workflow/
    ├── SKILL.md
    ├── references/
    └── assets/
        └── voice-packs/
            └── 高松灯爱音语音包/
```

## Contributing

Contributions are welcome: animation recipes, scene setups, resource sources, translations, and methods tested in real productions.

Explain what an addition does, which tools it needs, how to use it, and what you tested. Include the source and creator information for third-party resources. Keep the workflow centered on **confirming the script and reviewing the result**, with the agent handling routine production work.

## License & attribution

The project's original skill instructions, documentation, and code are released under the **[MIT License](LICENSE)**. You may use, modify, redistribute, and use them commercially, provided you retain the copyright and license notice in copies or substantial portions.

Source: **[Luxunno / coupenguin-video-workflow](https://github.com/Luxunno/coupenguin-video-workflow)**.

Voice clips, character models, music, Workshop addons, and other third-party assets retain their original creators' licenses and usage terms. Their inclusion or mention does not relicense them under MIT.

---

<div align="center">

**Describe the idea. Review the performance. Keep creating.** 🐧

</div>
