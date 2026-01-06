---
title: 贡献指南
description: 如何为文档做出贡献
weight: 10
---

{{% pageinfo %}}

这些基本示例指南假设您的 Docsy 站点使用 Netlify 部署，您的文件存储在 GitHub 中。您可以"按原样"使用这些指南，或使用您自己的说明进行调整：例如，其他部署选项、关于您的文档项目文件结构的信息、特定于项目的审查指南、版本控制指南或您的用户在更新您的站点时可能觉得有用的任何其他信息。
[Kubeflow](https://github.com/kubeflow/website/blob/master/README.md) 有一个很好的示例。

不要忘记链接到您自己的文档仓库而不是我们的示例站点！还要确保用户可以从您的文档仓库 README 中找到这些指南：要么在那里添加它们并从此页面链接到它们，要么在此处添加它们并从 README 链接到它们，或者在两个位置都包含它们。

{{% /pageinfo %}}

我们使用 [Hugo](https://gohugo.io/) 来格式化和生成我们的网站，使用 [Docsy](https://github.com/google/docsy) 主题进行样式设置和站点结构，并使用 [Netlify](https://www.netlify.com/) 来管理站点的部署。Hugo 是一个开源静态站点生成器，为我们提供模板、标准目录结构中的内容组织以及网站生成引擎。您用 Markdown（或 HTML，如果您愿意）编写页面，Hugo 将它们包装成一个网站。

所有提交，包括项目成员的提交，都需要审查。我们为此目的使用 GitHub pull requests。有关使用 pull requests 的更多信息，请查阅 [GitHub 帮助](https://help.github.com/articles/about-pull-requests/)。

## 使用 Netlify 快速开始

这是更新文档的快速指南。它假设您熟悉 GitHub 工作流，并且您很高兴使用文档更新的自动预览：

1. 在 GitHub 上 Fork [RoboticPlus.AI 仓库](https://github.com/roboticplus/flash)。
1. 进行更改并发送 pull request (PR)。
1. 如果您还没有准备好进行审查，请在 PR 名称中添加 "WIP" 以表示正在进行中。（**不要**在页面前置元数据中添加 Hugo 属性 "draft = true"，因为这阻止了下一段中描述的内容预览的自动部署。）
1. 等待自动 PR 工作流进行一些检查。准备就绪后，您应该看到类似这样的评论：**deploy/netlify — 部署预览已准备就绪！**
1. 单击 "Deploy preview ready" 右侧的 **Details** 以查看更新的预览。
1. 继续更新您的文档并推送您的更改，直到您对内容满意为止。
1. 当您准备好进行审查时，在 PR 中添加评论，并删除任何 "WIP" 标记。

## 更新单个页面

如果您在使用文档时发现了想要更改的内容，Docsy 为您提供了一个快捷方式：

1. 单击页面右上角的 **编辑此页面**。
1. 如果您还没有项目仓库的最新 fork，系统会提示您获取一个 - 单击 **Fork 此仓库并提出更改** 或 **更新您的 Fork** 以获取要编辑的项目的最新版本。您 fork 中的相应页面以编辑模式显示。
1. 按照上面的 [使用 Netlify 快速开始](#使用-netlify-快速开始) 过程的其余部分来制作、预览和建议您的更改。

## 在本地预览您的更改

如果您想运行自己的本地 Hugo 服务器来预览您的工作更改：

1. 按照 [入门](/zh/docs/getting-started) 中的说明安装 Hugo 和您需要的任何其他工具。您至少需要 **Hugo 版本 0.146.0**（我们建议使用最新的可用版本），并且必须是支持 SCSS 的**扩展**版本。
1. 将 [RoboticPlus.AI 仓库](https://github.com/roboticplus/flash) fork 到您自己的项目中，然后使用 `git clone` 创建本地副本。

   ```
   git clone --branch main --depth 1 https://github.com/roboticplus/flash.git
   ```

1. 在站点根目录中运行 `hugo server`。默认情况下，您的站点将在 http://localhost:1313/ 可用。现在您正在本地提供站点，Hugo 将监视内容更改并自动刷新您的站点。
1. 继续使用通常的 GitHub 工作流来编辑文件、提交它们、将更改推送到您的 fork，并创建 pull request。

## 创建问题

如果您在文档中发现了问题，但不确定如何自己修复，请在 [RoboticPlus.AI 仓库](https://github.com/roboticplus/flash/issues) 中创建问题。您也可以通过单击页面右上角的 **创建问题** 按钮来创建关于特定页面的问题。

## 有用的资源

- [Docsy 用户指南](https://www.docsy.dev/docs/)：关于 Docsy 的所有内容，包括它如何管理导航、外观和多语言支持。
- [Hugo 文档](https://gohugo.io/documentation/)：Hugo 的综合参考。
- [Github Hello World!](https://guides.github.com/activities/hello-world/)：GitHub 概念和工作流的基本介绍。
