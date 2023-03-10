# 数据科学笔记本的过去、现在和未来

> 原文：<https://web.archive.org/web/20221129033335/https://www.datacamp.com/blog/the-past-present-and-future-of-the-data-science-notebook>

在过去 10 年的大部分时间里，笔记本电脑在数据科学领域已经很常见，每个数据科学家都使用过笔记本电脑。它们允许数据科学家通过快速环境创建、交互式输出和可按任意顺序执行的代码片段，快速进行实验和分享见解。

组织一直在数据科学和分析方面进行大量投资，投资的一个关键领域是允许数据科学家高效工作和快速试验数据的工具。笔记本电脑是这个问题的关键，也是我们今天在现代数据堆栈中看到的许多工具创新的组成部分。更重要的是，笔记本电脑还让公民数据科学家能够将数据见解民主化。

本文着眼于笔记本电脑的过去、现在和未来，以及笔记本电脑如何打破数据工作和协作的孤岛。

## 数据科学笔记本的历史

如今，几乎每个数据科学家都使用过笔记本，最流行的是 Jupyter 笔记本。然而，笔记本电脑在数据科学之前有着丰富的历史，可以追溯到 20 世纪 80 年代初。

### 识字编程的兴起

Donald Knuth 在 1984 年提出了识字编程，旨在作为一种方法来创建人类可读的程序。这个想法是用人类语言写出程序逻辑，用代码片段和宏编写成单独的注释，称为“WEB”。宏类似于用于教授计算机科学的伪代码。

