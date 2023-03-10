# 面向数据科学家的云计算和架构

> 原文：<https://web.archive.org/web/20230101103400/https://www.datacamp.com/blog/cloud-computing-and-architecture-for-data-scientists>

## 超越本地机器的可扩展数据科学

数据科学是一个代表许多重要事物的交集的术语。在我的一篇题为[什么是数据科学，数据科学家做什么？](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/what-is-data-science-does-data-scientist-do/?utm_source=datacamp&utm_medium=post&utm_content=postlink&utm_campaign=blog)，我讨论我称之为*的数据科学专业知识的支柱*。

这些专业支柱包括:

*   商业领域
*   概率与统计
*   计算机科学和软件编程
*   书面和口头交流

第三个所谓的支柱是对计算机科学和软件编程的理解。

虽然对于后起之秀的数据科学家来说，这可能不是显而易见的，但这一领域通常还包括 devops、云计算、数据管道、数据工程、查询不同类型数据库的专业知识、构建和部署生产软件解决方案等等。

此外，数据科学家需要培养扎实的编程技能，但他们在计算机科学、编程概念或一般生产软件架构和基础设施方面的教育和经验可能不如训练有素或经验丰富的软件工程师。当任何人开始学习数据科学时，他们会发现自己在本地计算机上安装 Python 和/或 R，然后在本地集成开发环境(IDE)中编写和执行代码，如 Jupyter Notebook 应用程序或 RStudio。

此外，随着高级分析变得越来越普遍，数据科学团队不断壮大，对提供洞察、预测分析、推荐系统等的协作解决方案的需求也越来越大。可重复的研究和笔记本工具与代码源代码控制相结合是协作解决方案的一部分，同时在另一方面利用基于云的在线协作工具和平台。

协作需求还扩展到包括数据科学团队以外的人员，特别是因为数据科学主要是为了实现业务目标而部署的。因此，数据科学项目的利益相关者可以包括高管、部门领导和其他数据团队成员，如架构师、数据工程师、分析师等。

本文旨在让数据科学家了解本地笔记本电脑或台式机之外的东西，特别是在将数据科学解决方案投入生产的背景下，或者在扩展您的计算能力方面。根据您对这些特定主题的体验，这些内容应该与所有技能水平的数据科学家相关。

我们开始吧！

## 云到底是什么？

啊，对了，臭名昭著且仍不为人所知的云。除了听起来非常假设和抽象，云实际上在它的预期意义上是非常具体的。在讨论云的概念之前，让我们先定义一些关键概念。

连接在一起共享资源的计算机被称为**网络**，互联网本身就是计算机网络的最大和最著名的例子。家庭网络是另一个例子，例如局域网(LAN)或 WiFi 服务集标识符(SSID ),其中连接了多台计算机，尽管它们小得多。这里描述的资源可以包括网页、媒体、数据存储、应用服务器、打印机等。

网络中的计算机通常被称为**节点**，它们使用定义良好的协议相互通信，如超文本传输协议(HTTP)、传输控制协议(TCP)/互联网协议(IP)等。这些通信可以用于状态更新、监控、请求/响应以及许多其他用途。

此外，计算机通常不位于内部，这意味着应用程序和数据通常托管在位于数据中心的计算机上。这些地方提供所有必要的基础设施，如电力、冷却、安全、灾难保护等。用于维护和成功运行公司或外部世界可访问的大量计算机。

因为随着时间的推移，计算机和存储变得相对便宜，所以现在许多解决方案采用多台协同工作的计算机，这些计算机的扩展成本不会太高，这与通过购买一台超级强大且非常昂贵的计算机来扩展解决方案相反。这种“协同工作”的一部分是为了确保即使其中一台计算机出现故障，解决方案也能继续自动运行，并且系统能够自动扩展以处理任何强加在系统上的负载。

Twitter、脸书、Instagram、Snapchat、网飞和 YouTube 是基于云的应用程序的完美例子，这些应用程序需要以这两种方式进行扩展。他们的应用程序完全“宕机”的可能性极小，而且他们还能够处理每天数百万的用户使用他们的平台。

当某一组计算机连接到同一个网络并一起工作来完成相同的任务或一组任务时，这被称为**集群**。一个集群可以被认为是一台单独的计算机，但是与一台单独的机器相比，它可以在性能、可用性和可伸缩性方面提供巨大的改进。这些好处将在本文后面讨论。

术语 ***分布式计算*** 或 ***分布式系统*** 是指为利用集群执行特定任务而编写的软件和系统，如 Hadoop、Spark 和 MapReduce。

