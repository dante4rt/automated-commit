# 自动提交 Automated-Commit

[English](README.md) | 简体中文

本仓库包含一个 GitHub Actions 工作流，每隔 12 小时会自动更新一个名为 `TIMESTAMP.txt` 的文件，并标注当前日期和时间。如果你是 GitHub 或 GitHub Actions 的新手的话，本 README 将详细介绍该工作流的操作方法，并指导你如何自定义和使用它。

### 概述

 `Automated-Commit` 工作流展示了 GitHub Actions 在仓库中自动化常规任务的能力。具体工作流如下：

- 从 `master` 分支检查最新代码。
- 使用当前日期和时间更新 `TIMESTAMP.txt` 文件。
- 如果检测到任何修改，则将修改提交到版本库。
- 将修改推送回 `master` 分支。

### 工作流程结构

工作流程定义在 `.github/workflows/master.yml` 文件中，包括：

- **触发器**： 配置为每 12 小时运行一次，可通过 GitHub UI 的 `workflow_dispatch` 事件手动触发。
- **工作和步骤**： 包含一个 `update_commit` 作业，在最新的 Ubuntu runner 上运行，执行设置 Git、更新 `TIMESTAMP.txt`、提交和推送更改等任务。
- **权限**： 授予对仓库内容的写入权限。

### 使用此工作流程

### 创建您自己的版本

要创建自己仓库和工作流程，请执行以下操作：

1. 点击 GitHub 仓库页面上的 “Use this template” 按钮。
2. 为您的新仓库创建一个名称，然后选择 “Create repository from template” 。
3. 克隆您的新仓库以便在本地进行进一步自定义。

### 自定义工作流程

在使用工作流之前，您需要使用您的 GitHub 用户邮箱和名称进行自定义：

1. 导航至仓库中的 `.github/workflows/master.yml` 文件。
2. 编辑该文件，在 `Setup Git Configuration` 步骤中将 `“rxmxdhxni@gmail.com”` 替换为您的电子邮件，将 `“dante4rt”` 替换为您的 GitHub 用户名。
3. 提交您的更改。

### 查看工作流运行

要查看工作流的运行历史：

1. 导航到您仓库的 `Actions` 标签。
2. 选择 `Automated-Commit` 工作流以查看每次运行的详细信息。

###手动触发工作流程

您可以手动触发工作流：

1. 前往您仓库的 `Actions` 标签。
2. 选择 `Automated-Commit` 工作流。
3. 点击 `Run workflow`，选择 `master`，然后再次点击 `Run workflow`。

## 贡献

欢迎贡献！随时 fork 仓库，进行更改并提交 pull request。

## 支持

如有问题或疑问，请在仓库提交 `Issues` 。

感谢您浏览 自动提交 Automated-Commit workflow！
