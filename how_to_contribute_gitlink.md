# Gitlink 项目贡献流程与命令详解  

以下为基于 **Gitlink** 平台的标准项目贡献流程，采用 `upstream` 上游同步机制，**适用于未开放 Pull 权限的参赛场景**（如 GPUCodeForces / GPUApps / GPUKernelContest 等仓库）。  

---

## 0  CLA 签署

- **目的**：为确保项目版权与贡献者权益的清晰，项目内的 Pull Request 需要贡献者**签署贡献者许可协议（CLA）** 后方可合并。  
- **步骤**：  
  点击 [CLA 签署链接](https://www.gitlink.org.cn/ccf-ai-infra/cla/governance)，阅读协议后在页面底部填写真实姓名，并使用参赛所用账号的邮箱完成签署。


---


##  总体流程

```mermaid
flowchart TD
  A[Fork 仓库到自己的 Gitlink 账户] --> B[Clone 本地并设置 upstream]
  B --> C[创建开发分支]
  C --> D[修改代码并提交 commit]
  D --> E[推送到远程 Fork 仓库]
  E --> F[在 Gitlink 上创建 Pull Request]
  F --> G[根据维护者反馈修改并更新 PR]
  G --> H[PR 被合并]
  H --> I[使用 upstream 同步上游仓库]（此步骤可在开发中途定期进行，以保证分支同步，减少冲突）
```

---

## 1️ Fork 仓库
**目的：** 将原始仓库复制到你的 Gitlink 账户下。

**操作方式：**  
- 登录您的 Gitlink之后，打开对应子赛题目标仓库（如 GPUCodeForces）。  
- 点击右上角 **「Fork」** 按钮。

> Fork 后地址示例：`https://gitlink.org/<yourname>/GPUCodeForces`

---

## 2️ Clone 仓库并设置 upstream
**目的：** 将 Fork 的项目克隆到本地，并指定原始仓库为上游（upstream）。

```bash
# 克隆你的 Fork
git clone https://gitlink.org/<yourname>/GPUCodeForces.git
cd GPUCodeForces

# 设置上游（仅一次）
git remote add upstream https://gitlink.org/opengrow/GPUCodeForces.git

# 查看远程配置，确认有 origin 与 upstream
git remote -v
```

> - `origin`：你的个人 Fork 仓库  
> - `upstream`：原始主仓库  

---

## 3. 创建新分支进行开发
- **目的**：在新的分支上进行修改，避免直接修改主分支。
- **步骤**：
  - 进入克隆的仓库目录（如：GPUCodeForces）。
    ```sh
    cd GPUCodeForces
    ```
    
  - 创建一个新的分支来（例如：`feature/fix-algo`分支）进行您的项目开发或者修订。
    ```bash
    # 确保当前为 main
    git checkout main
    # 使用 upstream 同步最新主仓库代码
    git pull upstream main
    # 创建新的开发分支
    git checkout -b feature/fix-algo
    ```
  >  定期使用 `git pull upstream main` 即可直接从上游拉取更新


## 4️ 修改代码并提交
**目的：** 完成开发任务并记录变更。

```bash
git status          # 查看变更
git add .           # 添加修改
git commit -m "fix: 修复算法精度问题 Fixes #45"
```

> 提交信息建议规范书写，包含类型（fix/feat/docs等）与说明。

---

## 5️ 推送到远程 Fork
**目的：** 将你的开发分支推送到远程仓库。

```bash
git push origin feature/fix-algo
```

> `origin` 是你个人的 Fork 仓库，PR 将从这里发起。

---

## 6️ 发起 Pull Request（PR）
**目的：** 向上游仓库提交合并请求。

**网页端操作：**  
- 登录 Gitlink，进入你的 Fork 仓库。  
- 点击 **「发起合并请求（Pull Request）」**。  
- 设置源分支（Source）：`<yourname>/feature/fix-algo`  
- 设置目标分支（Target）：`ODTC AI Infra/GPUCodeForces/main` (GPUCodeForces可替换成对应的子赛题仓库名)
- 填写变更说明。


---

## 7️ 根据反馈修改
**目的：** 根据代码评审反馈更新同一个 PR。

> 比赛要求参赛选手提交的一个PR中所包含的commit较为简洁，重复内容需合并为一个commit。
若已经出现多个无关且重复 commit 选手可尝试 rebase 进行解决。

推荐选手可以采用 amend 进行修改，以下是使用 amend 进行修改的示例代码。

```bash
# 修改后重新提交
git add .
git commit --amend -m "fix: 调整参数校验逻辑 (PR review update)"

# 更新远程 PR 分支
git push origin feature/fix-algo --force-with-lease
```

---

## 8. PR被合并
- **目的**：一旦您的PR被接受并合并到主分支，您的贡献就正式成为项目的一部分。
- **步骤**：
  - 项目维护者会合并您的PR。
  - 您的修改现在成为原始仓库的一部分。

---

## 9️ 使用 upstream 同步上游仓库（此步骤可以在每次开发前进行）
**目的：** 保持本地与上游主仓库一致。

```bash
# 切换到主分支
git checkout main

# 直接从 upstream 拉取最新版本
git pull upstream main

# 推送到自己的 Fork
git push origin main
```

>  建议每次开发前执行一次此步骤，保持分支同步，减少冲突。

---

##  建议实践
- 不要直接修改 main 分支。  
- 定期同步 upstream，保持分支干净。
- **每个功能一个独立分支**，方便维护与回溯。  
- **提交说明清晰、含义明确**，便于协作记录。
