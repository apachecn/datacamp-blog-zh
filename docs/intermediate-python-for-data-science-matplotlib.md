# 用于数据科学的中级 Python:Matplotlib

> 原文：<https://web.archive.org/web/20230101103415/https://www.datacamp.com/blog/intermediate-python-for-data-science-matplotlib>

## 课程摘录:面向数据科学的中级 Python-Matplotlib

*下面是摘自[数据科学中级 Python 课程](https://web.archive.org/web/20220817160401/https://www.datacamp.com/courses/intermediate-python-for-data-science/)第一章的视频和文字记录。[这里的](https://web.archive.org/web/20220817160401/https://www.datacamp.com/courses/intermediate-python-for-data-science/)是全章，包括互动练习。*

## 使用 matplotlib 的基本绘图

[https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/SiCyTcudoSE](https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/SiCyTcudoSE)

大家好，我叫菲利普，是 DataCamp 的一名数据科学家。在这个中级 Python 课程中，您将进一步提高数据科学的 [Python 技能](https://web.archive.org/web/20220817160401/https://www.datacamp.com/learn/python)。您将学习如何可视化数据和在新的数据结构中存储数据。在这个过程中，您将掌握控制结构，您将需要这些结构来定制您的脚本和算法的流程。我们将以一个案例研究来结束这一章，在这个案例中，你将把你所学到的一切融合在一起，来解决一个很酷的问题。

这第一章是关于[数据可视化](https://web.archive.org/web/20220817160401/https://www.datacamp.com/data-courses/data-visualization-courses)，这是数据分析非常重要的一部分。首先，您将持续使用它来探索您的数据集。你对数据理解得越好，你就能更好地获得洞察力。一旦你发现了这些洞见，同样，你将需要视觉化来与其他人分享你宝贵的洞见。举个例子，看看这幅美丽的图。



它是由瑞典教授汉斯·罗斯林制造的。他关于全球发展的演讲已经被观看了数百万次。让它们如此吸引人的是，通过制作美丽的情节，他让数据讲述它们自己的故事。这里我们看到一个气泡图，每个气泡代表一个国家。泡沫越大，这个国家的人口就越多，所以这里最大的两个泡沫是中国和印度。

有两个轴。横轴显示以美元计的人均国内生产总值。纵轴显示预期寿命。我们清楚地看到，在人均 GDP 较高的国家，人们寿命更长。尽管如此，收入水平相同的国家之间的预期寿命仍存在巨大差异。

为什么我要告诉你这些？嗯，因为到这一章结束的时候，你就能自己构建这个美丽的情节了。

Python 中有许多可视化包，但它们的鼻祖是`matplotlib`。您将需要它的子包`pyplot`。按照惯例，这个子包是作为`plt`导入的，就像这样。

对于我们的第一个例子，让我们试着了解一下世界人口的演变。我这里有一个年的列表，和一个相应人口的列表，以十亿为单位，pop。例如，在 1970 年，37 亿人生活在地球上。

为了将这些数据绘制成折线图，我们调用 plt.plot()并使用我们的两个列表作为参数。第一个参数对应于水平轴，第二个对应于垂直轴。你可能认为现在会弹出一个情节，但是 Python 非常懒惰。它将等待`**show()**`函数实际显示图形。这是因为在实际显示之前，您可能希望向绘图添加一些额外的成分，例如标题和标签定制。我稍后会再谈及此事。只要记住这一点:`**plot()**` 函数告诉 Python 要绘制什么以及如何绘制。`**show()**`实际显示情节。

当我们看我们的图时，我们看到横轴显示的是年份，纵轴显示的是人口数量。有四个数据点，Python 在它们之间画了一条线。1950 年，世界人口约为 25 亿。2010 年在 70 亿左右。因此，世界人口在 60 年里几乎增加了两倍，这相当可怕。如果人口继续这样增长会怎么样？世界会变得人口过剩吗？你会在练习中发现的。

让我先给你介绍另一种类型的图:散点图。要创建它，我们可以从之前的代码开始。不过，这一次，您将绘图函数改为散点图。生成的散点图简单地绘制了所有单个数据点；Python 不是用一条线把点连接起来。对于许多应用程序，散点图通常是比折线图更好的选择，所以请记住这个散点图函数。你也可以说这是一种更诚实的绘制数据的方式，因为你可以清楚地看到这个图仅仅基于四个数据点。

现在我们已经了解了`matplotlib`的基础知识，该轮到你构建一些令人敬畏的情节了！

```py
 # define a simple function
import matplotlib.pyplot as plt
year = [1950, 1970, 1990, 2010]
pop = [2.519, 3.692, 5.263, 6.972]
plt.plot(year, pop)
plt.show()

import matplotlib.pyplot as plt
year = [1950, 1970, 1990, 2010]
pop = [2.519, 3.692, 5.263, 6.972]
plt.scatter(year, pop)
plt.show() 
```

## 直方图

[https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/Pqu8md5rt-k](https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/Pqu8md5rt-k)

在这个视频中，我将介绍直方图。直方图是一种非常有助于探索数据的可视化形式。它可以帮助你了解变量的分布。为了了解它是如何工作的，想象一下 0 到 6 之间的 12 个值。我把它们放在这里的数字线上。要构建这些值的直方图，您可以将线分成相等的块，称为条块。假设你有 3 个箱子，每个箱子的宽度为 2。接下来，计算每个箱中有多少个数据点。第一个箱中有 4 个数据点，第二个箱中有 6 个数据点，第三个箱中有 2 个数据点。最后，为每个箱子画一条横线。条形的高度对应于落在该条柱中的数据点的数量。结果是一个直方图，它给我们一个关于 12 个值如何分布的很好的概述。大多数值都在中间，但是低于 2 的值比高于 4 的值多。

当然，`matplotlib`也能够构建直方图。和以前一样，你应该从导入`matplotlib`里面的`pyplot`包开始。接下来，您可以使用`**hist()**`功能。让我们打开它的文档。你可以指定很多参数，但这里的前两个是最重要的。`x`应该是您要建立直方图的数值列表。您可以使用第二个参数`bins`来告诉 Python 应该将数据分成多少个箱。基于这个数字，`**hist()**`将自动为所有的容器找到合适的边界，并计算每个容器中有多少个值。如果不指定`bins`参数，它将默认为 10。

因此，要生成您之前看到的直方图，让我们首先构建一个包含 12 个值的列表。接下来，您只需调用`**hist()**` 并将这个列表作为输入传递，因此它与参数`x`匹配。我还将`bins`参数指定为 3，这样这些值就被分成三个部分。如果您最终调用 show 函数，就会得到一个漂亮的直方图。直方图对于给出一个更大的图像非常有用。举个例子，看看这个所谓的人口金字塔。显示了欧洲联盟男性和女性的年龄分布。请注意，直方图翻转了 90 度；箱子现在是水平的。40 至 44 岁年龄组的人数最多，其中有 2000 万男性和 2000 万女性。他们就是所谓的婴儿潮一代。

这些是 2010 年的数据。你认为 2050 年会发生什么变化？让我们看一看。分布更加平坦，婴儿潮一代已经变老。眨眼间，你就可以很容易地看到人口统计将如何随着时间的推移而变化。这就是直方图在这里发挥作用的真正力量！现在开始练习，亲自用直方图做实验！

```py
 values = [0,0.6,1.4,1.6,2.2,2.5,2.6,3.2,3.5,3.9,4.2,6]
import matplotlib.pyplot as plt
plt.hist(values,bins=3)
plt.show() 
```

## 用户化

[https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/aS4WlOJQ4mQ](https://web.archive.org/web/20220817160401if_/https://www.youtube.com/embed/aS4WlOJQ4mQ)

创造情节是一回事。制作正确的情节，使信息非常清晰，是真正的挑战。对于每个可视化，您有许多选择。首先，有不同的情节类型。对于每个地块，您可以进行无限数量的定制。您可以更改颜色、形状、标签、轴等。选择取决于，第一，数据，第二，你想用这些数据讲述的故事。因为有这么多可能的定制，最好的学习方法是通过例子。

让我们从这个脚本中的代码开始，构建一个简单的线图。它类似于我们在第一个视频中创建的线图，但这一次年度和流行列表包含更多数据，包括联合国预测的 2100 年前的预测。如果我们运行这个脚本，我们已经得到了一个非常好的图:它显示了正在发生的人口爆炸，将在本世纪末放缓。

但是有些东西是可以改进的。首先，我们应该更清楚地显示哪些数据，尤其是对于第一次看到图表的人。第二，这个情节确实需要引起人们对人口爆炸的注意。你需要做的第一件事就是给你的坐标轴贴上标签。让我们通过添加`xlabel` `()`和`ylabel` `() `函数来实现这一点。作为输入，我们传递应该放在轴旁边的字符串。确保在调用`**show()**`方法之前调用这些函数，否则您的定制将不会显示。如果我们再次运行脚本，这一次轴被注释。我们还将使用标题功能为我们的图添加一个标题。我们通过实际的标题，“世界人口预测”，作为一个论点。还有就是标题！

因此，使用`xlabel`、`ylabel`、和`title`，我们可以给读者更多关于图中数据的信息:现在他们至少可以说出图是关于什么的。为了正确看待人口增长，我想让 y 轴从零开始。您可以使用`**`yticks` ()**` 功能来完成此操作。第一个输入是一个列表，在这个例子中，数字从 0 到 10，间隔为 2。如果我们运行这个，图将会改变:曲线上移。很明显，在 1950 年，这个星球上已经有大约 25 亿人了。

接下来，为了清楚地表明我们在谈论十亿，我们可以向`yticks()`函数添加第二个参数，这是一个包含刻度显示名称的列表。该列表应该与第一个列表的长度相同。滴答 0 得到名称 0，滴答 2 得到名称 2B，滴答 4 得到名称 4B，以此类推。顺便说一下，B 在这里代表十亿。如果我们运行这个版本的脚本，标签会相应地改变，太好了。

最后，让我们添加一些历史数据来强调过去 60 年的人口爆炸。在维基百科上，我找到了 1800 年、1850 年和 1900 年的世界人口数据。我可以把它们写成列表的形式，用加号把它们添加到列表`pop`和`year`中。如果我现在再次运行脚本，三个数据点被添加到图形中，给出了一个更完整的图像。现在，这就是你如何把一个普通的线条图变成一个有清晰故事可讲的视觉效果！现在交给你了。开始练习，逐步定制世界发展图，成为下一个汉斯·罗斯林！

```py
 import matplotlib.pyplot as plt
import pandas as pd
year = list(range(1950, 2101))
pop = [2.53,2.57,2.62,2.67,2.71,2.76,2.81,2.86,2.92,2.97,3.03,3.08,3.14,3.2,3.26,3.33,3.4,3.47,3.54,3.62,3.69,3.77,3.84,3.92,4.,4.07,4.15,4.22,4.3,4.37,4.45,4.53,4.61,4.69,4.78,4.86,4.95,5.05,5.14,5.23,5.32,5.41,5.49,5.58,5.66,5.74,5.82,5.9,5.98,6.05,6.13,6.2,6.28,6.36,6.44,6.51,6.59,6.67,6.75,6.83,6.92,7.,7.08,7.16,7.24,7.32,7.4,7.48,7.56,7.64,7.72,7.79,7.87,7.94,8.01,8.08,8.15,8.22,8.29,8.36,8.42,8.49,8.56,8.62,8.68,8.74,8.8,8.86,8.92,8.98,9.04,9.09,9.15,9.2,9.26,9.31,9.36,9.41,9.46,9.5,9.55,9.6,9.64,9.68,9.73,9.77,9.81,9.85,9.88,9.92,9.96,9.99,10.03,10.06,10.09,10.13,10.16,10.19,10.22,10.25,10.28,10.31,10.33,10.36,10.38,10.41,10.43,10.46,10.48,10.5,10.52,10.55,10.57,10.59,10.61,10.63,10.65,10.66,10.68,10.7,10.72,10.73,10.75,10.77,10.78,10.79,10.81,10.82,10.83,10.84,10.85]
pop = [1,1.262,1.650] + pop
year = [1800,1850,1900] + year
plt.plot(year, pop)
plt.xlabel('Year')
plt.ylabel('Population')
plt.title('World Population Projections')
plt.yticks([0,2,4,6,8,10],['0','2B','4B','6B','8B','10B'])
plt.show() 
```

