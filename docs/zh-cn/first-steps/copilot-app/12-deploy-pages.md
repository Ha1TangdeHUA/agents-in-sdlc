---
title: "课程 12 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot 应用配置 Pages 工作流、审查拉取请求并验证已发布的 Space Quiz。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

使用 GitHub Pages 部署 Space Quiz，让更多人可以访问。Copilot 可以准备工作流并指导部署，但你仍需负责审查更改并确认网站已上线。

在本课程中，你将：

- 请 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和拉取请求。
- 跟进部署并验证已发布的网站。

## 场景

Space Quiz 已位于 GitHub 存储库中，但其他人仍需要一种简单的方式来试用它。使用 GitHub Pages 发布这个单文件网站后，它就能通过公共 URL 访问，无需添加服务器或运行时依赖项。

## 请 Copilot 部署网站

在 `space-quiz` 的 Copilot 应用会话中发送以下提示：

```plaintext
为此存储库启用 GitHub Pages。创建一个 GitHub Actions 工作流，在需要时构建网站并将其部署到 GitHub Pages。如果尚无 README，请添加一个文件，介绍应用以及如何在本地运行它。使用这些更改创建拉取请求，并在必需的检查通过后合并。持续监视部署，直到成功，然后报告已上线网站的最终 URL。如果你没有启用 Pages 或合并的权限，请准确说明我需要批准或执行的操作；在网站上线之前，不要报告成功。
```

![三阶段示意图：已合并的 space-quiz 拉取请求；GitHub Actions 中 Deploy website 运行成功，包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及通过 yourname.github.io/space-quiz/ 访问的 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求智能体创建并合并拉取请求，以及更改存储库的 Pages 设置。继续之前，请审查差异、部署权限和 GitHub 的审批提示。

## 审查工作流并验证部署

1. 确认仅当存储库尚无 README 时才添加了 README。
2. 审查拉取请求中的更改，包括工作流的构建和部署步骤。
3. 仅在必需的拉取请求检查通过后合并。
4. 跟进 GitHub Actions 部署运行，直到成功。
5. 打开报告中的 URL，确认 Space Quiz 可以加载。

如果智能体无法启用 Pages 或合并拉取请求，请按照它提供的具体说明操作。只有在部署成功且网站可以加载后，才能将任务视为完成。

## 总结和后续步骤

Space Quiz 现在已作为网站上线。你亲自验证了部署，而不是仅依赖智能体的报告。继续学习[课程 13：回顾与后续步骤][next-lesson]。

[next-lesson]: ../13-review/