然后，一个预处理器解析 WEB 来创建源代码(“tangle”)和文档(“weave”)。识字编程今天仍在使用，例如在 [Axiom](https://web.archive.org/web/20220810140007/http://www.axiom-developer.org/) 中，但识字编程中的关键思想导致了笔记本的发展，这些笔记本看起来与我们今天看到的非常相似。

### 早期笔记本

关键的早期笔记本是 Wolfram Mathematica 和 Maple，发布于 20 世纪 80 年代末。他们在前端运行，在后端运行内核。下图显示了一个使用 Mathematica 生成的 3D 图，带有我们今天在笔记本上继续看到的熟悉的`In[ ]`和`Out[ ]`符号。

![Mathematica notebook](img/09304a5810138dad83a49edc52a3dc5c.png)

早期的 Wolfrom Mathematica 笔记本

这些工具有细微的差别，例如使用 enter 而不是 shift + enter 来运行代码，以及数学运算显示方式的变化。然而，两者都包含了影响现代笔记本设计的思想。

广泛采用的一个关键障碍是成本，因为这些工具价格昂贵，并且需要许可证才能使用。这是一个贯穿整个行业的问题，导致了 1998 年[开源倡议](https://web.archive.org/web/20220810140007/https://en.wikipedia.org/wiki/Open_Source_Initiative)的诞生，它带来了我们今天使用的许多强大的免费工具(例如 Jupyter 笔记本！).

### 现代数据科学笔记本的早期基础

2001 年，IPython 和 SciPy 发布，2003 年 Matplotlib 紧随其后。SciPy 允许在 Python 中进行一系列科学计算，而 IPython 改善了终端中的用户体验，并增加了对分布式计算的支持。像今天一样，Matplotlib 允许在 Python 中轻松创建数据可视化。

直到 2005 年，这些开源工具(以及其他工具)才被纳入一个名为 SageMath 的工具中。这样做的目的是为 Mathematica 和 Maple 提供一个开源的替代方案，在其他科学开源工具的基础上进行组合和构建，并提供基于网络的功能，这些功能是当今现代笔记本的主要功能。

2011 年，IPython 发布了它的笔记本，在 web 应用程序前端和底层笔记本文档之间有着明显的区别。

![2011 IPython notebook](img/2e56470d409e38104dd2fa97c666986c.png)

IPython 笔记本

### 木星笔记本的诞生

Jupyter 于 2014 年从 IPython 中分离出来，引入了笔记本界面，并采用了 IPython 的其他语言无关部分。它以其支持的原始语言命名: **Ju** lia、 **Pyt** hon、 **R** 。Jupyter 笔记本现在是数据科学家的首选，无疑是当今使用最广泛的笔记本界面。

近年来的一个关键发展领域是将前端与内核分离的应用程序，这样用户可以在浏览器中访问前端，但内核在基于云的数据中心运行。这种工具的一个很好的例子是 [DataCamp Workspace](https://web.archive.org/web/20220810140007/https://www.datacamp.com/workspace) ，在这里您可以直接在浏览器中使用 Jupyter Notebook 实例。

![Jupyter Notebook](img/2c4432dd75a64641c5626e648ee789db.png)

data camp 工作区中的 JupyterLab

随着笔记本电脑越来越受欢迎，过去几年迎来了一波现代笔记本电脑界面的浪潮，使任何人都可以轻松地处理数据。在下一节中，我们将分析现代笔记本电脑如何打破数据处理的障碍。

## 现代数据科学笔记本如何增强公民数据科学家的能力

公民数据科学家的想法是由 [Gartner 在 2016 年提出的。](https://web.archive.org/web/20220810140007/https://www.gartner.com/en/documents/3534848)公民数据科学家拥有技术技能，但可能没有传统的数据科学、统计学或计算机科学背景。

随着数据科学越来越多地从一个领域发展成为解决业务问题的方法，公民数据科学家成为现代数据驱动型组织的代表。笔记本电脑是公民数据科学家的绝佳工具，因为它们允许快速实验和分享见解，几乎没有准入门槛。

尽管笔记本电脑在快速探索和分析数据集方面一直表现出色，但它们此前在协作和分享见解等领域一直表现不佳。在 2022 年，随着现代笔记本电脑和周围的生态系统遇到许多这些历史盲点，情况将不再如此。以下是笔记本电脑引领生产力、效率和协作进步的一些方式。

### 现代数据科学笔记本是协作的

现代协作工具的一个明显例子是谷歌文档。许多用户可以使用和编辑文档，尽管用户也可以控制谁可以进行编辑，谁只能提出评论。更改会定期保存，以防止灾难发生。

类似的技术现在也适用于配备了像 Deepnote 和 T2 这样的工具的笔记本电脑。多个用户可以编辑和运行笔记本，并留下评论。所有这些协作都是实时进行的，使得整个过程更加高效。

![DataCamp Workspace](img/d12a8a91cd66c00a0fb77ccf506f0aee.png)

data camp 工作空间中的协作

协作对于任何使用数据的人来说都是必不可少的。减少协作障碍还意味着通过共享知识和专业技能来减少数据孤岛。传统上，使用笔记本电脑进行协作可能会很慢，但现代数据堆栈快速高效。许多工具无缝集成到现有的技术堆栈中，这意味着用户可以使用他们习惯的工具工作，同时仍然可以与同事协作。

### 它们有助于数据洞察的民主化

与其他用户共享分析可能很困难，无论他们是业务利益相关者还是更有技术头脑的个人。过去，从业者通过电子邮件、Slack、演示或定制的 web 应用程序在 insights 中共享笔记本报告。

然而，现代笔记本电脑通过无缝共享笔记本电脑使见解民主化。例如， [IPyWidgets](https://web.archive.org/web/20220810140007/https://ipywidgets.readthedocs.io/en/latest/) 允许将交互式小部件添加到笔记本中，这意味着用户可以拖动滑块来改变图形，并与洞察力进行更多的交互。 [Binder](https://web.archive.org/web/20220810140007/https://mybinder.org/) 将回购变成托管的互动笔记本，这意味着任何人都可以共享和运行互动笔记本。[瞧](https://web.archive.org/web/20220810140007/https://blog.jupyter.org/and-voil%C3%A0-f6a2c08a4a93)把一个笔记本变成一个托管的网络应用程序，再次意味着用户可以完全互动，甚至不用看到所有的代码。 [Datacamp Workspace](https://web.archive.org/web/20220810140007/https://workspace-docs.datacamp.com/) 允许用户共享笔记本，并提供模板来为数据添加故事。

![sharing notebooks in DataCamp Workspace](img/9fed65f906e11b6d8d3d8a26b0b8cbb7.png)

在 DataCamp 工作区发布报告

### 他们可以弥合人才差距

数据科学既广又深:在许多不同的领域都有很多东西需要学习。成为一名 NLP 专家并不会让你成为一名伟大的数据工程师，甚至不会让你成为一个懂计算机视觉的人。

数据科学的不同子领域之间的关键联系是数据和基础设施。没有好的数据，模型就不会有好的表现。同样，如果没有支持模型开发和数据清理的基础设施，入门也是非常困难的。

对于公民数据科学家来说，不需要工程方面的技能。现代笔记本电脑允许任何人利用基于云的基础架构快速启动并运行。环境和包得到了很好的管理，大多数用户可以很容易地更新和修改。这确保了工程技能中的缺口不需要被填补，并且从业者可以花时间提供见解。

此外，大多数数据科学技术都与笔记本电脑完全兼容——可以训练模型，绘制 3D 图形，以及构建数据管道。这确保了公民数据科学家可以试验各种技术，并轻松地将结果传达给利益相关者或与其他技术用户共享代码。

### 现代笔记本与其他工具集成

我们已经了解了现代笔记本如何打破团队之间的数据孤岛，降低数据处理的门槛。然而，笔记本电脑历史上的另一个痛点是缺乏与数据科学工作流中使用的其他工具的集成。这方面的一个重要例子是 SQL。

历史上，从业者使用 Python 上的``mysql.connector``或 r 上的``DBI``等包建立数据库连接，这些包需要手动建立数据库连接，并手动输入数据访问的相关凭证。

另一方面，现代笔记本电脑提供了本地 SQL 支持。例如，使用 DataCamp Workspace，用户可以直接从 DataCamp 笔记本编辑器建立到数据库的安全连接，如 PostgreSQL、MySQL 和 Amazon Redshift。从集成数据库中提取的数据可以使用 R 或 Python 进行分析。

![Extracted Data in Workspace](img/23380b9f66f61dc6850c312f9eda1f36.png)

data camp 工作区中的 SQL 单元格

## 数据科学笔记本的未来

现代笔记本电脑是数据革命的核心。它使不同技能的从业者能够轻松地试验数据、分享见解，并在业务和数据团队之间架起一座桥梁。此外，笔记本电脑正在增强公民数据科学家的能力，引领当今组织内数据流畅的新浪潮。

像网飞这样的数据优先组织以其[笔记本创新](https://web.archive.org/web/20220810140007/https://netflixtechblog.com/notebook-innovation-591ee3221233)而闻名，因为笔记本是他们跨角色和团队处理数据的最受欢迎的工具。笔记本电脑的未来将由更高的灵活性、与剩余数据堆栈的更好集成以及强大的协作和共享来定义，以实现数据洞察的民主化。要了解有关笔记本电脑的更多信息，请查看以下资源:

*   [[播客]为现代数据分析师赋能](https://web.archive.org/web/20220810140007/https://www.datacamp.com/podcast/empowering-the-modern-data-analyst)
*   [【小抄】Jupyter 笔记本小抄](https://web.archive.org/web/20220810140007/https://www.datacamp.com/cheat-sheet/jupyter-notebook-cheat-sheet)
*   [【博文】R 用户笔记本](https://web.archive.org/web/20220810140007/https://www.datacamp.com/blog/notebooks-for-r-users)