最后，谈谈云的定义。除了上面描述的共享资源，其他重要的解决方案资源可以包括服务器、服务、微服务、网络等等。**云**描述了一方拥有、管理一组联网计算机和共享资源的情况，这些计算机和资源通常用于托管和提供基于软件的解决方案。根据这个定义，虽然互联网肯定被认为是一个网络，但它不是云，因为它不是由一方所有。

要深入了解云计算，并讨论创建可扩展软件和大数据架构的关键概念，请查看我关于该主题的三部分[深入系列](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/cloud-software-big-data-architecture-application-types-requirements-components/?utm_source=datacamp&utm_medium=post&utm_content=postlink&utm_campaign=blog)。

## 云中的数据科学

这篇文章已经足够深入地讨论了云计算和其他相关概念，希望能够阐明相关概念。如果您在这一点上对软件架构和工程的接触仅限于本地开发，您可能会奇怪为什么这些都与数据科学家有关。这是接下来要讨论的内容。

如果您熟悉数据科学流程，您会知道大多数数据科学工作流通常是在数据科学家的本地计算机上执行的。计算机上安装了各种语言，比如 Python 和 R，还有数据科学家喜欢的 IDE。另一个主要的开发环境设置是通过像 Anaconda 这样的包管理器或者通过手动安装单个包来安装相关的包。

一旦开发环境设置好并准备就绪，典型的数据科学工作流或过程就开始了，数据是大部分情况下唯一需要的东西。迭代工作流步骤通常包括:

*   获取数据
*   解析、管理、争论、转换和净化数据
*   分析和挖掘数据，例如探索性数据分析(EDA)、汇总统计，...
*   构建、验证和测试模型，例如预测、建议，...
    *   注:如果不构建模型，那么识别模式或趋势，生成可操作的见解，提取有用的信息，创建报告，等等。在这里，本教程将考虑“创建可交付成果”的任何一种情况。
*   调整和优化模型或交付物

然而，有时在自己的本地开发环境中执行所有数据科学或大数据相关任务并不实际或不可取。以下是一些主要原因:

*   数据集太大，不适合开发环境的系统内存(RAM)用于模型训练或其他分析
*   开发环境的处理能力(CPU)无法在合理或足够的时间内执行任务，或者根本无法执行任务
*   可交付成果需要部署到生产环境中，并可能作为一个组件合并到一个更大的应用程序中(例如，web 应用程序，SaaS 平台，...)
*   最好使用更快、更强大的机器(CPU，RAM，...)并且不会给本地开发机器带来必要的负载

当这些情况出现时，有多种选择。人们通常不使用数据科学家的本地开发机器，而是将计算工作卸载到本地机器或基于云的虚拟机(例如，AWS EC2、AWS Elastic Beanstalk)。使用虚拟机和自动扩展虚拟机集群的好处是，它们可以根据需要启动和丢弃，还可以定制以满足计算和数据存储需求。

在将可交付成果部署到生产环境中作为更大的应用程序或数据管道的一部分的情况下，有许多选项和挑战需要考虑。对此的进一步讨论超出了本文的范围。

除了定制开发的基于云或生产数据科学的解决方案和工具之外，非常著名的供应商也提供了许多基于云和服务的产品，这些产品通常可以与 Jupyter 等笔记本工具配合使用。这些主要作为大数据、机器学习和人工智能 API 提供，包括 AWS 人工智能平台、Databricks、谷歌云平台 Datalab 和机器学习等选项。

有关生产与开发中的数据科学和高级分析的更详细、更深入的讨论，包括对语言、包、框架和平台的建议，请查看我关于该主题的三部分[系列](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/cloud-software-big-data-architecture-application-types-requirements-components/?utm_source=datacamp&utm_medium=post&utm_content=postlink&utm_campaign=blog)。我的可扩展软件和大数据架构[系列](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/cloud-software-big-data-architecture-application-types-requirements-components/?utm_source=datacamp&utm_medium=post&utm_content=postlink&utm_campaign=blog)也是对云计算的一个很好的补充。

## 软件架构和质量属性

软件架构包括设计一个软件系统，通常基于云，代表一个产品、服务或基于任务的计算系统。你可能也听说过术语*系统架构*或*软件架构*，这两个术语的意思差不多。

