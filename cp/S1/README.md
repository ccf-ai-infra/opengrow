# 开源GPU创新生态赛常规赛第一期（S1）

## 背景
中国计算机学会（CCF）开源发展委员会（ODTC）主办的“开源GPU创新生态赛（常规赛）”即将启动。该赛事聚焦GPU技术与开源生态的深度融合，旨在推动国产算力创新及人工智能普惠化发展，吸引全球开发者、高校团队及企业共同探索GPU底层优化、算法加速与生态共建。面对大模型推理的“三高”困境（高延迟、高显存、高生态依赖），本次竞赛聚焦 GPU 底层算力革新与开源生态建设，诚邀全球开发者共同攻坚。优胜团队将获得奖金及与头部企业合作机会。在享受技术挑战的同时能获得意外的收获：

✅ **顶会论文署名：** 优胜方案将整合发表于相关论文（半年分赛道前50贡献者署名）
✅ **工业级落地：** 核心成果应用于头部企业生产环境，最佳实践直通官方仓库

赛事提供免费算力支持，并联合国产GPU厂商、互联网厂商、大模型研究机构等企业提供技术指导，推动GPU开源生态繁荣。

## 🎯 设置三大赛道，10万奖金等你来拿！！！

- **[赛道一、评测数据集生成挑战赛](https://gitee.com/ccf-ai-infra/GPUCodeForces)** 
- **[赛道二、GPU 开源生态挑战赛](https://gitee.com/ccf-ai-infra/GPUApps)**
- **[赛道三、GPU 算子优化挑战赛](https://gitee.com/ccf-ai-infra/GPUKernelContest)**

## 💥 三大赛道解读·硬核攻坚GPU开源生态

### 赛道一、评测数据集生成挑战赛

在 AI 模型开发和部署中，GPU 性能评测是一个非常重要的环节。不同 GPU、不同深度学习框架（如 PyTorch、TensorFlow、PaddlePaddle 等）在运行相同任务时，速度、吞吐量、内存占用等表现差异很大。本次挑战赛希望通过社区的力量，构建一个标准化、带权重的评测数据集，让 GPU 性能比较更加科学、公正。

#### 📌 挑战方向
- **目标：** 构建测试 GPU 的样本加权的评测数据集（来源：PyTorch、PaddlePaddle、TensorFlow、Jax、MMCV、Transformers 等）
- **项目价值：** 形成标准的 GPU 评测数据集和评价方法
- **参赛资格：**
  参赛者贡献的样本中，被评审通过并正式整合到[GPU CodeForces](https://gitee.com/ccf-ai-infra/GPUCodeForces)数据集项目的样本总数 ≥ 1

#### 📤 提交要求

- 每位选手按赛题解读要求提交内容：先开赛题Iusse，关联Iusse ID的PR方式提交，详见：[001-sample](https://gitee.com/ccf-ai-infra/GPUCodeForces/tree/main/example/001-example)
- **接受数量** = 提交并被接受的样本总数

#### 🏆 评分规则及排名机制

1. 按“接受数量”从高到低排序
2. **评估规则：** 取前 12 名作为最终获奖选手
3. 若数量相同：
   - 比较总评分高者优先
   - 若仍相同，比加分项得分高者优先
4. 当同一参赛选手在本赛题有多个赛题的提交时，可累加赛题PR合并的数量，最终以每个选手唯一ID提交合并的总数为准。

> 感兴趣详细了解细致参考：[赛题一详细解读](https://gitee.com/ccf-ai-infra/GPUCodeForces)

---

### 赛道二、GPU 开源生态挑战赛

在CUDA成为目前最主流的开源AI生态，如何能高效的构建兼容CUDA的GPGPU软件生态会成为后续AI生态成长很重要的一个方向。通过该赛道的挑战，能摸索一条相对快速的适配上游社区快速支持国产MXMACA软件生态。利用MXMACA兼容CUDA的GPU软件生态，实现GPU软件生态的快速适配，并尝试利用GPU软件生态的优化，提高模型性能。

#### 📌 挑战方向

- **目标：**
    - 模型迁移：单 Transformers 模型迁移到 vLLM / SGLang（可运行并优化）
    - 论文复现：AI4S 领域前沿论文复现与加速
    - 生态破局：将 CUDA AI 开源软件迁移至国产 MXMACA 软件栈
    - 生态繁荣：Jax 模型迁移至 PyTorch
- **可参考项目列表:**
    - [LMDeploy](https://github.com/internlm/lmdeploy)
    - [InfiniCore](https://github.com/InfiniTensor/InfiniCore)
    - [FlashMLA](https://github.com/MetaX-MACA/FlashMLA)
    - [vLLM-metax](https://github.com/MetaX-MACA/vLLM-metax)
    - [mcPytorch](https://github.com/MetaX-MACA/mcPytorch)
- 其它方向
- **项目价值：** 推动国产 AI 基础设施自主化
- **参赛资格：** 提交的代码可在MXMACA软件栈上运行

#### 📤 提交要求及评分标准

- 每位选手按赛题解读要求提交内容：先开赛题Iusse，关联Iusse ID的PR方式提交。
- 如提交直接是上游仓库的PR，先开赛题Iusse，Iusse关联上游PR<注意：最终审核已唯一email地址是否为同一账号为唯一依据，注意：请其它上游仓库用相同email地址作为提交邮箱>。

- **评分标准：**
  
  - 能成功复现运行：60 分
  - 输出正确结果（参考 CUDA 平台）：61~100 分
  - **加分项：**
    - 提供性能优化，且提供可复现的对比测试报告：+0~50 分

#### 🏆 排名机制

1. 评委评分从高到低排序
2. **评估规则：** 取前 12 名作为最终获奖选手
3. 若分数相同：
   - 性能提升高者优先
   - 内容完整性高者优先
4. 当同一参赛选手在本赛题有多个赛题的提交时，只取最高分，不累加多个赛题得分

---

### 赛道三、GPU 算子优化挑战赛

在大模型推理时代，通过GPU算子优化比赛汇聚开发者，加速国产硬件软硬件协同优化，突破生态壁垒，推动从“可用”到“好用”；针对Transformer等推理负载激发生态创新，锤炼底层算子的极致性能与能效，缩短与国际芯片的性能差距；以赛促研，培养国产芯片适配人才，同时沉淀优化经验，为建立自主产业标准提供实践基础。

#### 📌 挑战方向

- **定向突破：** 基于大模型 Test Time Scaling 技术，优化 PyTorch / PaddlePaddle 算子性能
- **核心攻坚：** LLM 的 Gemm 核心计算内核极致调优
  
 ▶ **项目价值：** 在同等硬件条件下提升 30% 推理性能

#### 📤 提交要求及评分规则

- **参赛资格：** 优化内容可在曦云 C500 上运行，并被主办方审核合并（Merge）
- **提交方式：** 通过 PR 提交到 Gitee 仓库（GPUKernelContest），最终以成功 Merge 为准

- **基础得分（Level）：**
  
  - Level 1：单个 PyTorch / Paddle 算子（5 分）
  - Level 2：2~9 个算子融合（10 分）
  - Level 3：带有 MMA 的融合算子（50 分）
  - Level 4：大模型推理复杂融合算子（50 分）
  - 成功 PR 合并至沐曦正式算子项目（50 分）

- **加分项：**
  
  1. 代码质量：+10 分
  2. 性能优化：+10 分
  3. 写明优化过程并加权说明大模型来源：+20 分
  4. 使用 LLM prompt 生成算子及测试样例：+20 分

> 注意： 加分项只针对于在基础得分相同的情况下通过加分项来区分不同的排名和后续优秀选手的参考。

#### 🏆 排名机制

1. 评委评分从高到低排序
2. **评估规则：** 取前 12 名作为最终获奖选手
3. 若基础得分相同：
  - 加分项多者优先
  - 提交数量多者优先
  - 提交时间早者优先
4. 当同一参赛选手在本赛题有多个赛题的提交时，多个赛题计算累计得分

#### 📂 沐曦正式算子项目仓库参考

- https://github.com/MetaX-MACA/FlashMLA
- https://github.com/MetaX-MACA/mcTVM
- https://github.com/MetaX-MACA/mcEigen
- https://github.com/MetaX-MACA/mcPytorch

---

## ⚠️ 注意事项（以下情况取消参赛资格）

1. 抄袭他人代码或成果
2. 恶意提交（如相同算子多次提交、相近优化重复提交）
3. 

## 赛事支撑及支持

### 赛事联系方式

- 邮箱：zhangjinnan@hotmail.com

### 算力平台及算力卷支持

- [算力平台使用说明](https://ai.gitee.com/docs/compute/container)
- [算力券兑换发放和兑换](https://ai.gitee.com/docs/billing/coupons)
