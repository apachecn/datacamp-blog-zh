# 用 MLOps 操作机器学习

> 原文：<https://web.archive.org/web/20221129054701/https://www.datacamp.com/blog/operationalizing-machine-learning-with-mlops>

[![](img/0ff2c6cffdaef87fef7e778c14cb2dd2.png)](https://web.archive.org/web/20220703052910/https://www.datacamp.com/community/podcast/operationalizing-machine-learning-with-mlops)

[https://web.archive.org/web/20220703052910if_/https://embed.podcasts.apple.com/us/podcast/67-operationalizing-machine-learning-with-mlops/id1336150688?i=1000530032315](https://web.archive.org/web/20220703052910if_/https://embed.podcasts.apple.com/us/podcast/67-operationalizing-machine-learning-with-mlops/id1336150688?i=1000530032315)

DataCamp 播客 DataFramed 的主持人阿德尔·内梅最近采访了 WhyLabs 的首席执行官兼联合创始人阿莱西娅·维森吉奇。

## [介绍阿莱西娅·维森吉奇](https://web.archive.org/web/20220703052910/https://www.datacamp.com/community/podcast/operationalizing-machine-learning-with-mlops)

Adel Nehme:大家好，我是来自 DataCamp 的 Adel Nehme，欢迎来到 DataFramed，这是一个涵盖所有数据及其对世界各地组织的影响的播客。你知道，在过去的几年里，我们肯定看到了一件事的兴起，即实现机器学习模型和生产的迫切重要性。

Adel Nehme:新冠肺炎让我们看到了概念或数据漂移，许多模型在生产中崩溃，这是因为在强制锁定后产生的数据不断变化的性质以及由此产生的完全不同的习惯。因此，我们已经看到了描述操作化、监控和从机器学习和生产中提取价值的新方法和方式的爆炸。其中最主要的是 MLOps。

阿黛尔·奈姆:这就是为什么我今天非常兴奋，因为今天的节目中有阿莱西娅·维森吉奇。Alyssa 是 WhyLabs 的首席执行官和联合创始人，why labs 是一家人工智能观察公司，致力于建立人工智能和人类操作员之间的界面。在加入 WhyLabs 之前，Alyssa 是艾伦人工智能研究所(Allen Institute for AI)的常驻首席技术官，她在那里评估人工智能研究最新进展的商业潜力。在她的职业生涯早期，Alyssa 在亚马逊工作了九年，领导机器学习的采用和调整工作。她是亚马逊在柏林的第一个机器学习中心的创始成员。德国。

Adel Nehme: Alyssa 也是 RSquared AI 的创始人，这是一个由 1000 多名人工智能从业者组成的全球社区，致力于使人工智能技术变得强大并对所有人负责。在这一集中，Alyssa 和我讨论了数据团队面临的机器学习挑战，这些挑战刺激了对 MLOps 的需求；MLOps 与其他术语(如数据操作、模型操作和 AIOps)的交叉和区别；组织应如何以及何时开始其信封之旅；以及 MLOps 最重要的组件是什么等等。如果你想查看播客的前几集并显示注释，请务必前往[www.datacamp.com/community/podcast](https://web.archive.org/web/20220703052910/https://www.datacamp.com/community/podcast)。

阿黛尔·尼姆:艾丽莎，很高兴你能来参加我们的节目。

阿莱西娅·维森吉奇:当然。我也很兴奋能参加这个节目，阿黛尔。谢谢你邀请我。

Adel Nehme:我很高兴能与您谈论 MLOps，组织如何开始使用它，您启动 WhyLabs 的经验等等。但在此之前，你能简单介绍一下你的背景和你是如何进入数据空间的吗？

阿莱西娅·维森吉奇:所以我的旅程从华盛顿大学开始，我在那里学习应用数学。2008 年我本科毕业，那段时间真的很搞笑；很多和现在类似的未知，也许。我真的很想去读研并获得博士学位，但由于不确定的时期，我决定在进入这个行业之前先了解一下这个行业。所以我加入了亚马逊，这在 2008 年还是一家不太知名的公司。其实我奶奶评价我去了一家连店都没有的书店上班。

阿莱西娅·维森吉奇:但有趣的是，那是在一个非常有趣的时期。所以公司发展迅速。这项技术发展迅速。因此，我非常幸运地在整个 DevOps 文化刚刚在公司爆发的时候加入了亚马逊。我在一个名为平台卓越的小组工作，在那里我确保网站快速运行。它没有异常，没有问题。

阿莱西娅·维森吉奇:在我职业生涯的中途，我一直在寻找机会回归应用数学的根基。2013 年，当亚马逊开始他们的第一个 R&D，机器学习 R&D 的时候。因此，他们开始在业务部门内部创建 R&D 团队。我加入了其中的一个，然后我搬到了德国的柏林，去帮助这个组织播种，帮助成立这个组织。

阿莱西娅·维森吉奇:该小组专注于在公司内部部署机器学习应用程序。所以我很幸运在正确的时间出现在了正确的地方。有很多优秀的机器学习科学家加入了这个团队。我们的任务是将机器学习应用程序构建和部署到供应链个性化、仓库等等。

阿莱西娅·维森吉奇:所以我有机会成为机器学习工程和商业之间的桥梁。在这个角色中，由于我之前的 DevOps 经验，我也是一个经常携带寻呼机的勇敢的人，支持我们部署的机器学习应用程序。因此，我很高兴也很冒险地去感受一下在非常大的部署的早期运行机器学习产品是什么感觉。

阿莱西娅·维森吉奇:我运营过的最大一次部署是需求预测渠道，它为亚马逊全球四分之一的零售产生了每日预测，这令人难以置信。我们正在为亚马逊上的数亿件产品创建预测，并在生产中支持它是一项巨大的努力。这就是我进入这个空间的方式。

## 什么是 MLOps？

Adel Nehme:我很高兴能与您讨论所有关于 MLOps 的最新信息。因此，虽然 MLOps 是一个相对较新的术语，但它已经成为当今许多组织关注的焦点。我们目前正处于可以被描述为炒作阶段的 MLOps。我想我们讨论一下什么是 MLOps，什么不是。

Adel Nehme:但首先，我想做的是搭建舞台，阐明 MLOps 的动机及其重要性。所以你已经在机器学习领域呆了很长时间了。您能否向我们介绍一下数据团队在大规模部署机器学习模型时面临的具体挑战，这些挑战真正刺激了对 MLS ops 的需求？

阿莱西娅·维森吉奇:这是进入主题的一个奇妙的入口。因此，首先，作为铺垫，我想后退一步，想想这个术语是从哪里来的，不出所料，它反映了我们在传统软件中的 DevOps 文化。DevOps 的核心是持续集成、持续交付和持续部署。

阿莱西娅·维森吉奇:当我说这些术语时，突出的是连续的，术语在继续。在这里，它真正的意思是，我们希望软件对客户来说是一种持续的体验，持续和一致的体验，这似乎非常简单，也是软件的一个基本定义。但是在机器学习的世界里，这才刚刚确立。

阿莱西娅·维森吉奇:所以在机器学习领域，当我们在学术界研究机器学习模型时，通常我们会选取一个数据集，然后对其进行迭代，以得出越来越好的模型。在行业中，您有一个模型，它部署在生产环境中，每天都会遇到越来越新的数据，它需要为用户提供连续、一致的体验。因此，MLOps 真正关心的是工具文化过程，它有助于确保机器学习模型持续提供它们被设计来提供的体验。

Adel Nehme:好的。太好了。因此，在过去几年中，有相当多的不同术语试图在机器学习工作术语中捕捉数据的操作方面，如 DataOps、AIOps 以及现在的 MLOps。你介意给我们介绍一下这些术语是如何区别和交叉的吗？

阿莱西娅·维森吉奇:是的，我们的行业正被新术语淹没。为了回答你的问题，我们先来看看 AIOps 和 MLOps 的区别。那是最容易定义的一个。因此，AIOps 是一个用来描述 AI 和机器学习技术的术语，这些技术应用于常见的 IT 问题。也就是说，自动化异常检测和点击流数据，或者自动化传统意义上的监控和警报聚合。因此，像 Datadog 和 Splunk 这样的公司正在应用人工智能和机器学习日志数据，这些数据是他们收集来识别异常的机器日志数据。

阿莱西娅·维森吉奇:MLOps，尽管只有 AI 和 ML 的区别。我不知道这些术语是如何变得如此相似又如此不同的。MLOps 是一套技术，不一定是与人工智能和机器学习相关的技术，而是用于操作机器学习和人工智能应用的技术。

阿莱西娅·维森吉奇:这些技术可能是数据版本化、可再生数据管道、数据记录和监控等等。所以 AIOps 和 MLOps 是非常不同的东西。现在，如果我们讨论 DataOps 与 MLOps，差异就不那么明显了。因此，DataOps 通常专注于数据管道、数据版本、数据仓库和数据稳定性，而 MLOps 则专注于机器学习管道和机器学习应用。

阿莱西娅·维森吉奇:现在，机器学习管道面临的挑战基本上是数据管道。因此，数据操作的开始和结束位置以及数据操作的开始和结束位置仍然是一个灰色区域。

Adel Nehme:好的，太棒了。总之，如果我错了，请纠正我，MLOps 可以被视为一套工具、实践和技术，可确保机器学习系统的可靠和可扩展部署，类似于软件工程领域的 DevOps。对吗？

阿莱西娅·维森吉奇:是的，我认为这是一个很好的定义。我还会把文化加入其中。所以工具、实践、技术、心态或文化。

#### 构成成功的 MLOps 实践的关键焦点领域是什么？

Adel Nehme:是的，我很高兴能和你谈论文化。众所周知，这是充分利用数据的组织与不充分利用数据的组织的真正区别。因此，我想重点介绍一些仍在涌现的最佳实践和 MLOps。你认为成功的 MLOps 实践有哪些原则、模式或重点领域？

阿莱西娅·维森吉奇:是的，我想回到我之前在 DevOps 实践中强调的术语或模式，持续交付、持续部署、持续集成的概念，这种模式基本上要求应用程序是一致的、可重复的、健壮的。因此，日复一日，机器学习模型为客户产生的体验需要持续和一致。

阿莱西娅·维森吉奇:这在机器学习领域相当具有挑战性，原因有几个。我认为最大的原因是机器学习应用，不像传统软件，它们不是异端。传统软件本质上是我们制定的一套规则，当客户来到这里，他们满足这些规则中的一条，他们就获得了某种体验。对于机器学习，规则是由机器学习模型训练的数据生成的。

阿莱西娅·维森吉奇:因此，机器学习模型本质上是通过查看数据来建立规则，而不是制定规则。这就产生了一些有趣的挑战。首先，数据真的动摇了体验。因此，机器学习模型的行为会有所不同，即使没有进行代码更改，即使没有进行配置更改，也没有进行部署。如果作为模型输入的数据不同，如果模式不同，那么体验就会不同。

阿莱西娅·维森吉奇:我最近听到的一个最喜欢的例子是语音识别软件，它部署在野外，在现实世界中，可以识别某些说出的单词或短语。当 COVID 开始工作，每个人都开始戴口罩时，软件开始工作得不太准确，比以前差得多，因为口罩有点盖住了你的嘴，这使得你的声音听起来不太清楚，这使得麦克风拾取你的声音不太清楚，这基本上打破了模型。

阿莱西娅·维森吉奇:对于机器学习应用程序来说，这是一种非常具体、非常独特的行为，因此进入应用程序的数据会改变模型。我认为，当你为成功的机器学习操作定义那些实践时，要记住这一点。总之，我想说的是，从对连续行为的渴望中融合出来的高级模式是可复制的，这对于机器学习应用程序来说是一种非常常见和重要的概念和模式。

阿莱西娅·维森吉奇:再现性意味着我在本地机器或开发环境中对一些数据进行了实验。我有一个很酷的模型。比我之前的型号要好。现在我想在不同的环境中重现它。我该怎么做？或者我让这个模型今天运行，施加某种行为，我如何确保它明天施加类似的行为？这就是再现性，这是一个重要的模式。

阿莱西娅·维森吉奇:然后我想到了稳健。因此，稳健性本质上意味着我的模型和产品正在生成预测，但 30%的用户对预测不满意，并不意味着我的模型失败了。对于我的模型，失败意味着什么，失败模式是什么，失败在概率系统中意味着什么？所以回答这些问题是健壮性模式的范畴。

阿莱西娅·维森吉奇:最后是透明度。所以你有一个数据管道，它处理千兆字节或兆兆字节的数据，预测出来了。你如何调查不受欢迎的模型行为？你如何解释这些预测？你如何调试正在做出的预测？透明度作为一种模式，可以捕捉到一些问题、工具、文化和机制。因此，我会强调再现性、健壮性和透明性这三个关键模式。

Adel Nehme:太棒了。所以在过去的几年里，我们看到了从实验到操作化的转变。你认为负责操作化的主要角色是什么？开发模型的是同一批数据科学家吗？是 it 工程师，像机器学习工程师这样的混合角色，还是像 MLOps 工程师这样的专家角色？

阿莱西娅·维森吉奇:是的，实际上最近有一个全新角色的发展，我认为在过去的三、四或六个月里，MLOps 工程师的角色已经确定下来了。所以我喜欢把所有参与构建和操作机器学习和人工智能应用的人都称为人工智能构建者。我认为其中有许多不同的角色。

阿莱西娅·维森吉奇:所以很明显，首先是研究人员建立模型，同时也是拥有专业知识的人定义问题的范围。因此，通常，如果我们在谈论个性化模型，那么它通常是营销团队。如果我们在谈论一个供应链应用，人工智能应用，它可能是在股票经理。因此，它从数据科学家和主题专家开始。随着模型的开发，模型的生命周期继续，通常会涉及到项目经理、工程师或工程团队。可能会有一个 QA 团队参与进来。

阿莱西娅·维森吉奇:最终，我认为模型的所有权一旦建立和部署，而不是生产，我认为历史上它一直由建立它的团队所有，所以是数据科学家和工程师的混合团队。我认为，今天我们看到了一个实际的 MLOps 工程师角色的出现，我们的 ML 工程师也参与进来，他们通常处理数据管道，实际上是模型的生产实现步骤。

阿莱西娅·维森吉奇:今天我看到了 MLOps 工程师的大量涌现。事实上，昨天，我为播客做了一点准备，我继续搜索了 MLOps 这只是我偶尔做的一件有趣的事情，看看就业市场上发生了什么。我发现有大量的公司试图雇用有 MLOps 经验的人，像 Peloton 和麦当劳这样的公司，传统的公司甚至不是因为人工智能而出名，但他们确实在内部部署了人工智能机器学习。因此，他们正在寻找这种类型的人，以便在机器学习模型投入生产后，从本质上维护它们。所以我认为这是我们开始看到的新的新兴角色。

#### 数据科学家正在变得越来越专业化吗？

Adel Nehme:那么你认为在这个意义上，数据科学家正在变得越来越专业化吗？

阿莱西娅·维森吉奇:我不知道我们是否能肯定地说。我看到这两种组织结构都很成功，因此 Stitch Fix 的 Eric Colson 是全栈数据科学家或全栈 ML 实践者学科的思想领袖之一，这基本上意味着就像全栈工程师一样。数据科学家能够建立模型，部署模型，操作模型，并拥有整个周期。我认为在许多组织中仍然是这种情况。

阿莱西娅·维森吉奇:但与此同时，我们确实看到了非常专业化的规则的平行，数据科学家是真正开发新技术的机器学习科学家，数据科学家开发关于数据的新技术，然后我们看到机器学习工程师通常生产或扩大机器学习应用。现在我们看到 MLOps 工程师。所以有迹象表明，这两者，我想是组织结构，都有自己的位置。我想说，我们还没有决定哪一个更好或更有效，或者两者都有空间。

## MLOps 采用

Adel Nehme:从这个意义上来说，鉴于 MLOps 仍处于发展阶段，您认为在 MLOps 作为一种实践和组织被广泛采用之前，我们还需要什么？

阿莱西娅·维森吉奇:是的。我认为我们还有很长的路要走。我认为采用的最大障碍之一是文化和对 MLOps 需求的理解，以及对工具、实践、流程和文化需求的理解，以便操作这项技术。通常，在与各种数据科学团队的交谈中，我仍然看到他们的思维方式在生产中止步不前。

阿莱西娅·维森吉奇:所以他们正在跑这场马拉松，它从获取数据、捕捉问题、构建模型、迭代、实验、生产开始，当模型投入生产时，它就结束了。这就是我们在组织中看到的最常见的想法，MLOps 是一种运动，本质上说，“看，你必须考虑你的模型后期制作会发生什么，因为这几乎是最重要的一步。”

阿莱西娅·维森吉奇:一旦模型投入生产，它就能提供价值或不提供价值，提供积极的客户体验或消极的客户体验。因此，思考后期制作会发生什么可能比之前的其他步骤更重要。所以我认为意识到这一点的重要性是最大的障碍之一。

阿莱西娅·维森吉奇:创造这种文化，帮助企业理解这是有必要的，因为许多组织仍在试图采用机器学习，试图推出他们的第一个机器学习模型。他们在这方面花费了大量的资源，雇佣了专业的数据科学家和机器学习科学家，他们真的很兴奋能够得到他们的第一个模型，但他们经常会惊讶地发现仍然需要更多的资源和更多的工作。所以我认为改变这种心态非常关键。

阿莱西娅·维森吉奇:我认为从技术角度来看，MLOps 作为一个软件类别，我认为我们仍然在技术方面搞清楚一些事情，我们正在搞清楚可解释性对运营模式意味着什么。我们如何利用一些来自学术界的可解释技术，从研究到运营方面的帮助。那么公平是另一个，公平和偏见，是另一个巨大的空间，仍然是一个巨大的研究领域。

阿莱西娅·维森吉奇:我想说的不是包容性，但有一些我们同意的指标，一些我们在公平和偏见领域没有同意的指标。因此，我们仍在弄清楚这意味着什么，以及公平和偏见如何在 MLOps 工具和 MLOps 流程中体现出来。当然，还有因果关系。所以大多数机器学习系统都不是因果的。这对运营意味着什么？

阿莱西娅·维森吉奇:因为当我们想到软件运营时，我们总是想到因果关系。随着机器学习系统不再像根本原因那样具有因果性，分析变得有些棘手，等等。因此，可解释性、公平性和因果性，我认为仍然在技术方面产生一些挑战，这些工具看起来像什么，我们如何确保这些工具能够正确地服务于理解机器学习模型的行为。

#### 工具堆栈的标准化

Adel Nehme:这真的很有见地。谢谢你。你在这里提到了工具堆栈。在分析方面，数据科学工具包似乎已经围绕开源编程、语言和工具(如 Python、Pandas、Scikit-learn 等)实现了标准化。你认为我们什么时候会在工具堆栈和 MLOps 领域实现标准化？

阿莱西娅·维森吉奇:我不确定规范堆栈是否有终结期。我认为我们正开始走向某种团体和组织，他们开始形成他们对规范堆栈的想法。其中一个组织是人工智能基础设施联盟(AI Infrastructure Alliance，简称 II ),我本人就是其中一员，也是它的忠实粉丝。这是一群创业公司，他们实际上正在建立一个基础设施联盟，或者为机器学习应用建立规范的堆栈。

阿莱西娅·维森吉奇:因此，不仅仅是 MLOps 需要一个规范的堆栈，而是一个用于构建、开发、部署和操作机器学习应用的规范堆栈。所以这是一个了不起的举动，我真的很高兴看到堆栈将会是什么样子，而不是一个剧透警报，因为你可以去人工智能基础设施联盟的网站，看看联盟是如何处理这个问题的。

阿莱西娅·维森吉奇:我想说，这不会是一个处方，你把这 10 个工具添加到你的过程中，然后你就可以走了，这是非常具体的用例；它具体到组织在他们采用机器学习和人工智能的旅程中处于什么位置；具体到什么规模，你运行的东西，等等。但我认为我们看到了一些积极的迹象，即出现了一套工具，或者我甚至可以说是一套实践，这些实践被广泛接受为您的组织中的必要实践，以便很好地实施机器学习操作。

#### 组织应该何时开始他们的 MLOps 之旅？

Adel Nehme:这太令人兴奋了。因此，如果您有一个蓝图来为组织提供如何以及何时开始的信息，您认为组织应该何时开始他们的 MLOps 之旅？如果你有一个蓝图，这个蓝图会是什么样的？

阿莱西娅·维森吉奇:越早越好。与此同时，他们开始采用和建立机器学习组织，采用机器学习技术。所以我会从定义几个主题开始，再次回到 DevOps，因为真的没有理由重新发明那些轮子。正如我提到的，我要说的是要考虑的重要主题，可再现性、透明度、稳健性，我还要将质量和所有权文化加入其中。

阿莱西娅·维森吉奇:当你开始开发机器学习应用程序时，这是你需要记住的五件事。这些是本组织应该尽快开始问自己的问题。然后，我会说，对于一个组织来说，一个很好的过程，一个轻量级的过程来制定他们自己的蓝图，就是从他们的 DevOps 团队开始，来制定这个组织已经为传统软件实施的所有活动、过程、机制，然后扩展他们的思维，以包括数据和包括机器学习非确定性概率应用。

阿莱西娅·维森吉奇:所以这意味着你应该为传统软件做传统软件的开发工作。然后，您应该拥有特定于理解数据过程的过程和工具，以及特定于理解模型的工具。这本身并不是一个蓝图，但是如果您经历这个过程，它将帮助您为您的组织和您的特定使用情形开发非常专业的蓝图。

Adel Nehme:现在，回到人的因素，您认为数据、文化和数据素养在促进环境扩展以及解决大规模部署机器学习模型的核心问题时有多重要？

阿莱西娅·维森吉奇:我认为数据文化和数据素养绝对是创造正确环境的关键，创造一个可以让我们说负责任地希望学习采用的环境。我这么说的原因是因为这很简单，当我们说机器学习时，很容易只考虑和专注于算法，并把数据视为理所当然。这是非常危险的，因为正如我们所知，正如我们看到的那种成为新闻的机器学习失败，大多数源于机器学习的不幸经历都来自于收集得很差的训练数据，很差的机器学习预测，这种预测会让不幸的经历一直出现在客户面前。

阿莱西娅·维森吉奇:更具体地说。我会说数据隐藏了偏见，数据隐藏了错误，数据隐藏了希望学习失败。如果我们不考虑数据，这些数据是如何收集的，谁带来了这些数据，谁是数据提供商，谁清理了这些数据，我们是否了解这些数据描述了我们客户的哪一部分，这些数据是否完整地描述了我们所有的客户，这些数据是否包含个人身份信息，等等。

阿莱西娅·维森吉奇:如果没有这种文化，也不了解他们知道你处理的数据有多有价值，但如果处理不当也会很危险，我认为机器学习在一家公司是不会成功的。说到这里，我真的很高兴听到 Andrew Ang 是如何看待数据文化的整个概念的。他在这个问题上确实直言不讳。他的很多演讲都侧重于鼓励数据科学家首先考虑他们的数据，模型是处理数据的第二种方式。

阿莱西娅·维森吉奇:我的一个好朋友，来自三元数据公司的乔·里斯也经营着一个播客，他是一个伟大的、直言不讳的人，来自数据工程领域，他将自己的经验与机器学习文化相结合，带来了许多有趣的见解，这些见解捕捉到了围绕数据的文化或缺乏文化如何影响学习采用的意愿。所以我建议听众去看看，我确信 Andrew Ang 是一个非常著名的，所以看看他最近的一些演讲中有很多关于数据文化的有趣信息和见解，然后三元数据的 Joe Reis 有很多关于数据文化和数据素养的有趣内容，

Adel Nehme: 100%。我们肯定会把这些内容包含在演出笔记中。现在，我想重点谈谈 WhyLabs 以及它如何融入 MLOps 工具堆栈，但在此之前，您如何描述 MLOps 中的当前工具空间？

阿莱西娅·维森吉奇:嗯，我想说工具领域正在迅速崛起。所以我可以看到两类工具。一类是提供某种机器学习构建模块的云提供商。因此，从数据流到数据仓库，再到扩展 Jupiter 笔记本电脑，这一切都是科学家们经常用来构建模型的。

阿莱西娅·维森吉奇:所以云提供商也开始增加工具来帮助你完成 MLOps。因此，用于测试、版本控制、监控机器学习应用程序和数据管道的工具。这是一个类别。第二类是一群初创公司，他们正在使用专门构建的工具来运行机器学习应用程序。因此，无论你作为一个组织处于旅程的哪个阶段，我想有两个大的选择值得关注:云提供商和初创公司。当您为组织的 MLOps 播种工具时，绝对不缺少尝试和考虑的选项。

## 为什么实验室

Adel Nehme:您能向我们介绍一下 WhyLabs 及其使命，以及它如何解决大规模部署 ML 模型的一些棘手问题吗？

阿莱西娅·维森吉奇:当然。所以 WhyLabs 是一家人工智能可观察性公司，我们的使命是在人工智能应用程序和人类操作员之间建立一个接口。因此，我们帮助人工智能建造者的是，确保他们的模型正在产生它们被建造来产生的影响。我具体指的是，我们有一个人工智能可观察性平台，它有助于确保模型不会意外失败，有助于确保模型在我们可以计算的最大程度上是公平的，有助于模型实现 ROI，并确保连续和自动化的交付。

Adel Nehme:太好了。您介意向我们介绍一下数据团队目前可以利用的一些特定功能吗？

阿莱西娅·维森吉奇:当然。实际上，我要做的是，我会专注于我们在社区中非常流行的开源库。该库名为 whylogs 和 whylogs 是什么，whylogs 是数据记录的标准，它是整个 MLOps 实践的基础。因此，在传统软件中，我们会在日志中捕获大量关于软件运行情况的信息。

阿莱西娅·维森吉奇:说到机器学习，你可以从传统日志中获取大量信息。然而，当涉及到流经管道并在每一步进行转换的数据时，传统上没有办法捕捉数据的样子以及它在每一步之间是如何变化的。所以 whylogs 可以帮你做到这一点。

阿莱西娅·维森吉奇:这是一个专门构建的机器学习日志库，由我们在 WhyLabs 的团队开源，旨在提供一种非常轻量级、可移植和可配置的方式来记录数据的统计属性以及批处理和流数据工作负载中的模型预测。因此，既然 whylogs 是一个开源库，它能让任何人做的就是捕获数据的统计属性，然后在此基础上建立测试、监控和警报，以识别数据漂移、数据偏差、数据异常值等情况，然后识别模型性能的退化。

## 行动呼吁

Adel Nehme:这太令人兴奋了。最后，阿莱西娅，在我们结束之前，你还有什么最后的行动呼吁吗？

阿莱西娅·维森吉奇:是的。首先，我很高兴能成为 MLOps 对话的一部分，我认为这个领域正在迅速崛起。因此，如果您的组织正在考虑建立一种 MLOps 文化，那么您这位听众会很乐意与您交谈。当我们在 WhyLabs 为数据记录建立 whylogs 标准时，每一个正在收听的人工智能从业者都会喜欢你的反馈和贡献。

阿莱西娅·维森吉奇:这需要一个村庄，需要每个人来定义像数据记录这样规范的东西的标准。因此，我将分享链接获得枢纽，并会喜欢反馈，贡献，问题，功能请求，获得帮助明星等。加入我们发起的为数据记录和 MLOps 建立标准的运动。

Adel Nehme:太棒了。阿莱西娅，非常感谢你参加今天的播客。

阿莱西娅·维森吉奇:谢谢你，阿黛尔。很高兴来到这里。

Adel Nehme:今天的 DataFramed 节目就到这里了。谢谢你和我们在一起。我非常喜欢 Alessya 对 MLOps 以及数据科学如何发展以满足组织需求的见解。如果你喜欢今天的节目，请务必在 iTunes 上留下评论。我们下一集将采访普华永道负责人工智能的主管玛丽亚·露丝安娜·阿申特。我希望它对你有用，我们希望下次能在 DataFramed 上看到你。