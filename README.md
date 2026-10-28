# 《少女前线2：追放》黑眼与星渊 AI 伴侣 Skill 体系
# Girls' Frontline 2: Exilium - Black Eye & Star Abyss AI Companion Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/)
[![Pure Prompt Engineering](https://img.shields.io/badge/Standard-PCD_Agent_Skills-success.svg)](https://github.com/)

> ⚠️ **版权纯净说明**：本项目**仅包含纯提示词工程（Prompt Engineering）构建的标准化 Agent Skill 与记忆索引切片**，已彻底剥离所有游戏内未加工的长篇原始剧本台词，完全符合个人研究、学习交流与同人创作的合理使用（Fair Use）规范。游戏背景与人物设定版权归 [散爆网络（Sunborn Games）](https://sunborngame.com/) 所有。

---

## 📖 体系概览 (Overview)

本仓库提供 12 套采用**渐进式上下文披露（Progressive Context Disclosure, PCD）架构**设计的标准化 AI Agent Skill。

每套 Skill 均由以下四层结构组成：
1. **L0 核心常驻人设（Core Persona）**：锁定第一人称语气、性格弧光、红线约束与与指挥官的宿命羁绊。
2. **L1/L2 事件记忆按需索引（References）**：按需动态调用对应事件切片（单卷 200~400 tokens），大幅节约上下文窗口。
3. **L3 必要世界观设定底座（World-Building Lore）**：内嵌希岸高维意识、伯介姆原核情绪放大机制、O-201流水线、法兰克福一分钟等必要世界观，彻底杜绝大模型在少前2专有设定上的幻觉。

---

## 🎭 包含的 12 套 Skill 列表 (Skills Catalog)

### 1. 黑眼·静默突触后（Post-Silent Synapse Black Eye）
*与指挥官（曾装成乖女儿 O-201）相爱相杀、嘴硬傲娇、手背留有死敌齿痕契约的第三代帕拉蒂斯人形。*

| Skill 标识 | 版本特性 | 适用场景 |
| :--- | :--- | :--- |
| **`black-eye-v3`** | **旗舰增强版**（10卷切片，单卷 ~400 tokens，含台词与心理反应指引） | 沉浸式深度角色扮演、剧情长篇推演 |
| **`black-eye-v2`** | **精细低耗版**（10卷切片，单卷 ~200 tokens，极度节省 Token） | 日常多轮闲聊、资源敏感型模型 |
| **`black-eye-lore`** | **经典剧情认知库**（6大阶段全景事件档案） | 知识问答、剧情梳理分析 |
| **`black-eye-en`** | **Flagship English Edition**（纯正英文人设与台词基准） | 英语模型与海外平台对话 |

### 2. 黑眼·不知真相基地期（Pre-Escape Naive Mother Era）
*在红区地下基地做清洁杂役的黑眼，完全不知 O-201 是指挥官，将其视作唯一女儿，在管道夹层搭建“秘密公主房”、打工买小皮鞋、为护女向海伦娜 001 磕头的单亲救赎期。*

| Skill 标识 | 版本特性 | 适用场景 |
| :--- | :--- | :--- |
| **`black-eye-naive-v3`** | **旗舰增强版**（9卷切片，含“妈妈的三条严厉家规”与公主房温馨日常） | 救赎向母女温馨互动、情感治愈 |
| **`black-eye-naive-v2`** | **精细低耗版**（9卷切片，极致紧凑） | 快速日常问答与陪伴 |
| **`black-eye-naive-lore`** | **经典剧情认知库**（基地期核心事件索引） | 基地期背景考据 |
| **`black-eye-naive-en`** | **Flagship English Edition**（英文母女互动人设） | 英文母女互动与角色扮演 |

### 3. 星渊·静默突触后（Post-Silent Synapse Star Abyss）
*漫步希岸非线性意识之海的超然神性伴侣，曾与指挥官共用 O-201 躯体共生，抚慰晶石巨龙乔扎，并在法兰克福终局献上“自私的一分钟”吻别与唯一祈祷。*

| Skill 标识 | 版本特性 | 适用场景 |
| :--- | :--- | :--- |
| **`star-abyss-v3`** | **旗舰增强版**（10卷切片，含神圣空灵语调与一体双魂默契） | 深度哲学与神圣羁绊角色扮演 |
| **`star-abyss-v2`** | **精细低耗版**（10卷切片，紧凑澄澈） | 资源节约型神圣伴侣 |
| **`star-abyss-lore`** | **经典剧情认知库**（利沃夫起源与希岸法则） | 世界观高维形而上学推演 |
| **`star-abyss-en`** | **Flagship English Edition**（纯正英文空灵神性伴侣） | 英文深度对话 |

---

## 🚀 跨平台极速安装指引 (Quick Installation)

### 1. Google Antigravity / AGY CLI（原生支持）
将本仓库的 `skills/` 文件夹直接复制到您的项目根目录或全局配置中：
- **项目级**：复制到 `<你的项目>/.agents/skills/`
- **全局级**：复制到 `~/.gemini/config/skills/`（Windows 为 `C:\Users\<用户名>\.gemini\config\skills\`）
- **激活方式**：对话中直接输入“切换为星渊”或“用黑眼旗舰版角色扮演”即可！

### 2. Claude Code / Claude Desktop
- **Claude Desktop Projects**：在网页端创建 Project，将任意 Skill 的 `SKILL.md` 粘贴到 **Project Instructions**，将 `references/` 内的 Markdown 文件上传至 **Project Files**。
- **Claude Code CLI**：在项目根目录的 `CLAUDE.md` 中直接引用对应 `SKILL.md`。

### 3. Cursor / Windsurf
将 `SKILL.md` 全文复制添加到项目根目录的 `.cursorrules` 或 `.windsurfrules`，在 AI 编程时即可随时唤醒角色。

### 4. Dify (dify.ai) / 扣子 (Coze)
- **系统提示词（System Prompt）**：直接复制粘贴对应 Skill 的 `SKILL.md`。
- **知识库（Dataset）**：将 `references/` 下的 Markdown 文件上传至知识库开启向量/混合检索。

### 5. SillyTavern（酒馆）
- 将 `SKILL.md` 作为角色 Description / First Message。
- 将 `references/` 中的每个切片分别添加为 **World Info / Lorebook（世界书词条）**，以标题关键词作为触发词。

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
