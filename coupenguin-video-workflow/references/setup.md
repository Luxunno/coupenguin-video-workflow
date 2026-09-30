# 环境配置

## 安装这个 Skill

将整个 penguin-video-workflow 文件夹放到当前 Agent 的 skills 目录，保持 SKILL.md 与 references 的相对位置。Codex 通常使用用户目录下的 .codex/skills；自定义过 CODEX_HOME 时使用对应目录。刷新技能列表或开启新会话后，可以这样调用：

“使用 penguin-video-workflow，帮我从零制作凑企鹅小剧场，先准备场景和动作，再让我在 GMod 里看效果。”

复制 Skill 时一并保留 assets/voice-packs/ 下的语音素材。游戏、模型、工具和 RVC 声线按实际创作需要准备；语音音频与 RVC 声线权重是不同资源。

## 新机器需要什么

| 工具 | 用途 | 准备方式 |
|---|---|---|
| Steam 和 Garry's Mod | 场景、角色、动作和拍摄 | 安装游戏并登录 Steam，进入一次单人 Sandbox |
| 角色、地图及相关工坊内容 | 搭建作品 | 从工坊下载所需素材及依赖 |
| PAC3 | 角色外观、附件、骨骼姿态与动画配置 | 需要这类能力时安装 |
| ActMod | Agent 按描述匹配动作；用户也可自行挑选 | 检查是否已安装；已有就直接使用，缺少时安装插件及所需依赖 |
| RVC 与目标声线 | 音色转换 | 安装兼容版本，准备模型权重和配套索引 |
| 录音工具 | 用户麦克风录音 | 系统录音机、Audacity、剪辑软件等任选 |
| FFmpeg 或剪辑软件 | 提音、混音、拼接、导出 | 按 Agent 的控制能力与用户习惯选择 |
| Blender | 新建、修改模型和动作 | 需要建模时安装，不作为每次创作的必需项 |
| Source 导出和编译工具 | 将 Blender 模型做成 GMod 模型 | 需要正式导入可动模型时安装 |

优先使用已有可运行的软件。版本选择参考所用插件的兼容说明；RVC 整合包可保留自带 Python，不必为它升级全局环境。

官方入口：
- [Garry's Mod](https://store.steampowered.com/app/4000/Garrys_Mod/)
- [Blender](https://www.blender.org/download/)
- [PAC3](https://github.com/CapsAdmin/pac3)
- [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI)
- [FFmpeg](https://ffmpeg.org/download.html)
- [Blender Source Tools](https://github.com/Artfunkel/BlenderSourceTools)
- [Audacity](https://www.audacityteam.org/)

## 找到实际目录

Agent 先查 Steam 库与 GMod 安装位置，再找 Blender、RVC 和输出目录。不沿用旧机器的 E 盘、F 盘路径。Windows 原生程序使用 Windows 路径，WSL 工具使用对应 /mnt 路径。

简单记录项目会用到的工具位置即可。素材、工程、音频和成片放在独立项目文件夹，名称由当前作品决定；不要求生成机器清单或大量报告。

## 安装工坊素材

1. 搜索角色、地图或插件，阅读原条目的依赖说明。
2. 通过 Steam 订阅下载；Agent 也可在 GMod 内用 steamworks.DownloadUGC 获取资源。
3. 需要检查内部模型、材料或动作注册时，用游戏附带的 gmad 解包到项目目录。
4. 添加脚本型插件后，按实际情况重载地图或重启游戏，使插件初始化。
5. 在游戏里打开模型或地图，能正常显示后继续搭建。

下载接口：[DownloadUGC](https://wiki.facepunch.com/gmod/steamworks.DownloadUGC)；挂载接口：[MountGMA](https://wiki.facepunch.com/gmod/game.MountGMA)。挂载资源与执行插件脚本是两件事，找不到功能时先检查是否已重新加载。

Funkis、Simple Holster、Enhanced PlayerModel Selector 等可以按题材选用，教程里出现不代表全部必装。第三方地图缺贴图时查所需游戏内容和依赖，不必因此重装整个环境。

## 配置 RVC

选择可信发行版，按其说明安装。将目标声线权重与对应索引放到该版本要求的位置，启动界面或调用其推理入口。用当前作品的一小段音频确认能换声即可，参数与声音调整详见 audio-edit.md。

无 GPU 时可根据工具支持使用 CPU；有 GPU 则选兼容后端。转换速度慢时再考虑优化，不先把硬件升级作为创作前提。

## 配置 Agent 的操作入口

让 Agent 能写项目文件、调用本地工具、控制游戏或加载项目 addon。优先脚本批量调整；个别安装或登录步骤需要用户完成时，说明具体操作。

项目 addon 可放在 garrysmod/addons/<项目名>，运行数据放在 garrysmod/data/<项目名>。先进入单人场景，再加载制作内容，避免影响其他游戏会话。
