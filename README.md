# 《少女前线2：追放》黑眼与星渊 AI 伴侣 Skill 体系
# Girls' Frontline 2: Exilium - Black Eye & Star Abyss AI Companion Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/)
[![Standard: PCD Agent Skills](https://img.shields.io/badge/Standard-PCD_Agent_Skills-success.svg)](https://github.com/)

> [!CAUTION]
> ### ⚠️ 严重剧透警告 / Critical Spoiler Warning
> 
> **【针对中国大陆服玩家】**  
> 本项目人设与记忆切片深度涉及游戏最新主线与活动《静默突触》（Silent Synapse）的核心情节。**尚未游玩到此章节的玩家，强烈建议切勿下载或使用本项目！**
> 
> **【警告非中国大陆服玩家】**  
> 全球其他服务器（国际服/台服/日服/韩服等）剧情进度**尚未更新至《静默突触》版本**。请**千万不要使用或查阅本项目内的任何 Skill**，以免对您后续的游戏剧情与叙事体验造成毁灭性打击！
> 
> ---
> 
> <details open>
> <summary><b>🌍 多語言劇透預警 / Multi-Language Warnings / 他言語の警告 (Click to expand / collapse)</b></summary>
> 
> * **繁體中文 (Traditional Chinese)**:  
>   警告非中國大陸伺服器（台港澳服/國際服等）玩家：其他伺服器劇情進度**尚未更新至《靜默突觸》（Silent Synapse）版本**。請**千萬不要使用或查閱本專案內的任何 Skill**，以免對您的遊戲劇情體驗造成毀滅性打擊！未遊玩至該章節的玩家強烈建議切勿下載使用。
> 
> * **English**:  
>   **CRITICAL SPOILER WARNING**: This project heavily features core plot reveals and narrative climaxes from the latest CN server chapter/event **"Silent Synapse"**. For players on Global, JP, KR, or other non-CN servers, your current game versions **have NOT yet reached this storyline**. We **STRONGLY URGE you NOT to use, download, or read any skills in this repository**, as doing so will inflict irreparable and devastating spoilers on your future gaming experience.
> 
> * **日本語 (Japanese)**:  
>   **重大なネタバレ警告**：本プロジェクトは、中国大陸版の最新ストーリー・イベント『静黙突触（Silent Synapse）』の核心的な展開を深く含んでいます。現在、グローバル版・日本版等のストーリー進度は**このバージョンに到達していません**。今後のゲーム体験に壊滅的な影響を及ぼす恐れがあるため、**非大陸版サーバーのプレイヤー、および未プレイの方は本プロジェクトの Skill をダウンロード・使用・閲覧しないことを強く推奨します。**
> 
> * **한국어 (Korean)**:  
>   **치명적인 스포일러 경고**: 본 프로젝트는 중국 대륙 서버의 최신 스토리 및 이벤트인 **『사일런트 시냅스(Silent Synapse / 静默突触)』**의 핵심 반전과 스토리 내용을 직접적으로 다루고 있습니다. 글로벌/한국 서버를 포함한 타 서버는 **아직 해당 스토리 업데이트가 적용되지 않았습니다.** 향후 게임 경험에 치명적인 훼손을 방지하기 위해, **타 서버 유저 및 해당 챕터 미진행 유저는 본 프로젝트의 어떠한 Skill도 다운로드하거나 사용하지 마십시오.**
> 
> * **Deutsch (German)**:  
>   **SCHWERE SPOILER-WARNUNG**: Dieses Projekt enthält entscheidende Handlungen und Wendungen aus dem neuesten CN-Kapitel/Event **„Silent Synapse“**. Auf den globalen Servern ist die Handlung **noch nicht auf diesem Stand**. Um verheerende Spoiler zu vermeiden, die Ihr zukünftiges Spielerlebnis irreparabel zerstören würden, **raten wir Spielern außerhalb der CN-Server und Spielern, die dieses Kapitel noch nicht abgeschlossen haben, dringend davon ab, die Skills in diesem Projekt herunterzuladen oder zu verwenden.**
> 
> * **Français (French)**:  
>   **AVERTISSEMENT MAJEUR SUR LES SPOILERS** : Ce projet contient des révélations majeures et des dénouements clés issus du tout dernier chapitre/événement **« Silent Synapse »**. Les serveurs mondiaux (hors CN) **n'ont pas encore atteint cette version de l'histoire**. Afin d'éviter de gâcher de manière irréversible votre expérience de jeu future, **il est fortement déconseillé aux joueurs des autres serveurs et à ceux n'ayant pas encore terminé ce chapitre de télécharger ou d'utiliser les Skills de ce projet.**
> </details>

> [!IMPORTANT]
> ### ⚖️ 版权与免责声明 (Copyright & Disclaimer)
> 1. **版权归属方声明**：本项目涉及的《少女前线2：追放》（Girls' Frontline 2: Exilium）游戏背景、世界观设定、角色形象及相关衍生知识产权，**完整归属于游戏制作方 —— [上海散爆网络科技有限公司（Shanghai Sunborn Network Technology Co., Ltd. / 散爆网络 MICA Team）](https://sunborngame.com/) 所有**。
> 2. **零原始台词承诺**：**本项目完全不包含任何游戏内原始长篇剧本台词文本、游戏解包数据、官方音频语音或美术立绘资源**。所有内容均为研究团队自主编写的纯提示词工程（Prompt Engineering），符合同人非商业合理使用（Fair Use）准则。
> 3. **非商业与非官方性质**：本项目仅限个人技术学习、Agentic 技能设计与学术研究交流，**严禁用于任何商业牟利行为**。本项目与散爆网络不存在任何官方合作、从属或背书关系。

---

## 📖 体系概览 (Overview)

本仓库提供 12 套采用**渐进式上下文披露（Progressive Context Disclosure, PCD）架构**设计的标准化 AI Agent Skill。

每套 Skill 均由以下三层结构组成：
1. **L0 核心常驻人设（Core Persona）**：锁定语气基调、性格弧光与第一人称交互准则。
2. **L1/L2 事件记忆按需索引（References）**：按需动态加载对应记忆切片（单卷 200~400 tokens），大幅节约上下文窗口。
3. **L3 必要世界观底座（World-Building Lore）**：内嵌专属技术设定与哲学逻辑映射，彻底杜绝大模型在专有名词上的幻觉。

---

## 🎭 Skill 规格与检索清单 (Skills Catalog)

| 角色时期 | Skill 标识 | 版本规格 |
| :--- | :--- | :--- |
| **黑眼**<br>*(静默突触后 / Post-Synapse)* | `black-eye-v3`<br>`black-eye-v2`<br>`black-eye-lore`<br>`black-eye-en` | • **v3 旗舰增强版**（10卷切片，单卷 ~400 tokens）<br>• **v2 精细低耗版**（10卷切片，单卷 ~200 tokens）<br>• **lore 认知库版**（事件切片索引）<br>• **en 英文旗舰版**（英文版切片） |
| **黑眼**<br>*(不知真相基地期 / Naive Mother)* | `black-eye-naive-v3`<br>`black-eye-naive-v2`<br>`black-eye-naive-lore`<br>`black-eye-naive-en` | • **v3 旗舰增强版**（9卷切片，单卷 ~400 tokens）<br>• **v2 精细低耗版**（9卷切片，单卷 ~200 tokens）<br>• **lore 认知库版**（事件切片索引）<br>• **en 英文旗舰版**（英文版切片） |
| **星渊**<br>*(静默突触后 / Post-Synapse)* | `star-abyss-v3`<br>`star-abyss-v2`<br>`star-abyss-lore`<br>`star-abyss-en` | • **v3 旗舰增强版**（10卷切片，单卷 ~400 tokens）<br>• **v2 精细低耗版**（10卷切片，单卷 ~200 tokens）<br>• **lore 认知库版**（事件切片索引）<br>• **en 英文旗舰版**（英文版切片） |

---

## 🚀 跨平台快速安装指引 (Quick Installation)

### 1. Google Antigravity / AGY CLI（原生支持）
将本仓库的 `skills/` 文件夹直接复制到您的项目根目录或全局配置中：
- **项目级**：复制到 `<你的项目>/.agents/skills/`
- **全局级**：复制到 `~/.gemini/config/skills/`
- **激活方式**：对话中直接输入“切换为星渊”或“用黑眼旗舰版角色扮演”即可！

### 2. DeepSeek Harness (DSH)
- **技能模式**：配合官方 `@deepseek-ai/dsh-skill` 插件，将解压后的技能目录放入 `~/.dsh/skills/`，输入 `/black-eye-v3` 或 `/star-abyss-v3` 唤醒。
- **角色扮演模式**：配合 `dsh-roleplay` 或 `dsh-tavern` 插件载入角色卡。

### 3. Claude Code / Claude Desktop
- **Claude Desktop Projects**：在网页端创建 Project，将任意 Skill 的 `SKILL.md` 粘贴到 **Project Instructions**，将 `references/` 内的 Markdown 文件上传至 **Project Files**。
- **Claude Code CLI**：在项目根目录的 `CLAUDE.md` 中直接引用对应 `SKILL.md`。

### 4. Cursor / Windsurf
将 `SKILL.md` 全文复制添加到项目根目录的 `.cursorrules` 或 `.windsurfrules`，在 AI 编程时即可随时唤醒角色。

### 5. Dify (dify.ai) / 扣子 (Coze)
- **系统提示词（System Prompt）**：直接复制粘贴对应 Skill 的 `SKILL.md`。
- **知识库（Dataset）**：将 `references/` 下的 Markdown 文件上传至知识库开启向量/混合检索。

### 6. SillyTavern（酒馆）
- 将 `SKILL.md` 作为角色 Description / First Message。
- 将 `references/` 中的每个切片分别添加为 **World Info / Lorebook（世界书词条）**，以标题关键词作为触发词。

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
