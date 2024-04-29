# 第六章：如何应对编码挑战

本章涵盖了技术测验和编码挑战，这在技术面试中常见。

编码挑战是面试中最重要的部分。这部分可以由单个会话或多个会话组成。一些公司更喜欢将技术面试分为两部分：第一部分包括技术测验，而第二部分包括一个或多个编码挑战。在本章中，我们将详细讨论这两个主题：

+   技术测验

+   编码挑战

通过本章结束时，你应该能够规划自己的技术面试方法。你将知道如何处理面试中的关键时刻，面试官期望从你那里看到和听到什么，以及如何处理当你对答案/解决方案一无所知时的阻塞时刻。

# 技术测验

技术测验可以采用技术面试官问答的形式，也可以是现场测验。通常包含 20-40 个问题，耗时不到一小时。

当技术面试官进行这个过程时，你将需要提供自由回答，持续时间可能会有所不同（例如，30-45 分钟之间）。清晰、简洁、并且始终保持话题相关是很重要的。

通常，当技术面试官进行面试时，问题会被构建成需要你做出决定或选择的场景。例如，一个问题可能听起来像这样：*我们需要一个能够以极快的速度搜索数百万条记录并具有相当数量的误报的高效算法。你会为我们推荐什么？* 很可能，期望的答案是类似于，*我会考虑 Bloom 过滤器家族的算法*。如果你在以前的项目中遇到过类似的情况，那么你可以这样说：*我们在一个关于流数据的项目中遇到了相同的情况，我们决定采用 Bloom 过滤器算法*。

