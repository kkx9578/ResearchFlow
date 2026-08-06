# KAKAMEDLAB ResearchFlow

> Proprietary software information repository. Source code and executable files are not distributed through this repository.

**把临床 LLM 研究从手动复制粘贴，推进到标准化、可追溯、可批量运行、可形成投稿材料的可视化工作流。**

## 中文

KAKAMEDLAB ResearchFlow 是面向临床大语言模型研究的可视化工作流软件。它用于把固定 Prompt、统一模型配置、批量研究材料处理、运行记录和客观指标分析组织为可追溯的研究流程，降低直接编写 API 工程代码的门槛。

### 核心概念

- **标准化生成**：在同一 Prompt、材料契约和预设生成配置下运行一个或多个模型。
- **批量与重复运行**：支持批量研究材料、多模型比较和同一条件下的重复生成。
- **运行留痕**：记录模型标识、参数、响应状态、Token、费用、时间和内容校验值。
- **投稿材料**：生成正文简写、补充方法学和补充结果文件，供研究团队审阅后用于论文写作。
- **客观指标分析**：对已生成文本计算中文描述指标、文本结构、端到端效率和可选英文可读性指标。

ResearchFlow 是研究流程工具，不替代研究方案设计、伦理审查、临床专家评价、统计分析或医学判断。

### 课程与软件

ResearchFlow 是 **卡卡的Med大模型实验室（KAKAMEDLAB）临床大语言模型应用 SCI 课程**的配套研究工具，面向临床医学生、研究生和医生。课程系统讲解临床应用场景、Prompt 设计、API 运行、研究评价和论文报告；软件则把其中需要工程实现的批量调用、过程留痕和投稿材料整理收进可视化流程，让学员无需先成为程序员，也能规范开展 API 实验。

这不是替代科研判断的“自动写论文工具”，而是一套帮助研究者固定流程、减少重复劳动并保留方法学证据的研究基础设施。

### 当前版本

`Version 3.0.0 · Build 20260807.1`

版本变化见 [CHANGELOG.md](CHANGELOG.md)。

### 推荐致谢

> API-based LLM execution, run logging, and objective-metrics processing were supported by KAKAMEDLAB ResearchFlow (version 3.0.0, Build 20260807.1; KAKAMEDLAB, China). Software information is available at: https://github.com/kkx9578/ResearchFlow.

### 获取与联系

ResearchFlow 为商业专有软件，本仓库不提供源代码或安装包。

课程、软件授权与购买事宜，请联系微信公众号：**卡卡的Med大模型实验室（KAKAMEDLAB）**。

## English

KAKAMEDLAB ResearchFlow is a proprietary visual workflow application for clinical large-language-model research. It supports standardized API-based generation, batch and repeated execution, run provenance, publication-oriented supplementary artifacts, and objective text metrics.

This repository documents the product concept, release identity, and recommended acknowledgement only. It does not distribute source code, executables, activation components, payment systems, credentials, or internal infrastructure.

ResearchFlow does not replace protocol design, ethics review, clinical evaluation, statistical analysis, or professional medical judgment.

See [PROPRIETARY_NOTICE.md](PROPRIETARY_NOTICE.md) for rights and use restrictions.
