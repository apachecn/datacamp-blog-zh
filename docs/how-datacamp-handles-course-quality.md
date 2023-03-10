# DataCamp 如何处理课程质量

> 原文：<https://web.archive.org/web/20221129045010/https://www.datacamp.com/blog/how-datacamp-handles-course-quality>

在 DataCamp，我们为拥有学习数据科学的最佳平台和最佳课程而自豪。为此，我们付出了很大的努力，以确保每项练习既有教育意义，又令人愉快。课程启动后，我们并不认为它是完整的:启动只是数据收集的开始。每当学生在课程中尝试一个练习时，我们都会捕捉数据点，例如他们尝试了多少次来解决这个练习，以及他们是否需要通过询问提示或解决方案来获得帮助。通过汇总所有学生的数据，我们可以了解一个练习的难度。此外，学生可以从一颗星到五颗星对练习进行评级，并向我们提供反馈，让我们知道练习的受欢迎程度。

我们的内容质量团队与教师合作，根据这些数据改进课程。这有各种各样的形式，因为很多事情都可能在练习中出错。

有时候，小事情会让很多学生心烦意乱。在[数据科学工具箱(第一部分)](https://web.archive.org/web/20220817160804/https://www.datacamp.com/courses/python-data-science-toolbox-part-1)中，学生们学习如何使用基于 J.R.R .托尔金的《指环王》三部曲中的《指环王》的数据集编写 Python lambda 函数。不幸的是，数据集遗漏了甘道夫和皮聘。我们的学生很有理由抱怨，所以我们倾听并解决了问题。

![](img/b894bd0ec3fbe7342ffcf99d0c356d52.png)

分析许多练习的反馈可以揭示学生的误解模式。许多数据分析以矩形形式保存数据，每行是一些记录，每列是属于该记录的一个值。例如，每行可以对应一个人，列可以是他们的名字、身高和他们最喜欢的颜色。

一个真正常见的数据操作实践是过滤矩形数据的行。教师可能会写下这样的指令:

*过滤数据集，删除身高低于 170cm* 的行。

这是可以的，但是大多数统计软件，包括 R 的 dplyr 包和 Python 的 Pandas 包，让你通过指定你想要保留的东西来过滤数据集。如果指令以下列方式重写:

*过滤数据集，保留身高超过 170cm 的行*。

然后，指令与代码的工作方式相匹配，避免了学生的困惑。对于要求学生熟悉数据操作的高级课程来说，这种措辞不是问题。在我们的[熊猫基金会](https://web.archive.org/web/20220817160804/https://www.datacamp.com/courses/pandas-foundations)课程中，我们发现许多学生都在努力解决这个问题，并改变了语言。

所有 DataCamp 练习都使用我们的内容工程团队开发的软件自动评分。如果学生答错了，这允许他们得到即时的智能反馈。这可能是我们平台最大的特点。最难的部分之一是预测学生将会做错什么，以便给他们好的建议，告诉他们下次应该做什么。这意味着有时一个正确的解决方案会被标记为不正确。出现这种情况，学生真的很讨厌。有一次，一名学生抱怨说:

![](img/223e460f104b1fb74a8d6ca42e59f05a.png)

在我们的 R 课程中的[聚类分析中，许多学生发现，尽管一个练习的建议解决方案使用了众所周知的 min()函数来计算最小值，但还有一个更简单、更优雅的解决方案，它使用了鲜为人知的并行最小值函数 pmin()。](https://web.archive.org/web/20220817160804/https://www.datacamp.com/courses/cluster-analysis-in-r)

![](img/e6b44dbdc6a86608872146be8b02d82d.png)

最初，这个练习只允许一个解决方案，但是基于学生们的巧妙想法，两个解决方案现在都被接受了。内容工程团队开发 DataCamp 反馈系统的目标之一是提高评分的灵活性，允许学生以自己的方式解决问题。

学生在使用我们的自动反馈时可能遇到的另一个挫折是，在做练习时重复看到相同的反馈。原理如下图所示，要求学生创建一个包含三个元素的 Python 数组。

![](img/8aa0ec2d05dd1e7aa598a1cc36fc2bae.png)

通过提供更细致的反馈来解决学生答案中的具体问题，我们可以提供更积极的学习体验。反馈改善的结果令人鼓舞。在我们的[中级 Python for Data Science](https://web.archive.org/web/20220817160804/https://www.datacamp.com/courses/intermediate-python-for-data-science) 课程的一个练习中，切换到粒度反馈意味着学生不止一次看到相同反馈消息的比例从大约 65%下降到 10%以下。

![](img/068b4128ed087dc0ec2b76b7077a53e8.png)

不止一次看到相同反馈信息的用户百分比是我们对所有练习和课程进行监控的指标。结合课程的受欢迎程度，我们创建了一种数据驱动的方式，以最具影响力的方式不断改善学习体验。

我们今年年底的目标是，对于所有课程中最受欢迎的那一半，每门课程所有练习的平均重复反馈百分比低于 30%。

我们将继续在学生可以在 DataCamp 上学习的所有技术中添加这些改进。在内部，我们还改进了用于创建反馈和分析学生提交内容的工具，以确保我们不断改善所有当前和未来内容的学习体验。

练习可能会出错的地方还有很多，但我希望这能给你一些鼓励，DataCamp 倾听学生的反馈，并不断努力提高学生对我们课程的满意度。