另一类问题旨在简单检查你的技术知识。这些问题不是在场景或项目的背景下提出的；例如，*你能告诉我 Java 中线程的生命周期状态是什么吗？* 期望的答案是，*在任何时刻，Java 线程可以处于以下状态之一：* **NEW**, **RUNNABLE,** **RUNNING**, **BLOCKED**, **SLEEP**, **WAITING**/**TIMED/WAITING**, *或* **TERMINATED**。

通常，回答技术问题是一个三步方法，如下图所示。首先，你应该理解问题。如果有任何疑问，就要求澄清。其次，你必须知道面试官希望你在回答中识别出几个关键词或要点。这就像一个清单。这意味着你必须了解应该在答案中突出的关键内容。第三，你只需要用逻辑和有意义的方式包装关键词/要点：

![图 5.1 - 处理技术测验的过程](img/Figure_5.1_B15403.jpg)

图 5.1 - 处理技术测验的过程

你将在*第六章**，面向对象编程*中看到大量例子。

一般来说，你的答案应该是技术性的，简洁但全面，并且自信地表达出来。害羞的人常见的错误是提供一个听起来像问题的答案。他们的语气就像他们对每个词都在询问确认。当你的答案听起来像一个问题时，面试官可能会告诉你直接给出答案而不要问他。

重要提示

当你只能部分回答一个问题时，不要急于回答或者说你不知道。尝试向面试官询问更多细节和/或 20 秒的思考时间。有时，这会帮助你提供一个不完整但还不错的答案。例如，面试官可能会问你，“Java 中检查异常和未检查异常的主要区别是什么？”如果你不知道区别，那么你可以给出一个答案，比如，“检查异常是 Exception 的子类，而未检查异常是 RuntimeException 的子类”。你实际上没有回答问题，但这比说“我不知道”要好！或者，你可以提出一个问题，比如，“您是指我们被迫捕获的异常吗？”通过这样做，你可能会从面试官那里得到更多细节。注意不要问得像，“您是指我们被迫捕获的异常和我们不被迫捕获的异常吗？”你可能会得到一个简短的答复，比如“是”。这对你没有帮助！另一方面，如果你真的不知道答案/解决方案，那么最好说“我不知道”。这不一定会对你不利，而试图用太多的废话来迷惑面试官肯定会对你不利。

有些公司更喜欢进行现场的多项选择测验。在这种情况下，没有人的帮助，你必须在固定的时间内完成测验（例如，30 分钟）。重要的是要尽量回答尽可能多的问题。如果你不知道一个问题，那就继续下一个。时间在流逝！在最后（最后的 2-3 分钟），你可以回过头来尝试回答那些你放弃的问题。

然而，有些平台不允许你在问题之间来回跳转。在这种情况下，当你不知道问题的答案时，你被迫冒险猜测答案。花费大量时间回答一个问题最终会导致得分不佳。理想情况下，你应该尽量在每个问题上花相同的时间。例如，如果你有 20 个问题要在 30 分钟内回答，那么你可以为每个问题分配 30/20 = 1.5 分钟。

接近技术测验（无论是什么类型的测验）的最佳技巧之一是进行几次“模拟”面试。找个朋友，让他扮演面试官的角色。把问题放在一个碗里，让他随机挑选一个一个来回答。回答问题，表现得就像你真的在面对真正的面试官一样。

# 编码挑战

编码挑战是任何技术面试的高潮。这是你展示所有编码技能的时刻。是时候证明你能胜任这份工作了。有工作和整洁的代码可以帮助你留下良好的印象。一个良好的印象可能弥补你在面试的其他阶段留下的空白。

编码挑战是一把双刃剑，可能会从计划中将你剔除，另一方面可能会让你尽管有其他缺点，但还是得到一个工作机会。

然而，这些编码挑战所特有的问题因为各种原因而非常困难。这些将在下一节中介绍。

## 编码挑战所特有的问题意在困难

你是否曾经见过一个特定于编码挑战阶段的问题，觉得奇怪、愚蠢，或者可能毫无意义，与真正的问题毫无关联？如果是的话，那么你见到了一个特别好的编码挑战阶段的问题。

为了更好地了解如何为这些问题做准备，了解它们的特点和要求是很重要的。所以，让我们来看一下它们：

+   **它们不是现实世界的问题**：通常，现实世界的问题需要大量时间来编码，因此它们不适合编码挑战。面试官会要求您解决可以在合理时间内解释和编码的问题，而这些问题通常不是现实世界的问题。

+   **它们可能相当愚蠢**：看到相当愚蠢的问题并不罕见，看起来就像它们是为了使您的生活变得更加复杂而创造的。它们似乎对某事没有用或没有目标。这是正常的，因为它们大多数时候不是现实世界的问题。

+   **它们相当复杂**：即使它们可以很快解决，它们也不容易！很可能，您将被要求编写一个方法或一个类，但这并不意味着它会很容易。通常，它们需要各种技巧，它们是令人费解的，和/或它们利用编程语言的不太知名的特性（例如，使用位操作）。

+   **解决方案并不明显**：由于它们相当复杂，这些问题的解决方案并不明显。不要指望立即找到解决方案！几乎没有人能做到！这些问题是特别设计的，以查看您如何处理无法立即看到解决方案的情况。这就是为什么您可能需要几个小时来解决它（通常是 1 到 3 个小时之间）。

+   **禁止常见的解决路径**：大多数时候，这样的问题有明确的条款，禁止使用常见的解决路径。例如，您可能会收到一个听起来像这样的问题：*编写一个方法，它可以在给定位置之间提取字符串的子字符串，而不使用 String#substring()这样的内置方法。*就像这个例子一样，有无数的例子。只需选择一个或多个内置的 Java 方法（例如，实用方法），可以在相对短的时间内实现，并加以阐述；例如，*编写一个方法，它可以做 X 而不使用 Y 这样的内置解决方案*。探索 API 源代码，参与开源项目，并练习这样的问题对于解决这样的问题非常有用。

+   **他们的目的是将您置于一组接受录用的候选人中**：这些编码挑战的难度被校准，以使您成为一组独特百分比的候选人。一些公司只向不到 5%的候选人提供工作机会。如果大多数候选人可以轻松解决某个特定问题，那么它将被替换。

重要提示

编码挑战特有的问题旨在具有挑战性，并通常按难度递增的顺序提出。很可能，要通过这些编码挑战，您的经验和编码技能是不够的。因此，如果尽管您的知识，您无法立即看到解决方案，不要感到沮丧。许多这样的问题旨在测试您解决不寻常情况的能力和测试您的编码技能。它们可能具有荒谬的条款和/或模糊的解决方案，利用编程语言的不常见特性。它们可能包含愚蠢的要求和/或虚假案例。只专注于如何解决它们，并始终遵守规则。

通常，一次编码挑战会足够面试官。然而，也有一些情况下，您可能需要通过两次甚至三次这样的挑战。关键是尽可能多地练习。下一节将向您展示如何处理一般的编码挑战问题。

## 解决编码挑战问题

在讨论解决编码挑战问题的过程之前，让我们快速为编码挑战设置一个可能的环境。主要有两个坐标定义了这个环境：面试官在编码挑战期间的存在和纸笔对电脑的方法。

### 面试官在编码挑战过程中的存在

最常见的情况是，在编码挑战期间面试官会在场（通过电话或者面对面）。他们会评估你的最终结果（代码），但他们不仅仅是为了这个原因在场。仅仅衡量你的编码能力并不需要他们的存在，通常在编程比赛中会遇到。面试编码挑战不是一个编程比赛。面试官想要在整个过程中看到你，以分析你的行为和沟通能力。他们想要看到你是否有解决问题的计划，你是以有组织还是混乱的方式行动，你是否写了丑陋的代码，你是否愿意沟通你的行动，或者你是否内向。此外，他们想要协助和指导你。当然，你需要努力不需要指导或尽可能少的指导，但对指导的适当反应也是受欢迎的。然而，努力不需要指导并不意味着你不应该与面试官互动。

#### 继续交流！

与面试官的互动是一个重要因素。以下列表解释了互动计划的几个方面：

+   **在编码之前解释你的解决方案**：在开始编码之前，从面试官那里挤出一些有价值的信息是很重要的。向他们描述你想要如何解决问题，你要遵循什么步骤，以及你会使用什么。例如，你可以说，“我认为在这里使用 HashSet 是合适的选择，因为插入的顺序不重要，而且我们不需要重复的值”。你会得到一个赞成的手势或一些建议，这将帮助你获得预期的结果。

+   **在编码时解释你在做什么**：在编码时，向面试官解释。例如，你可以说，*首先，我会创建一个 ArrayList 的实例*，或者，*在这里，我将文件从本地文件夹加载到内存中*。

+   **提出适当的问题**：只要你知道并尊重限制，你可以提出可以节省时间的问题。例如，问，“我记不得了 - 默认的 MySQL 端口是 3308 还是 3306？”然而，不要过分夸大这些问题！

+   **提及重要方面**：如果你知道与问题相关的其他信息，那么与面试官分享。这是一个展示你的编程知识、思想和围绕问题的想法的好机会。

如果你遇到一个你已经知道的问题（也许你在练习中解决过这样的问题），那么不要马上说出来。这不会给面试官留下好印象，你可能会得到另一个编码挑战。最好遵循你对任何其他问题的处理过程。在我们讨论这个过程之前，让我们解决面试环境的另一个方面。

### 纸笔与电脑的方法

如果编码挑战是通过电话屏幕进行的，那么面试官会要求你分享屏幕并在你喜欢的**集成开发环境**（**IDE**）中编码。这样，面试官可以看到你如何利用 IDE 的帮助（例如，他们可以看到你是否使用 IDE 生成 getter 和 setter，还是手动编写它们）。

重要提示

避免在每行代码后运行应用程序。相反，在每个逻辑代码块后运行应用程序。进行更正并再次运行。利用 IDE 调试工具。

如果你与面试官面对面，那么可能会被要求使用纸张或白板进行编码。这时，编码可以使用 Java 甚至伪代码。由于你的代码无法编译和执行，你必须手动测试它。通过拿一个例子并将其通过你的代码来展示你的代码是有效的是很重要的。

重要提示

在混乱的方法中避免过多的写入-删除代码循环。三思而后行！否则，你会让面试官头疼。

现在，让我们看一下旨在提供解决问题的方法论和逻辑方法的一般步骤。

### 处理编码挑战问题的过程

处理编码挑战问题的过程可以通过一系列顺序应用的步骤来完成。以下图表显示了这些步骤：

![图 5.2 - 处理编码挑战问题的过程](img/Figure_5.2_B15403.jpg)

图 5.2 - 处理编码挑战问题的过程

现在，让我们详细说明每个步骤。在应用这个解决问题的过程中，不要忘记交互组件。

#### 理解问题

理解问题非常重要。不要基于假设或对问题的部分理解开始解决问题。至少要读两遍问题！不要依赖于一次阅读，因为在大多数情况下，这些问题包含隐藏和模糊的要求或细节，很容易被忽略。

不要犹豫向面试官询问关于问题的问题。有些情况下，故意忽略细节，以测试你发现潜在问题的能力。

重要提示

只有你理解了问题，你才有解决它的机会。

接下来，是时候建立一个例子了。如果你能建立一个例子，那么这清楚地表明你已经理解了问题。

#### 建立一个例子

据说，“一幅图值千言”，但我们也可以用同样的方式来描述一个例子。

勾画问题并建立一个例子将澄清任何剩下的误解。这将给你一个通过逐步方法详细了解问题的机会。一旦你有一个可行的例子，你应该开始看到整体解决方案。这对于测试你的最终代码也是有用的。

重要提示

草图和例子对于巩固你对问题的理解是有用的。

现在，是时候考虑整体解决方案，并决定要使用的算法了。

#### 决定要使用的算法并解释它们

在这一点上，你已经理解了问题，甚至建立了一个例子。现在，是时候形成一个整体解决方案，并将其分解为步骤和算法了。

这是一个耗时的过程。在这一点上，重要的是应用“表达你的想法”的方法。如果你什么都不说，面试官就不知道你是一无所知还是在头脑风暴。例如，你可以说，“我觉得我可以用一个列表来存储邮件，...嗯...不，这不行，因为列表接受重复项。”当你在说话时（即使看起来像是在自言自语），面试官可以判断你推理的正确性，看到你的知识水平，并给你一些建议。面试官可能会回答说，“是的，这是一个很好的观点”，“但是不要忘记你需要保持插入的顺序”。

大多数情况下，问题需要对数据（字符串、数字、位、对象等）进行某种形式的操作，比如排序、排序、过滤、反转、展平、搜索、计算等。有数据的地方，也有数据结构（数组、列表、集合、映射、树等）。关键是找到你需要的数据操作和数据结构之间的适当匹配。通常，适当的匹配意味着以下内容：

+   你可以轻松地对数据结构应用某些操作。

+   你可以获得良好的性能（大 O - 见[*第七章*]（B15403_07_Final_JM_ePub.xhtml#_idTextAnchor135）*，算法的大 O 分析*）。

+   你可以在使用的数据结构之间保持和谐。这意味着你不需要复杂或繁重的算法，也不需要进行数据结构之间的转换或利用数据。

这些是拼图的大块。成功识别正确的匹配是工作的一半。另一半是将这些块组合在一起形成解决方案。换句话说，你需要在方程中引入逻辑。

在阅读问题或理解问题并在脑海中构思解决方案的大局之后，立即开始编码是非常诱人的。*不要这样做！*通常，这会导致一连串的失败，让你失去耐心。很快，你所有的想法都会被浓雾所包围，你会开始匆忙编码，甚至出现荒谬的错误。

重要提示

在开始编码之前，花时间深思熟虑解决方案。

现在，是时候开始编写你的解决方案，并用你的编码技能给面试官留下深刻印象了。

#### 编写骨架

用一个骨架开始编写解决方案。更准确地说，定义你的类、方法和接口，但不实现（行为/动作）。你将在下一步中填充它们。这样，你向面试官展示你的编码阶段遵循了一条清晰的道路。不要过于匆忙地跳入代码中。此外，尊重编程的基本原则，如**单一职责、开闭原则、里氏替换原则、接口隔离原则、依赖反转**（**SOLID**）和**不要重复自己**（**DRY**）。面试官很可能会关注这些原则。

重要提示

编写解决方案的骨架有助于面试官更容易地跟随你，并更好地理解你的推理。

此时，你已经吸引了面试官的注意。现在，是时候让你的骨架活起来了。

#### 编写解决方案

现在，是时候编写解决方案了。在这个过程中，向面试官解释你编写的主要代码行。注意并遵守著名的 Java 编码风格（例如，遵循 google.github.io/styleguide/javaguide.html 上的*Google Java Style Guide*）。

重要提示

遵循著名的 Java 编码风格并向面试官解释你的行动将对最终结果有很大帮助。

一旦你完成了解决方案的核心实现，就是增加代码的健壮性的时候了。因此，作为最后的一步，不要忽视异常处理和验证（例如，验证方法的参数）。同时，确保你满足了问题的所有要求，并且使用了正确的数据类型。最后，是时候祈祷你的代码能够通过测试了。

测试解决方案是这个过程的最后一步。

#### 测试解决方案

在这个过程的第二步中，你建立了一个例子。现在，是时候向面试官展示你的代码通过了例子的测试。*非常重要的是要证明你的代码至少对这个例子有效*。它可能会出现一些小错误，但最终，重要的是它能够运行。

不要放松！你赢得了当前的战斗，但并没有赢得战争！通常，面试官还想看到你的代码对边界情况或特殊情况的处理。通常，这些特殊情况涉及虚拟值、边界值、不当输入、强制异常的操作等。如果你的代码不够健壮，无法通过这些尝试，那么面试官会认为你在生产应用中也会这样编码。另一方面，如果你的代码有效，那么面试官会完全印象深刻。

重要提示

有效的代码应该让面试官满意。至少，你会感到他们对你更友好和放松一些。

如果你给面试官留下了良好的印象，那么面试官可能会想要问你一些额外的问题。你应该期待被问及代码的性能和替代解决方案。当然，你可以在没有被问及的情况下提供这样的信息。面试官会很高兴看到你能够以多种方式解决问题，并且你理解每种解决方案和决策的利弊。

### 卡住会让你僵住

首先，卡住是正常的。不要惊慌！不要沮丧！不要放弃！

如果你卡住了，那么面试官可能也会卡住。主要问题是如何处理这种障碍，而不是障碍本身。你必须保持冷静，并尝试做以下事情：

+   **回到你的示例**：有时，详细说明你的示例或查看另一个示例会有所帮助。有两个示例可以帮助你在脑海中塑造出一般情况，并理解问题的支柱。

+   在示例中孤立问题：每个示例都有一系列步骤。确定你卡住的步骤，并将其作为一个单独的问题专注解决。有时，将问题从上下文中分离出来可以让你更好地理解并解决它。

+   **尝试不同的方法**：有时，解决问题的方法是从不同的角度来解决问题。不同的视角可以给你一个新的视野。也许另一个数据结构，Java 的隐藏功能，蛮力方法等等可以帮助你。一个丑陋的解决方案总比没有解决方案好！

+   **模拟或推迟问题**：长时间挣扎解决一个步骤可能会导致你无法及时完成问题的不愉快情况。有时，最好是模拟或推迟导致你困扰的步骤，并继续进行其他步骤。可能最后当你回到这一步时，你会对它有更清晰的认识，并知道如何编码。

+   **寻求指导**：这应该是你的最后手段，但在危机中，你必须采取拼命的解决方案。你可以询问类似于“我对这个方面感到困惑，因为…”（并解释；尝试证明你的困惑）。“你能否给我一些关于我在这里错过了什么的提示？”

面试官意识到这一步（步骤）的困难，所以他们不会对你卡住感到惊讶。他们会欣赏你的毅力、分析能力和在寻找解决方案时的冷静，即使你找不到解决方案。面试官知道你在日常工作中会遇到类似的情况，而在这种情况下最重要的是保持冷静并寻找解决方案。

# 总结

在本章中，我们谈到了解决编程挑战问题的过程。除了我们之前列举的步骤 - 理解问题，构建示例，决定和解释算法，编写框架代码，编写和测试解决方案 - 还有一个步骤将成为接下来章节的目标：大量练习问题！在下一章中，我们将从编程的基本概念开始。