设计软件架构的一部分是选择适当的编程语言和技术(也称为堆栈)、组件、包、框架、平台等等。这可能需要很多考虑，尤其是围绕系统的预期目的和任何其他重要的权衡。软件架构的这一方面需要一个人，比如软件架构师，随着时间的推移而获得的技能、知识和经验。

系统和软件架构和工程的另一个关键方面是所谓的[质量属性](https://web.archive.org/web/20220705013840/https://en.wikipedia.org/wiki/List_of_system_quality_attributes)或[非功能需求](https://web.archive.org/web/20220705013840/https://en.wikipedia.org/wiki/Non-functional_requirement)。对于现实世界的生产解决方案来说尤其如此。

非功能性需求通常包括以下内容:

*   有效性
*   表演
*   可靠性
*   可扩展性(向上和向外)
*   展开性
*   可用性
*   模块性
*   复用性

在本文中，您将简要了解其中最重要的四个方面，即可用性、性能、可靠性和可伸缩性。请注意，讨论是高层次的，并不涉及这些质量属性的基于度量的定义或需求。

**可用性**顾名思义，系统是可用的，或者换句话说，系统正常运行。这可能意味着很多事情，并且也严重依赖于可靠性和可伸缩性。“正常启动和运行”意味着系统能够按照预期的方式在需要的时候正常工作。这可以是终端用户尝试使用系统，例如脸书或网飞，或者可以是一组用于处理数据的基于云的服务。

**可靠性**是一个术语，表示系统正常运行和工作而不出现故障或错误的能力。一个系统越能以这种方式运行，这个系统的容错能力就越强。因为很难事先想到并测试所有可能的使用和边缘情况，所以很难实现 100%的可靠性。此外，失败的原因有很多，包括代码错误、环境问题和有限的资源(CPU、RAM、磁盘内存，...)是一些主要的罪魁祸首。

**性能**是一个术语，用来描述系统执行任务的速度，或者换一种方式来思考，就是系统执行一个特定任务所花费的时间。以 YouTube 为例。您希望在观看视频时，视频会在合理的时间内加载并开始播放。谷歌让 YouTube 的性能越好，视频加载和开始播放的速度就越快，YouTube 的用户就越高兴，他们放弃这个应用程序的可能性就越小。相反，如果 YouTube 运行速度非常慢，以至于不值得受益，因此人们停止使用它。幸运的是，大多数时候是前者，而不是后者。

最后，**可扩展性**对于某些应用程序来说至关重要，它是一个术语，用来表示系统在系统负载不断增加的情况下保持一定性能水平(如上所述，也是高水平)的能力。负载是一个术语，用来表示对系统的并发或同时请求的数量。

需要可伸缩性的一个很好的例子是当一个受欢迎的运动队或表演音乐艺术家的门票第一次出售时。根据受欢迎程度的不同，在 Ticketmaster 这样的网络应用程序上购票的并发请求数量在门票首次发售时可能会达到数十万。根据系统的扩展能力，这可能会大大降低其性能，也可能会导致系统完全关闭。这两种情况都不好。

为了满足这一要求，使用了一些技术来纵向扩展或横向扩展系统。向上扩展是指系统中的计算设备被更强大的(CPU、更多内核，...)和具有更大资源(如系统内存或 RAM)的可靠机器。像这样的机器可能很贵。

另一方面，横向扩展是指使用低成本的商用机器，这些机器单独使用时功能不是特别强大，但是作为一个组使用时，能够处理系统上的负载。由于使用这种技术的解决方案需要多台计算机，因此设置系统来自动处理一台或多台计算机(节点)出现故障或崩溃(故障转移)等情况非常重要。

## 结论

希望这篇文章有助于阐明数据科学在本地开发之外的许多重要方面，以及现实世界的生产解决方案。当处理生产数据解决方案或需要额外的计算能力和资源时，理解基于云的计算和架构概念非常重要。

请在下面的评论中分享你的想法。如果你想了解更多，你可以在 Twitter 上关注 [@innoarchitech](https://web.archive.org/web/20220705013840/https://twitter.com/innoarchitech) ，注册 InnoArchiTech [简讯](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/newsletter/?utm_source=datacamp&utm_medium=bio&utm_content=newslink&utm_campaign=guest)，看看 InnoArchiTech [博客](https://web.archive.org/web/20220705013840/https://www.innoarchitech.com/?utm_source=datacamp&utm_medium=bio&utm_content=homelink&utm_campaign=guest)。也可以看看我的目标驱动的人工智能和机器学习[课](https://web.archive.org/web/20220705013840/http://skl.sh/2sEOYGT)。