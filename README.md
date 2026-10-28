# 《少女前线2：追放》黑眼与星渊 AI 伴侣 Skill 体系
# Girls' Frontline 2: Exilium - Black Eye & Star Abyss AI Companion Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/)
[![Standard: PCD Agent Skills](https://img.shields.io/badge/Standard-PCD_Agent_Skills-success.svg)](https://github.com/)

> [!WARNING]
> ### ⚠️ 剧透警告 (Spoiler Warning)
> 本项目中的角色人设、心理状态机及记忆切片涉及《少女前线2：追放》主线剧情及重要活动故事线。
> 为保证最佳的原作游戏剧情与叙事体验，**建议在体验原作相关剧情后再行查阅或使用本 Skill**。

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

| 角色形态 | Skill 标识 | 版本规格 | 适用场景 |
| :--- | :--- | :--- | :--- |
| **黑眼·傲娇死敌态**<br>*(Post-Synapse)* | `black-eye-v3`<br>`black-eye-v2`<br>`black-eye-lore`<br>`black-eye-en` | • **v3 旗舰增强版**（10卷切片，含台词口癖与心理反应）<br>• **v2 精细低耗版**（10卷切片，单卷 ~200 tokens）<br>• **lore 认知库版**（全景事件档案索引）<br>• **en 英文旗舰版**（纯正英文人设基准） | 深度沉浸扮演<br>日常多轮闲聊<br>知识问答分析<br>海外平台对话 |
| **黑眼·单亲守护态**<br>*(Naive Mother)* | `black-eye-naive-v3`<br>`black-eye-naive-v2`<br>`black-eye-naive-lore`<br>`black-eye-naive-en` | • **v3 旗舰增强版**（9卷切片，含家规指引与温馨日常）<br>• **v2 精细低耗版**（9卷切片，极致紧凑省流）<br>• **lore 认知库版**（历史事件索引）<br>• **en 英文旗舰版**（英文守护母女人设） | 救赎治愈互动<br>日常陪伴交流<br>背景设定考据<br>英文角色扮演 |
| **星渊·神性伴侣态**<br>*(Star Abyss)* | `star-abyss-v3`<br>`star-abyss-v2`<br>`star-abyss-lore`<br>`star-abyss-en` | • **v3 旗舰增强版**（10卷切片，空灵神性与深层羁绊）<br>• **v2 精细低耗版**（10卷切片，紧凑澄澈）<br>• **lore 认知库版**（高维世界观考据）<br>• **en 英文旗舰版**（纯正英文神性伴侣） | 深度哲学扮演<br>资源节约伴侣<br>世界观推演<br>英文深度交流 |

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
