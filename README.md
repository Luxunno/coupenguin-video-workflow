<div align="center">

# 🐧 凑企鹅视频创作 Workflow

**从一句想法到凑企鹅表演，让 Agent 帮你完成制作流程。**

原创小剧场 · 参考视频改编 · 唱跳与梗视频

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg)](LICENSE)
[![Workflow: GMod](https://img.shields.io/badge/Workflow-Garry%27s_Mod-0284c7.svg)](penguin-video-workflow/SKILL.md)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-8b5cf6.svg)](penguin-video-workflow/SKILL.md)

[English](README.en.md) · **简体中文**

[快速开始](#快速开始) · [制作流程](#制作流程) · [文档导航](#文档导航) · [扩展与贡献](#扩展与贡献)

</div>

---

> **开源许可：** 本项目原创的 Skill 指令、文档和代码采用 [MIT License](LICENSE)，允许使用、修改、分发及商业使用，保留版权与许可声明即可。来源：[Luxunno / coupenguin-video-workflow](https://github.com/Luxunno/coupenguin-video-workflow)。语音、模型、音乐和工坊插件等第三方素材沿用原作者的授权条件。

让 Agent 根据你的想法，完成凑企鹅视频的素材准备、场景搭建、动作编排、配音和剪辑。

支持从零创作，也支持把参考视频改编成凑企鹅版本。你负责确认大致脚本、表达偏好和查看效果；Agent 负责把想法落实到 GMod 工程与成片。

> 本项目是以 `SKILL.md` 为入口的制作工作流，包含详细操作文档与常用语音素材。制作时，Agent 根据具体作品调用本地工具、生成脚本并调整工程。

## 可以做什么

- **原创小剧场**：从一句构思展开人物、台词、情节与分镜。
- **参考视频改编**：借用剧情、表演或镜头设计，制作凑企鹅版本。
- **唱歌、跳舞与梗视频**：组合语音、音乐、动作和音效。
- **自动准备资源**：查找本地素材、语音网站、Steam 创意工坊及创作者发布内容。
- **模型与动作适配**：处理骨架匹配、动作速度、过渡、道具接触和镜头。
- **配音与换声**：直接使用语音包，或将导入音频、麦克风录音送入 RVC。
- **持续复用素材**：记录用过的语音、动作、场景和配置，减少重复准备。

## 快速开始

### 1. 安装 Skill

下载本仓库并解压，将其中的 `penguin-video-workflow` 文件夹完整放入所用 Agent 的技能目录，按该工具的方式刷新技能或开启新会话。

保留 `SKILL.md`、`references` 和 `assets` 的相对位置，语音包也应一起安装。

### 2. 准备制作环境

GMod 拍摄需要 Steam、Garry's Mod，以及 Agent 对本地文件和制作工具的操作能力。其余工具根据作品需要准备：

| 工具或资源 | 用途 |
| --- | --- |
| ActMod | 查找、试播和应用现成动作 |
| PAC3 | 角色外观、附件、姿态和动画配置 |
| RVC 与目标声线 | 需要改变音色时使用 |
| 录音工具 | 录制原创台词、拟声词或演唱 |
| Blender | 建模、修改模型、骨架与自定义动作 |
| FFmpeg 或剪辑软件 | 音频处理、画面合成和视频导出 |

已有可用环境可以直接复用。详细步骤见 [环境配置](penguin-video-workflow/references/setup.md)。

### 3. 告诉 Agent 你的想法

```text
使用 $penguin-video-workflow。

我想做一个凑企鹅短视频：企鹅一边咕咕嘎嘎，一边得意地扭两下，
最后突然发现旁边有人看着它。

先和我确认大致脚本。语音优先从随包素材中选，动作从 ActMod 中匹配。
搭好场景和分镜后，让我进入 GMod 看效果。
```

也可以从参考视频开始：

```text
使用 $penguin-video-workflow，把这条参考视频改编成凑企鹅版本。
我想保留它的笑点，但场景和结尾可以重新设计。
先给我一个简短脚本，我们确认后再制作。
```

## 制作流程

1. **确认脚本**  
   Agent 先整理人物、主要情节或表演、声音来源和结尾，与用户确认创作方向。

2. **准备资源**  
   优先查找随包语音、本地素材和已安装的 ActMod；缺少时再搜索、下载和整理补充资源。

3. **搭建与适配**  
   完成人物、场景、道具、动作、表情和分镜，同时处理音频与表演节奏。

4. **集中检查一次样片**  
   在邀请用户查看 GMod 效果之前，Agent 检查一次低成本样片，修正明显穿模、错误动作和镜头问题。

5. **在 GMod 中查看效果**  
   用户查看整段表演或按镜头重播，用自然语言提出修改意见，也可以自行挑选动作或微调姿态。

6. **拍摄、剪辑与交付**  
   根据反馈完成调整，录制或渲染画面，加入声音、字幕与效果，交付成片和可编辑工程。

声音制作可穿插进行：对白驱动的作品可以先录音再编排动作，画面优先的作品也可以后配音。

## 常用语音包

仓库随附 **高松灯爱音语音包**，包含咕咕嘎嘎等常用语音，位置为：

```text
coupenguin-video-workflow/assets/voice-packs/高松灯爱音语音包/
```

Agent 根据脚本搜索实际文件、试听候选并完成裁切、停顿、音量和入点调整。已符合目标声线的片段可以直接使用；需要改变音色时再使用 RVC。

没有合适台词时，可以由用户用麦克风录音，再交给 Agent 整理和换声。

- [语音包使用说明](penguin-video-workflow/references/voice-pack.md)
- [音源、录音与 RVC](penguin-video-workflow/references/audio-edit.md)
- [补充语音来源](https://apps.125ks.cn/qwyy/gxd2/)

## RVC 项目与模型资源

- **RVC 项目地址**：[Retrieval-based Voice Conversion WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI)
- **RVC 下载地址**：[下载页面](https://www.yuque.com/flowercry/hxf0ds)
- **RVC 原作者**：[@花儿不哭](https://space.bilibili.com/5760446)
- **MyGO!!!!! 五人 RVC 模型**：[百度网盘下载](https://pan.baidu.com/s/14qZlzSp1XZFt7fTtSKF2Pw?pwd=gggg)，提取码：`gggg`

## 动作与素材选择

用户可以描述“得意地扭两下”“惊讶后退”“抱着玩偶挥手”等表演，不需要知道动作名称或工坊 ID。

Agent 优先从 ActMod 和已有动画中匹配，再调整速度、循环、衔接与骨架。用户有明确偏好时，也可以直接在 ActMod 中挑选。没有合适动作时，可以组合片段、制作关键帧，或由用户在已搭好的场景中手动微调。

明确匹配的资源直接进入作品预览。只有候选会明显改变笑点、剧情或风格时，才提供少量试听或试播选项。用过的素材记录名称、别名、来源和用途，供后续作品复用。

## 文档导航

| 文档 | 内容 |
| --- | --- |
| [Skill 入口](penguin-video-workflow/SKILL.md) | Agent 的整体工作方式 |
| [环境配置](penguin-video-workflow/references/setup.md) | 新环境安装与工具准备 |
| [素材检索与扩展](penguin-video-workflow/references/discovery.md) | 自动获取资源、语义匹配与本地素材库 |
| [建模与导入](penguin-video-workflow/references/modeling.md) | 角色、道具、材质、骨架和 GMod 导入 |
| [场景、动作与分镜](penguin-video-workflow/references/animation.md) | 表演编排、动作适配与镜头 |
| [Agent 制作与拍摄](penguin-video-workflow/references/automation.md) | 工程组织、脚本控制与拍摄方式 |
| [音源、录音与 RVC](penguin-video-workflow/references/audio-edit.md) | 语音制作、混音与音画同步 |
| [预览与交付](penguin-video-workflow/references/validation.md) | 样片检查、GMod 预览与成片交付 |
| [参考资料](penguin-video-workflow/references/evidence.md) | 教程、实践来源与技术文档 |

## 项目结构

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

## 扩展与贡献

欢迎补充可复用的动作、场景配置、资源来源，以及经过实际制作检验的方法。提交时说明用途、所需工具、接入方式和实际效果，保留第三方素材的来源与作者信息。

新增内容应帮助 Agent 完成具体创作，并保持用户以“确认脚本、查看效果”为主的参与方式。
