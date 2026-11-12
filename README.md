<p align="center">  
  <img src=*"./logos/AI Infra/AI Infra.png" width="210" alt="CCF ODTC AI Infra 工作组">  
</p>*

*<h1 align="center">OpenGrow · 开源 AI Infra 入门实践者协作计划</h1>*

*<p align="center">  
  一个由入门者参与、也由入门者带入门者的开源协作空间。  
  
  你不需要先成为专家，才有资格开始贡献。  
</p>*

*<p align="center">  
  中国计算机学会（CCF）开源发展技术委员*会（ODTC）AI Infra 工作组 发起  
  
  依托「CCF-光华青年开源基金」 ｜ 木兰宽松许可证 v2  
</p>

---

## 🚀 几条最快的入口

| 我想……          | 从这里开始                                                                        |
| ------------- | ---------------------------------------------------------------------------- |
| 先搞清楚贡献流程      | [贡献指南（Gitlink 版，含流程图与 CLA）](./how_to_contribute_gitlink.md)                  |
| 先看看组织都有什么     | [项目地图：25 个仓库怎么挑](#map)                                                       |
| 找一件能马上上手的事    | [提交 Issue 认领任务](https://www.gitlink.org.cn/ccf-ai-infra/opengrow/issues/new) |
| 只想分享一点经验，不写代码 | [分享你的实践](#share)                                                             |

## 🌱 这是什么

OpenGrow 是由中国计算机学会（CCF）开源发展技术委员会（ODTC）AI Infra 工作组发起的开源志愿者计划项目，依托「CCF-光华青年开源基金」，汇聚高校、企业及开发者公益的力量，致力于构建开源 AI 基础设施项目健康发展，建立行业开放标准，推动产学研协同创新。

- **愿景**：用开源精神驱动 AI 进化，让智能更开放、平等。
- **使命**：通过开放协作降低 AI 开发门槛，加速技术民主化进程。

落到每个人身上，它其实只做一件事：**把「想参与开源、又不知道从哪下手」的人聚在一起，一起读代码、一起写文档、一起踩坑、再把踩过的坑写下来。**

这里不设门槛、不排名次、不卡身份。第一次提 Issue、第一次提 PR、第一次做一次十分钟的分享，都可以发生在这里。

## 👥 这里适合谁

- 还没提交过 PR，但想有一个真实仓库可以练手的学生和转行者
- 刚跑通第一个开源项目，想把过程记录下来、顺便帮到后来者的人
- 会写文档、会做翻译、会整理纪要，但觉得自己「不会写代码所以不算贡献者」的人
- 已经合过一次 PR，愿意回头带一位新人的实践者

不需要报名，不需要面试。看到有想做的事，直接开一条 Issue 说「我想做这个」即可。

## 🗺 组织里有什么：项目地图<a id="map"></a>

CCF ODTC AI Infra 组织下有 25 个仓库，看上去很杂，其实是三级台阶：**先跑起来 → 做出一个东西 → 再给上游提交**。按自己在哪一级来挑，不用从第一个仓库顺着看。

### 第一级 · 先跑起来（有教程、有算力，不必先会写代码）

| 项目 | 你会得到什么 | 技术栈 | 第一步 |
| --- | --- | --- | --- |
| [vLLM101](https://gitlink.org.cn/ccf-ai-infra/vLLM101) | 从装好第一个模型到多卡调优的 vLLM 完整路径 | vLLM / 沐曦 GPU | 按 Phase 1 → 4 顺序走 |
| [Intro-ops](https://gitlink.org.cn/ccf-ai-infra/Intro-ops) | TileLang 闯关式算子练习，已积累 95 次 fork | Python / TileLang | clone 后从第一关开始 |
| [Transformer-on-Metax](https://gitlink.org.cn/ccf-ai-infra/Transformer-on-Metax) | 21 天在国产 GPU 上手写一个 Transformer | PyTorch / 曦云 | 跟着六课任务做 |
| [AI-Starter](https://gitlink.org.cn/ccf-ai-infra/AI-Starter) | AI 模型部署与落地应用的入门教程 | Markdown | 直接读，照着示例跑 |
| [Model2App](https://gitlink.org.cn/ccf-ai-infra/Model2App) | 选一个模型，做出一款自己的 AI 应用 | Python / 模型 API | 先跑通示例再改造 |

### 第二级 · 做出一个能运行的东西

| 项目 | 你会得到什么 | 技术栈 | 第一步 |
| --- | --- | --- | --- |
| [Science-Agent-Lab](https://gitlink.org.cn/ccf-ai-infra/Science-Agent-Lab) | 用国产 GPU 做科研：AI4S Skills、Boltz2、GROMACS | Python / AI4S | 先读算力申请指南，再选一课 |
| [llm-learning-assistant](https://gitlink.org.cn/ccf-ai-infra/llm-learning-assistant) | 用 Agent 四步（Research → Design → Build → Test）做一个教育应用 | Python / 大模型 API | 跑参考案例，改一版自己的 |
| [from_prompt_to_prototype](https://gitlink.org.cn/ccf-ai-infra/from_prompt_to_prototype) | 从一句提示词到一个可运行原型的方法 | VS Code + Cline | 照工坊流程做一个自己的 |
| [gollamago](https://gitlink.org.cn/ccf-ai-infra/gollamago) | 九源软件栈 + 曦云 GPU 算子开发实战营 | Python / 曦云 | 按 Task01 → 04 补齐 |
| [Full_Link_Development_of_Large_Models](https://gitlink.org.cn/ccf-ai-infra/Full_Link_Development_of_Large_Models) | 书生体系大模型全链路教材（InternLM3 / InternVL） | HTML 书稿 | 已有 3 个勘误 Issue，改一处就能提交 |

### 第三级 · 给上游提交，或参与规则制定

| 项目 | 你会得到什么 | 技术栈 | 第一步 |
| --- | --- | --- | --- |
| [TileOPs-Metax](https://gitlink.org.cn/ccf-ai-infra/TileOPs-Metax) | 基于 TileLang 的高性能算子库，累计 177 个 Issue、151 次 fork | Python / TileLang / MACA | 挑一个「纯线上算子认领」 |
| [macawiki](https://gitlink.org.cn/ccf-ai-infra/macawiki) | 面向 MXMACA 的可追溯知识库，证据链 + Agent Skill | Python 标准库 | 跑 `scripts/validate.py`，提一份证据缺口 |
| [open-gov-book](https://gitlink.org.cn/ccf-ai-infra/open-gov-book) | 23 章开源治理书《当 AI 写代码，谁来守住护栏》 | Markdown | 认领一章做事实核对 |
| [opengrow](https://gitlink.org.cn/ccf-ai-infra/opengrow) | 就是本仓库：协作机制、标签体系、新人路径 | Markdown | 往下读「怎么开始」 |

### 怎么挑

- **只想先看看** → 第一级，一周内能跑通一个，先建立手感
- **想有个作品能演示** → 第二级，结束时手里有一个能运行的东西
- **想要 commit 记录，或想参与规则怎么定** → 第三级，真实的上游仓库与社区机制

### 三个容易踩的坑

- 课程与工坊类仓库（Intro-ops、Transformer-on-Metax、gollamago、Model2App、from_prompt_to_prototype、Science-Agent-Lab 等）的 Issue 是**作业与作品提交入口**，不是任务看板，别在那里认领任务
- GPUCodeForces、GPUApps、GPUKernelContest 是**历史赛季归档**，已经收口，不再接新任务
- openmeal、tilelang-puzzles 目前还是空仓，暂时没有内容可参与

## 🛠 你可以参与什么

项目地图告诉你「去哪个仓库」，这一节告诉你「做哪种角色」——两者可以叠加：你完全可以在 TileOPs 认领一个算子，同时在 opengrow 维护流程文档。

下面每一项都可以直接开始，不需要等谁批准。表格里没有你想做的方向，也欢迎自己开 Issue 提出来。

| 方向      | 需要什么基础           | 具体协作方式                       |
| ------- | ---------------- | ---------------------------- |
| 入门路径整理  | 零基础              | 把你自己摸清楚的过程写成步骤，供后来者复用        |
| 贡献指南维护  | 会 `git clone` 即可 | 校对、补充、修订流程文档，发现走不通的地方直接提 PR  |
| 文档与翻译   | 中文表达清楚           | 组织文档、项目 README 的中英互译与润色      |
| 社区分享    | 有过一次踩坑经验         | 提交分享提纲或笔记，组织一次线上小范围交流        |
| 新人答疑与结对 | 完成过一次 PR         | 认领 Issue 答疑，带一位新同学跑通自己的首个 PR |
| 活动记录与传播 | 会写纪要、会做图         | 整理分享会纪要、共建者故事、活动回顾           |
| 治理与标准讨论 | 对流程和规则敏感         | 参与治理框架讨论，把共识沉淀成文档            |

其中标有 `入门任务` 标签的 Issue 专为第一次参与的人准备，做不完也没关系。

## 🧭 怎么开始（四步）

1. **读一遍贡献指南** —— [Gitlink 版](./how_to_contribute_gitlink.md)（推荐，含 mermaid 流程图和 CLA 签署入口）；习惯 Gitee 的同学可以看 [Gitee/GitHub 版](./how-to-contribute.md)。
2. **领一件小事** —— 在 [Issues](https://www.gitlink.org.cn/ccf-ai-infra/opengrow/issues) 里挑一个，或者自己开一条说明你想做什么、大概需要什么帮助。
3. **提一个 PR** —— Fork → 建分支 → 修改 → 提交 → 发起 PR。**一个 PR 只做一件事**，标题写清「做了什么」，方便维护者快速看懂。
4. **签署 CLA** —— 首次 PR 需要先签[贡献者许可协议](https://www.gitlink.org.cn/ccf-ai-infra/cla/governance)，用提交所用账号的邮箱签署即可。

> 卡住了，就在 Issue 里直接说「我卡在第 2 步，报错是这样」。会有维护者回你——**这本身就是这个项目存在的意义之一**，不必等自己全懂了再发问。

## 🧩 卡住了？用标签说清你在等什么

开源的挫败感，多半不是技术难，而是「不知道该找谁、也不清楚自己到底在等什么」。所以这里的 Issue 用一个标签标明它此刻卡在哪：

| 标签    | 你在等  | 典型场景                           |
| ----- | ---- | ------------------------------ |
| `待确认` | 一个判断 | 方案或口径拿不准，需要有人拍板                |
| `待支持` | 一份资源 | 缺权限、算力、账号或环境，需要有人帮忙开通          |
| `待验收` | 一次收口 | 交付已就绪，等确认能否关闭或进入下一步            |
| `待上游` | 外部回应 | 已提 PR，等上游社区 review 或合并，球不在我们这边 |

另外三个标签用来表达别的东西：

- `入门任务` —— 专为第一次参与的人准备，不要求做完，也不追究半途而废
- `灵光一现` —— 你自己想到、还没立项的点子，欢迎来拍砖。请附&#x5E26;**「最小第一步」**，两周内会得到明确回应：采纳、合流，或暂缓并说明原因
- `建设性反对意见` —— 基于数据的反对，比附和更有价值

两条约定：

1. **标签只是索引，@ 具体的人才是动作。** 只打标签不发消息，大概率没人看见。
2. **提问不需要先自证水平。** 写清「我做到哪一步、报错是什么、我猜是什么原因」，比写一段客套话有用得多。

## ✍️ 分享你的实践<a id="share"></a>

我们相信「写下来」本身就是一种贡献，而且是最容易被低估的那种。三类不需要写代码的参与方式：

- **踩坑记录** —— 环境配置失败、编译不过、PR 被要求改了三轮……写成一页笔记，比你想象中更有用。
- **入门路径** —— 从零到第一个 merge 的完整步骤，标注每一步大概花了多久，后来者会照着走。
- **复盘与建议** —— 觉得贡献指南哪里绕、流程哪里多余，直接提 PR 改，比在群里吐槽有效。

做法很简单：开一条 Issue，标题以 `[分享]` 开头，正文贴 Markdown 或文档链接，再打上 `被看见` 标签。维护者会定期把优质内容汇总到本页，作者署名保留。

## 🎁 荣誉与激励

- **年度奖项**：最佳推广大使、最具影响力提案奖等荣誉体系
- **人才通道**：优秀贡献者推荐加入知名企业、参与开源企业生态合作
- **可追溯的贡献记录**：每一条 Issue、每一个 PR 都留在仓库历史里，可以写进简历、写进毕业材料

## 🌍 加入我们

- 关注组织动态：[CCF AI Infra @ Gitlink](https://www.gitlink.org.cn/ccf-ai-infra)
- 加入微信群，先潜水看看大家在做什么：

<p align="center">  
  <img src="./images/join_in.png" width="280" alt="OpenGrow 微信交流群二维码">  
</p>

## 📚 相关文档

- [贡献指南 · Gitlink 版](./how_to_contribute_gitlink.md) —— 含 CLA 签署、upstream 同步、PR 修改与 rebase
- [贡献指南 · Gitee/GitHub 版](./how-to-contribute.md) —— 基于网页端操作的逐步说明
- [AI Infra 工作组介绍](./AIInfra.md) —— 组织架构、核心目标、重点工作
- [工作组背景与年度目标](./AIInfra_target.md) —— 基金来源与年度任务
- [LOGO 下载与使用](./logos/AI%20Infra) —— 四套配色，含浅色/深色背景版与社交头像
- [许可协议](./LICENSE)

## 📄 许可协议

本仓库内容遵循[木兰宽松许可证，第 2 版（Mulan PSL v2）](./LICENSE)。引用、转载或二次分发，请保留出处与许可声明。
