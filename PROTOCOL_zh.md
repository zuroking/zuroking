# PROTOCOL.md: 技能驱动型开发生态系统 (Skill-Driven Development Ecosystem)

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · **中文** · [Deutsch](PROTOCOL_de.md) · [Español](PROTOCOL_es.md) · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · [Português](PROTOCOL_pt.md)

## 1. 概念与哲学

本文档描述了适用于混合智能体生态系统的组合内开发方法。该协议涵盖了整个产品生命周期——从初始架构草案到最终展示构件的生成。

核心原则：**架构决策必须是明确的、可复现的且有理有据的。** 我们已从单纯的编写代码转变为**技能驱动型开发 (Skill-Driven Development)**，其中常规操作、设计、测试和分析均委派给特定智能体的专业技能。

---

## 2. 角色与技能分配

参与该过程的有三个主要实体以及统一智能体环境。他们的角色严格区分，互不重叠。

### 2.1. 开发者 (人类)
产品所有者。对每个架构决策点拥有最终决定权，批准范围，设定开发方向，并接受智能体的交付成果。

### 2.2. OpenCode (自主执行者)
执行智能体，在终端中操作，上下文窗口高达 1M token。负责编写代码、构建界面以及生成文档和媒体构件。
拥有以下技能库：
*   **工程与代码：** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`。
*   **设计与前端：** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`。
*   **文档与办公：** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`。
*   **沟通与培训：** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`。

### 2.3. Claude Desktop (架构师与分析师)
充当数据中心和架构评审员。不直接编写生产代码，但验证逻辑、分析数据库数据并为 OpenCode 制定任务。
技能库：
*   **上下文管理：** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`。
*   **分析与验证：** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`。
*   **数据库与数据可视化：** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`。

### 2.4. Antigravity (统一智能体环境)
一个集成了全套 33 个技能的完全自主环境。
*   **核心规则：** 从今往后，所有项目文档必须排他性地通过 Antigravity 并使用 Gemini 和 Claude 模型（作为拥有无限制技能访问权限的顶级文档工具）进行创建和维护。

---

## 3. 协议阶段 (项目生命周期)

### 阶段 1：初始化与 ARCHITECTURE.md
在编写任何代码之前制定架构。
1.  **Claude Desktop** 激活 `morning` 和 `Import-memory` 技能以加载上下文和先前的工作。然后应用 `analyze` 来分解需求。
2.  **OpenCode** 使用 `build-project-docs` 创建 `ARCHITECTURE.md` 的草案。
3.  稳定文档：数据结构、存储格式、技术栈和模块划分。

### 阶段 2：Grill-me (架构压力测试)
架构不能凭信念接受。它必须受到审视和攻防。
1.  **Claude Desktop** 应用 `data-context-extractor` 来识别数据中的“盲点”，并应用 `doc-coauthoring` 来生成棘手的问题。
2.  **OpenCode** 可以使用 `discernment-nudge` 对所提出的技术解决方案进行批判性的自我评估。
3.  每个有争议的决策点都通过以下三元组来关闭：**所选解决方案 -> 拒绝替代方案的原因 -> 从范围中排除的内容**。

### 阶段 3：刻意偏离 (Deliberate Deviations)
`ARCHITECTURE.md` 中的一个部分，我们在其中记录我们**自觉选择不构建**的所有功能和能力。项目能力的边界是其架构的一个完整组成部分。如果开发过程中决策发生变化，旧决策将与原因一起移至此处。

### 阶段 4：逐模块实现
开发沿着依赖图自底向上进行。
1.  **OpenCode** 实现项目核心。对于集成和协议，利用 `mcp-builder` 和 `claude-api`。
2.  在处理视觉方面时，**OpenCode** 激活链条：`brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`。
3.  对于程序化图形生成或复杂的画布，应用 `algorithmic-art` 和 `canvas-design`。

### 阶段 5：代码评审与测试
验证始终与编写代码分离开来。
1.  **OpenCode** 使用 `code-review-skill` 进行单独的检查，识别错误和折中。
2.  UI 和集成测试通过 `webapp-testing` 技能进行。测试输出 (stdout/stderr) 保持原样保存，不作任何修改。
3.  **Claude Desktop** 介入验证数据处理：它使用 `sql-queries` 和 `write-query` 检查数据库完整性，同时结合 `validate-data` 和 `statistical-analysis` 来验证业务逻辑。

### 阶段 6：构件与分析生成
项目必须呈现给用户或利益相关者。
1.  **Claude Desktop** 使用 `build-dashboard`、`create-viz` 和 `data-visualization` 基于应用结果或指标生成报告。
2.  **OpenCode** 将这些数据打包成现成的业务构件：
    *   报告与规格书：`pdf`、`docx`、`xlsx` 技能。
    *   架构演示：`pptx` 技能。
    *   培训与内部材料：`academy-guide`、`internal-comms`。
    *   用于公告的动态内容：`slack-gif-creator`。

### 阶段 7：最终清单
发布前验证以下内容：
*   最终代码与 `ARCHITECTURE.md` 的同步性。
*   存在实际的测试日志。
*   不存在临时文件、缓存和密钥。

---

## 4. 模型选择政策

OpenCode 运行在免费模型上，其选择取决于任务：

| 模型 | 角色 | 用途 | 隐私状态 |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | 自主智能体 (核心) | 执行主技能矩阵，1M token 上下文，终端中的多步逻辑。 | 永久免费层级 |
| **Nemotron 3 Ultra Free** | 深度分析师 | 重度数学、复杂算法、大规模系统重构。 | **NVIDIA 试用** — 数据会被记录以改进产品。 |
| **Nemotron 3.5 Lightning Free** | 后台执行者 | 快速验证、实用函数调用、大规模流水线处理。 | **NVIDIA trial** — 与 Ultra 相同。 |
| **MiMo V2.5 Free** | UI/UX 助手 | 截图调试、即时进行 `frontend-design`。 | 临时免费期。 |

对于 **Antigravity**，**Gemini 3.5 Flash (Medium)** 被用作主要引擎，以确保最小化 limits/quotas 消耗，并允许在任务和文档上进行持续的工作。

**安全限制：** **严禁**将私钥、token、真实数据库和私有仓库传至试用端点 (Nemotron, MiMo)。敏感数据仅可使用本地或受信任的环境。

---

## 5. 核心生态系统原则

1. **明确的决策优于便利的默认设置。** 如果智能体遇到分叉路口，它不会去猜测，而是制定选项并等待批准（或记录折中方案）。
2. **技能用于其指定目的。** 如果需要 Excel 报告，则无需生成 Markdown 表格（使用 `xlsx`）。无需用文本描述仪表板（使用 `build-dashboard` + `create-viz`）。
3. **评审中发现错误意味着系统正常运行。** 在评审阶段通过 `code-review-skill` 发现问题证明了两阶段过滤器正在发挥作用。
4. **项目边界神圣不可侵犯。** 一个半成品的“万能”工具不如一个具有清晰记录的“刻意偏离 (Deliberate Deviations)”部分的专用工具。
