# 第十七章：数学和谜题

本章涵盖了一个在面试中经常遇到的有争议的话题：数学和谜题问题。许多公司认为这类问题不应该成为技术面试的一部分，而其他公司仍然认为这个话题是相关的。

这个话题包括的问题是令人费解的，可能需要相当高的数学和逻辑知识。如果你计划申请在学术领域工作的公司（数学、物理、化学等），你应该期待这样的问题。然而，亚马逊和谷歌等大公司也愿意依赖这类问题。

在本章中，我们将涵盖以下主题：

+   提示和建议

+   编码挑战

在本章结束时，你应该熟悉这类问题，并能够探索更多类似的问题。

# 技术要求

本章中包含的所有代码文件都可以在 GitHub 上找到：[`github.com/PacktPublishing/The-Complete-Coding-Interview-Guide-in-Java/tree/master/Chapter15`](https://github.com/PacktPublishing/The-Complete-Coding-Interview-Guide-in-Java/tree/master/Chapter15)。

# 提示和建议

当你遇到一个脑筋急转弯的问题时，最重要的是不要惊慌。多次阅读问题，并以系统化的方式写下你的结论是必不可少的。必须清楚地确定它应该遵守的输入、输出和约束条件。

尝试举几个例子（输入数据样本），画一些草图，并在分析问题时与面试官保持交流。面试官并不希望你立即得出解决方案，但他们期望听到你在尝试解决问题时的思考过程。这样，面试官可以追踪你的想法逻辑，并了解你解决问题的方式。

此外，非常重要的是写下你在解决问题时注意到的任何规则或模式。每写下一个陈述，你离解决方案更近一步。通常，如果你从解决方案的角度来看（你知道解决方案），这些问题并不是非常困难；它们只是需要高度的观察和更高的注意力。

让我们来试一个简单的例子。两个父亲和两个儿子坐下来吃鸡蛋。他们一共吃了三个鸡蛋；每个人都有一个鸡蛋。这怎么可能？

如果这是你第一次遇到这样的问题，你可能会认为这是不合逻辑或不可能解决的。认为文本中有错误（可能是四个鸡蛋，而不是三个）并一遍又一遍地阅读是正常的。这些是对脑筋急转弯问题最常见的反应。一旦你看到解决方案，它看起来就很简单了。

现在，让我们假设自己是面试官面前的候选人。以下段落采用了*大声思考*的方法。

如果每个人都有一个鸡蛋，而有三个鸡蛋，那么显然有一个人没有鸡蛋。所以，你可能会认为答案是三个人吃了一个鸡蛋（每个人都吃了一个鸡蛋），而第四个人什么都没吃。但问题说两个父亲和两个儿子坐下来吃鸡蛋，所以他们四个人都吃了鸡蛋。

试想一下：每个人都有一个鸡蛋，他们（四个人）一共吃了三个鸡蛋，所以问题并没有说每个人*吃*了一个鸡蛋；他们只是*有*一个鸡蛋。也许其中一个人把自己的鸡蛋分享给了另一个人。嗯，这似乎不太合乎逻辑！

可能只有三个人吗？如果其中一个父亲也是一个祖父，这意味着另一个父亲同时也是一个儿子和父亲。这样，通过三个人，我们有两个父亲和两个儿子。他们吃了三个鸡蛋，每个人都有一个鸡蛋。问题解决了！

正如你所看到的，解决方案是通过一系列推理的结果，逐个排除错误的解决方案而得到的。试图通过逻辑推理排除错误的解决方案来解决问题是解决这类问题的方法之一。其他问题只是关于计算。大多数时候，没有复杂的计算或大量的计算，但它们需要数学知识和/或推理。

很难断言有一些技巧和提示可以帮助你在几秒钟内解决数学和逻辑谜题问题。最好的方法是尽可能多地练习。有了这个，让我们继续进行*编码挑战*部分。

# 编码挑战

在接下来的 15 个编码挑战中，我们将专注于数学和逻辑谜题类别中最受欢迎的问题。让我们开始吧！

## 编码挑战 1 - FizzBuzz

**Adobe**，**Microsoft**

**问题**：考虑到你已经得到了一个正整数*n*。编写一个问题，打印从 1 到*n*的数字。对于 5 的倍数，打印*fizz*，对于 7 的倍数，打印*buzz*，对于 5 和 7 的倍数，打印*fizzbuzz*。在每个字符串或数字后打印一个新行。

**解决方案**：这是一个简单的问题，依赖于你对除法和 Java 取模(%)运算符的了解。当我们除两个数，被除数和除数，我们得到一个商和一个余数。在 Java 中，我们可以通过取模(%)运算符获得除法的余数。换句话说，如果*X*是被除数，*Y*是除数，那么*X*模*Y*（在 Java 中写作*X* % *Y*）返回*X*除以*Y*的余数。例如，11(被除数) / 2(除数) = 5(商) 1(余数)，所以 11 % 2 = 1。

换句话说，如果余数为 0，则被除数是除数的倍数；否则，它不是。因此，五的倍数必须满足*X* % 5 = 0，而七的倍数必须满足*X* % 7 = 0。基于这些关系，我们可以将这个问题的解决方案写成如下形式：

```java
public static void print(int n) {
  for (int i = 1; i <= n; i++) {
    if (((i % 5) == 0) && ((i % 7) == 0)) { // multiple of 5&7            
      System.out.println("fizzbuzz");
    } else if ((i % 5) == 0) { // multiple of 5            
      System.out.println("fizz");
    } else if ((i % 7) == 0) { // multiple of 7            
      System.out.println("buzz");
    } else {
      System.out.println(i); // not a multiple of 5 or 7
    }
  }
}
```

完整的应用程序称为*FizzBuzz*。

## 编码挑战 2 - 罗马数字

**Amazon**，**Google**，**Adobe**，**Microsoft**，**Flipkart**

**问题**：考虑到你已经得到了一个正整数*n*。编写一小段代码，将这个数字转换成它的罗马数字表示。例如，如果*n*=34，那么罗马数字就是 XXXIV。你已经得到了以下包含罗马数字符号的常量：

![图 15.1 - 罗马数字](img/Figure_15.1_B15403.jpg)

图 15.1 - 罗马数字

**解决方案**：这个问题依赖于罗马数字是常识。如果你从来没有听说过罗马数字，那么最好向面试官提到这一点。他们可能会同意给你另一个编码挑战来代替这个。但如果你知道罗马数字是什么，那太好了 - 让我们看看如何编写一个解决这个问题的应用程序。

这个问题的算法可以从几个例子中推导出来。让我们看几个用例：

+   *n* = 73 = 50+10+10+1+1+1 = L+X+X+I+I+I = LXXIII

+   *n* = 558 = 500+50+5+1+1+1 = D+L+V+I+I+I = DLVIII

+   *n* = 145 = 100+(50-10)+5 = C+(L-X)+V = C+XL+V = CXLV

+   *n* = 34 = 10+10+10+(5-1) = X+X+X+(V-I) = X+X+X+IV = XXXIV

+   *n* = 49 = (50-10)+(10-1) = (L-X)+(X-I) = XL+IX = XLIX

大致上，我们拿到给定的数字，然后尝试找到对应于个位、十位、百位或千位的罗马符号。这个算法可以表达如下：

1.  从千位开始并打印相应的罗马数字。例如，如果千位上的数字是 4，则打印 4000 的罗马数字等价物，即 MMMM。

1.  继续通过使用百位数字分割数字并打印相应的罗马数字。

1.  继续通过使用十位数字分割数字并打印相应的罗马数字。

1.  继续通过使用个位数对数字进行除法，并打印相应的罗马数字。

在代码方面，这个算法的工作原理如下：

```java
private static final String HUNDREDTHS[]
 = {"", "C", "CC", "CCC", "CD", "D", 
    "DC", "DCC", "DCCC", "CM"};
private static final String TENS[]
 = {"", "X", "XX", "XXX", 
    "XL", "L", "LX", "LXX", "LXXX", "XC"};
private static final String ONES[]
 = {"", "I", "II", "III", "IV", "V", 
    "VI", "VII", "VIII", "IX"};
public static String convert(int n) {
  String roman = "";
  // Step 1
  while (n >= 1000) {
    roman = roman + 'M';
    n -= 1000;
  }
  // Step 2
  roman = roman + HUNDREDTHS[n / 100];
  n = n % 100;
  // Step 3
  roman = roman + TENS[n / 10];
  n = n % 10;
  // Step 4
  roman = roman + ONES[n];
  return roman;
}
```

完整的应用程序称为*RomanNumbers*。另一种方法依赖于连续的减法而不是除法。*RomanNumbers*应用程序也包含了这种实现。

## 编码挑战 3 - 访问和切换 100 扇门

**Adobe**，**Microsoft**，**Flipkart**

**问题**：假设你有 100 扇门，它们最初都是关闭的。你必须访问这些门 100 次，每次都从第一扇门开始。对于每个访问的门，你都要切换它（如果它关闭，则打开它，反之亦然）。在第一次访问时，你访问所有 100 扇门。在第二次访问时，你访问每第二扇门（＃2、＃4、＃6……）。在第三次访问时，你访问每第三扇门（＃3、＃6、＃9……）。你按照这个模式一直到只访问第 100 扇门。编写一小段代码，揭示 100 次访问后门的状态（关闭或打开）。

**解决方案**：通过遍历几步可以直观地解决这个问题。在初始状态下，所有 100 扇门都是关闭的（在下图中，每个 0 都是关闭的门，每个 1 都是打开的门）：

![图 15.2 - 所有门都关闭（初始状态）](img/Figure_15.2_B15403.jpg)

图 15.2 - 所有门都关闭（初始状态）

现在，让我们看看在以下每个步骤中我们能观察和得出什么结论：

在第一次访问时，我们打开每扇门（我们访问每扇门，＃1、＃2、＃3、＃4、…，＃100）：

![图 15.3 - 所有门都打开（步骤 1）](img/Figure_15.3_B15403.jpg)

图 15.3 - 所有门都打开（步骤 1）

在第二次访问时，我们只访问偶数门（＃2、＃4、＃6、＃8、＃10、＃12……），所以偶数门关闭，奇数门打开：

![图 15.4 - 偶数门关闭，奇数门打开（步骤 2）](img/Figure_15.4_B15403.jpg)

图 15.4 - 偶数门关闭，奇数门打开（步骤 2）

在第三次访问时，我们只访问门＃3、＃6、＃9、＃12……这次，我们关闭了第一次访问时打开的门＃3，打开了第二次访问时关闭的门＃6，依此类推：

![图 15.5 - 应用第三次访问后的结果（步骤 3）](img/Figure_15.5_B15403.jpg)

图 15.5 - 应用第三次访问后的结果（步骤 3）

在第四次访问时，我们只访问门＃4、＃8、＃12……如果我们继续这样做，那么在第 100 次访问时，我们将得到以下结果：

![图 15.6 - 所有打开的门都是完全平方数（最后一次访问）](img/Figure_15.6_B15403.jpg)

图 15.6 - 所有打开的门都是完全平方数（最后一次访问）

因此，在最后一次访问（第 100 次访问）时，所有打开的门都是完全平方数，而其余的门都是关闭的。显然，即使我们观察到这一点，在面试中我们也没有足够的时间来遍历 100 次访问。但也许我们甚至不需要做所有 100 次访问来观察这个结果。让我们假设我们只做 15 步，然后我们试图看看某扇门发生了什么。例如，以下图像显示了门＃12 在 15 步中的状态：

![图 15.7 - 第 15 步后的门＃12](img/Figure_15.7_B15403.jpg)

图 15.7 - 第 15 步后的门＃12

检查前面图像中突出显示的步骤。门＃12 的状态在*步骤 1、2、3、4、6*和*12*发生了变化。所有这些步骤都是 12 的约数。此外，*步骤 1*打开门，*步骤 2*关闭门，*步骤 3*打开门，*步骤 4*关闭门，*步骤 6*打开门，*步骤 12*关闭门。从这个观察开始，我们可以得出结论，对于每一对约数，门最终都会回到初始状态，即关闭状态。换句话说，每个具有偶数个约数的门最终都会关闭。

让我们看看这是否对于一个完全平方数来说是正确的，比如 9。选择完全平方数的原因在于完全平方数总是有奇数个正因子。例如，9 的因子是 1、3 和 9。这意味着门#9 保持打开状态。

根据这两段文字，我们可以得出结论，经过 100 次访问后，保持打开状态的门是那些完全平方数（#1，#4，#9，#16，...，#100），而其余的门保持关闭状态。

一旦你理解了前面的过程，编写一个确认最终结果的应用程序就非常简单了：

```java
private static final int DOORS = 100;
public static int[] visitToggle() {
  // 0 - closed door
  // 1 - opened door     
  int[] doors = new int[DOORS];
  for (int i = 0; i <= (DOORS - 1); i++) {
    doors[i] = 0;
  }
  for (int i = 0; i <= (DOORS - 1); i++) {
    for (int j = 0; j <= (DOORS - 1); j++) {
      if ((j + 1) % (i + 1) == 0) {
        if (doors[j] == 0) {
          doors[j] = 1;
        } else {
          doors[j] = 0;
        }
      }
    }            
  }
  return doors;
}
```

完整的应用程序称为*VisitToggle100Doors*。

## 编码挑战 4 - 8 支队伍

**亚马逊**，**谷歌**，**Adobe**

**问题**：考虑有一个比赛，有 8 支队伍。每支队伍与其他队伍比赛两次。从所有这些队伍中，只有 4 支队伍进入半决赛。一支队伍要赢得多少场比赛才能进入半决赛？

**解决方案**：让我们将队伍标记为 T1、T2、T3、T4、T5、T6、T7 和 T8。如果 T1 与 T2...T8 比赛，他们将进行 7 场比赛。由于每个队伍必须与其他队伍比赛两次，所以我们有 8*7=56 场比赛。如果每场比赛中一支队伍可以赢得一分，那么我们有 56 分分配给 8 支队伍。

让我们考虑最坏的情况。T0 输掉了所有比赛。这意味着 T0 得到 0 分。另一方面，T1 对 T0 赢得了 2 分，并输掉了所有其他比赛，T2 对 T0 和 T1 赢得了 4 分，并输掉了所有其他比赛，T3 对 T0、T1 和 T2 赢得了 6 分，并输掉了所有其他比赛，依此类推。T4 赢得了 8 分，T5 赢得了 10 分，T6 赢得了 12 分，T7 赢得了 14 分。因此，一支赢得所有比赛的队伍赢得了 14 分。最后四支队伍（进入半决赛的队伍）赢得了 8+10+12+14=44 分。因此，一支队伍可以确保他们进入半决赛，如果他们获得至少 44/4=11 分。

## 编码挑战 5 - 找到具有质因数 3、5 和 7 的第 k 个数字

**Adobe**，**微软**

**问题**：设计一个算法，找到唯一的质因数是 3、5 和 7 的第 k 个数字。

**解决方案**：拥有一组数字，其唯一的质因数是 3、5 和 7，意味着一组看起来如下：1、3、5、7、9、15、21、25 等等。或者，更具启发性地，可以写成：1、1*3、1*5、1*7、3*3、3*5、3*7、5*5、3*3*3、5*7、3*3*5、7*7 等等。

通过这种具有启发性的表示，我们可以看到我们可以最初将值 1 插入列表中，而其余的元素必须计算出来。理解确定其余元素的算法最简单的方法是看实现本身，所以让我们来看看：

```java
public static int kth(int k) {
  int count3 = 0;
  int count5 = 0;
  int count7 = 0;
  List<Integer> list = new ArrayList<>();
  list.add(1);
  while (list.size() <= k + 1) {
    int m = min(min(list.get(count3) * 3, 
      list.get(count5) * 5), list.get(count7) * 7);
    list.add(m);
    if (m == list.get(count3) * 3) {
      count3++;
    }
    if (m == list.get(count5) * 5) {
      count5++;
    }
    if (m == list.get(count7) * 7) {
      count7++;
    }
  }
  return list.get(k - 1);
}
```

我们也可以通过三个队列来实现。该算法的步骤如下：

1.  初始化一个整数*minElem*=1。

1.  初始化三个队列；即*queue3*、*queue5*和*queue7*。

1.  从 1 到给定的*k*-1 进行循环：

a. 将*minElem**3、*minElem**5 和*minElem**7 分别插入*queue3*、*queue5*和*queue7*。

b. 更新*minElem*为 min(*queue3*.peek, *queue5*.peek, *queue7*.peek)。

c. 如果*minElem*是*queue3*.peek，则执行*queue3*.poll。

d. 如果*minElem*是*queue5*.peek，则执行*queue5*.poll。

e. 如果*minElem*是*queue7*.peek，则执行*queue7*.poll。

1.  返回*minElem*。

完整的应用程序称为*KthNumber357*。它包含了本节中提出的两种解决方案。

## 编码挑战 6 - 计算解码数字序列

**亚马逊**，**微软**，**Flipkart**

**问题**：假设*A*是 1，*B*是 2，*C*是 3，... *Z*是 26。对于任何给定的数字序列，编写一小段代码来计算可能的解码数量（例如，1234 可以解码为 1 2 3 4，12 3 4 和 1 23 4，也就是 ABCD、LCD 和 AWD）。如果给定的数字序列包含从 0 到 9 的数字，则它是有效的。不允许前导 0，不允许额外的尾随 0，也不允许连续出现两个或更多个 0。

**解决方案**：这个问题可以通过递归或动态规划来解决。这两种技术都在*第八章**，递归和动态规划*中讨论过。因此，让我们看看一个 *n* 位数字序列的递归算法：

1.  将解码的总数初始化为 0。

1.  从给定数字序列的末尾开始。

1.  如果最后一位不是 0，则对(*n*-1)位数字应用递归，并使用结果更新解码的总数。

1.  如果最后两位数字表示的数字小于 27（因此是有效字符），则对(*n*-2)位数字应用递归，并使用结果更新解码的总数。

在代码方面，我们有以下内容：

```java
public static int decoding(char[] digits, int n) {
  // base cases 
  if (n == 0 || n == 1) {
    return 1;
  }
  // if the digits[] starts with 0 (for example, '0212')
  if (digits == null || digits[0] == '0') {
    return 0;
  }
  int count = 0;
  // If the last digit is not 0 then last 
  // digit must add to the number of words 
  if (digits[n - 1] > '0') {
    count = decoding(digits, n - 1);
  }
  // If the last two digits represents a number smaller 
  // than or equal to 26 then consider last two digits 
  // and call decoding()
  if (digits[n - 2] == '1'
      || (digits[n - 2] == '2' && digits[n - 1] < '7')) {
    count += decoding(digits, n - 2);
  }
  return count;
}
```

这段代码运行时间是指数级的。但是我们可以应用动态规划，通过类似的非递归算法将运行时间降低到 O(n)，具体如下：

```java
public static int decoding(char digits[]) {
  // if the digits[] starts with 0 (for example, '0212')
  if (digits == null || digits[0] == '0') {
    return 0;
  }
  int n = digits.length;
  // store results of sub-problems 
  int count[] = new int[n + 1];
  count[0] = 1;
  count[1] = 1;
  for (int i = 2; i <= n; i++) {
    count[i] = 0;
    // If the last digit is not 0 then last digit must 
    // add to the number of words 
    if (digits[i - 1] > '0') {
      count[i] = count[i - 1];
    }
    // If the second last digit is smaller than 2 and 
    // the last digit is smaller than 7, then last 
    // two digits represent a valid character 
    if (digits[i - 2] == '1' || (digits[i - 2] == '2' 
          && digits[i - 1] < '7')) {
      count[i] += count[i - 2];
    }
  }
  return count[n];
}
```

这段代码运行时间是 O(n)。完整的应用程序称为 *DecodingDigitSequence*。

## 编程挑战 7 – ABCD

**问题**：找到一种类型的数字 ABCD，使得乘以 4 后得到 DCBA。

**解决方案**：这类问题通常相当难。在这种情况下，我们必须使用一些数学来解决它。

让我们从一些简单的不等式开始：

+   1 <= A <= 9（A 不能为零，因为 ABCD 是一个四位数）

+   0 <= B <= 9

+   0 <= C <= 9

+   4 <= D <= 9（D 必须至少为 4*A，所以至少应为 4）

接下来，我们可以假设我们的数字 ABCD 被写成 1000A + 100B + 10C + D。根据问题描述，我们可以将 ABCD 乘以 4 得到 DCBA，可以写成 1000D + 100C + 10B + A。

符合 4 的整除性，BA 是一个可以被 4 整除的两位数。现在，较大的 ABCD 是 2499，因为大于 2499 的数乘以 4 将得到一个五位数。

接下来，A 可以是 1 和 2。然而，如果 BA 是一个可以被 4 整除的两位数，那么 A 必须是偶数，所以必须是 2。

继续这种逻辑，这意味着 D 要么是 8，要么是 9。然而，由于 D 乘以 4 会以 2 结尾，所以 D 必须是 8。

此外，4000A + 400B + 40C + 4D = 1000D + 100C + 10B + A。由于 A=2 和 D=8，这可以写成 2C-13B=1。B 和 C 只能是 [1, 7] 范围内的个位整数，但由于 BA 是一个可以被 4 整除的两位数，B 必须是奇数。由于最大可能的数字是 2499，这意味着 B 可以是 1 或 3。

因此，结果是 2178，因为 2178*4=8712，所以 ABCD*4=DCBA。

我们也可以使用蛮力方法来找到这个数字。以下代码说明了这一点：

```java
public static void find() {
  for (int i = 1000; i < 2499; i++) {
    int p = i;
    int q = i * 4;
    String m = String.valueOf(p);
    String n = new StringBuilder(String.valueOf(q))
      .reverse().toString();
    p = Integer.parseInt(m);
    q = Integer.parseInt(n);
    if (p == q) {
      System.out.println("\n\nFound: " + p + " : " + (q * 4));
      break;
    }
  }
}
```

完整的应用程序称为 *Abcd*。

## 编程挑战 8 – 重叠的矩形

**亚马逊**，**谷歌**，**微软**

`true` 如果这些矩形重叠（也称为相交）。

**解决方案**：这个问题听起来有点模糊。重要的是要与面试官讨论并就两个重要方面达成一致：

*这两个矩形是平行的，并且与水平面成 0 度角（它们与坐标轴平行），或者它们可以在一个角度下旋转吗？*

大多数情况下，给定的矩形是平行的，并且与坐标轴平行。如果涉及旋转，那么解决方案需要一些几何知识，这在面试中并不那么明显。面试官很可能是想测试你的逻辑，而不是你的几何知识，但是挑战自己，为非平行矩形实现问题。

*矩形的坐标是在笛卡尔平面上给出的吗？* 答案应该是肯定的，因为这是数学中常用的坐标系。这意味着一个矩形从左到右，从下到上增加大小。

因此，让我们将矩形表示为*r1*和*r2*。它们每个都是通过左上角和右下角的坐标给出的。*r1*的左上角的坐标为*r1lt.x*和*r1lt.y*，而右下角的坐标为*r2rb.x*和*r2rb.y*，如下图所示：

![图 15.8-矩形坐标](img/Figure_15.8_B15403.jpg)

图 15.8-矩形坐标

我们可以说，如果两个矩形*接触*（至少有一个公共点），它们就是重叠的。换句话说，在下图中显示的五对矩形中，有重叠：

![图 15.9-重叠的矩形](img/Figure_15.9_B15403.jpg)

图 15.9-重叠的矩形

从前面的图表中，我们可以得出两个不重叠的矩形可能处于以下四种情况之一：

+   *r1*完全在*r2*的右边。

+   *r1*完全在*r2*的左边。 

+   *r1*完全在*r2*的上方。

+   *r1*完全在*r2*下方。

以下图表显示了这四种情况：

![图 15.10-不重叠的矩形](img/Figure_15.10_B15403.jpg)

图 15.10-不重叠的矩形

我们可以用坐标表示前面的四个项目，如下所示：

+   *r1*完全在*r2*的右边→*r1lt.x>r2rb.x*

+   *r1*完全在*r2*的左边→*r2lt.x>r1rb.x*

+   *r1*完全在*r2*上方→*r1rb.y>r2lt.y*

+   *r1*完全在*r2*下方→*r2rb.y>r1lt.y*

因此，如果我们将这些条件分组到代码中，我们得到以下结果：

```java
public static boolean overlap(Point r1lt, Point r1rb, 
        Point r2lt, Point r2rb) {
  // r1 is totally to the right of r2 or vice versa
  if (r1lt.x > r2rb.x || r2lt.x > r1rb.x) {
    return false;
  }
  // r1 is totally above r2 or vice versa
  if (r1rb.y > r2lt.y || r2rb.y > r1lt.y) {
    return false;
  }
  return true;
}
```

这段代码运行时间为 O(1)。或者，我们可以将这两个条件合并为一个条件，如下所示：

```java
public static boolean overlap(Point r1lt, Point r1rb, 
        Point r2lt, Point r2rb) {
  return (r1lt.x <= r2rb.x && r1rb.x >= r2lt.x
           && r1lt.y >= r2rb.y && r1rb.y <= r2lt.y);
}
```

完整的应用程序称为*RectangleOverlap*。请注意，面试官可能以不同的方式定义*重叠*。根据这个问题，你应该能够相应地调整代码。

## 编码挑战 9-乘以大数

**亚马逊**，**微软**

整数或长整数域。编写一个计算*a*b*的代码片段。

**解决方案**：让我们假设*a*=4145775 和*b*=771467。然后，*a*b*=3198328601925。解决这个问题依赖于数学。以下图像描述了可以在纸上应用并编码的*a*b*解决方案：

![图 15.11-两个大数相乘](img/Figure_15.11_B15403.jpg)

图 15.11-两个大数相乘

主要是，我们依赖于乘法可以写成一系列加法的事实。因此，我们可以将 771467 写成 7+60+400+1000+70000+700000，然后我们将这些数字中的每一个与 4145775 相乘。最后，我们将结果相加以获得最终结果 3198328601925。进一步推理，我们可以取第一个数字的最后一位（5）并将其乘以第二个数字的所有数字（7,6,4,1,7,7）。然后，我们取第一个数字的第二位（7）并将其乘以第二个数字的所有数字（7,6,4,1,7,7）。然后，我们取第一个数字的第三位（7）并将其乘以第二个数字的所有数字（7,6,4,1,7,7）。我们继续这个过程，直到我们将第一个数字的所有数字乘以第二个数字的所有数字。在添加结果时，我们声明*t*th 乘法移位。

在代码方面，我们有以下内容：

```java
public static String multiply(String a, String b) {
  int lenA = a.length();
  int lenB = b.length();
  if (lenA == 0 || lenB == 0) {
    return "0";
  }
  // the result of multiplication is stored in reverse order 
  int c[] = new int[lenA + lenB];
  // indexes to find positions in result
  int idx1 = 0;
  int idx2 = 0;
  // loop 'a' right to left
  for (int i = lenA - 1; i >= 0; i--) {
    int carry = 0;
    int n1 = a.charAt(i) - '0';
    // used to shift position to left after every 
    // multiplication of a digit in 'b' 
    idx2 = 0;
    // loop 'b' from right to left
    for (int j = lenB - 1; j >= 0; j--) {
      // current digit of second number 
      int n2 = b.charAt(j) - '0';
      // multiply with current digit of first number 
      int sum = n1 * n2 + c[idx1 + idx2] + carry;
      // carry of the next iteration
      carry = sum / 10;
      c[idx1 + idx2] = sum % 10;
      idx2++;
    }
    // store carry 
    if (carry > 0) {
      c[idx1 + idx2] += carry;
    }
    // shift position to left after every 
    // multiplication of a digit in 'a' 
    idx1++;
  }
  // ignore '0's from the right 
  int i = c.length - 1;
  while (i >= 0 && c[i] == 0) {
    i--;
  }
  // If all were '0's - means either both or 
  // one of 'a' or 'b' were '0' 
  if (i == -1) {
    return "0";
  }
  String result = "";
  while (i >= 0) {
    result += (c[i--]);
  }
  return result;
}
```

完整的应用程序称为*MultiplyLargeNumbers*。

## 编码挑战 10-具有相同数字的下一个最大数字

**亚马逊**，**谷歌**，**微软**

**问题**：考虑到你已经得到了一个正整数。编写一个返回具有相同数字的下一个最大数字的代码片段。

**解决方案**：通过几个示例可以观察到这个问题的解决方案。让我们考虑以下示例：

+   示例 1：6→不可能

+   示例 2：1234→1243

+   示例 3：1232→1322

+   示例 4：321→不可能

+   示例 5：621873→623178

从前面的例子中，我们可以直觉到解决方案可以通过重新排列给定数字的数字来获得。因此，如果我们可以找到交换数字的规则集，使我们得到要搜索的数字，那么我们可以尝试实现。

让我们尝试几个观察：

+   从示例 1 和 4 可以看出，如果给定数字的数字是降序的，那么不可能找到更大的数字。每次交换都会导致更小的数字。

+   从示例 2 可以看出，如果给定数字的数字是按升序排列的，那么具有相同数字的下一个更大数字可以通过交换最后两个数字来获得。

+   从示例 3 和 5 可以看出，我们需要找到所有更大数字中的最小数字。为此，我们必须从最右边处理数字。以下算法阐明了这一说法。

基于这三点观察，我们可以详细说明以下算法，该算法已在数字 621873 上进行了示例：

1.  我们从最右边的数字开始逐个遍历数字。我们一直遍历，直到找到一个比先前遍历的数字小的数字。例如，如果给定的数字是 621873，那么我们遍历到 621873 中的数字 1。数字 1 是第一个比先前遍历的数字 8 小的数字。

1.  接下来，我们关注我们在步骤 1 中找到的数字右侧的数字。我们想在这些数字中找到最小的数字（我们将其表示为*t*）。由于这些数字按降序排列，最小的数字在最后位置。例如，3 是 1 右侧数字中最小的数字，62**1**87**3**。

1.  我们交换这两个数字（1 和 3），我们得到 62**3**87**1**。

1.  最后，我们将所有数字按升序排列到*t*的右侧。但是由于我们知道*t*右侧的所有数字都是按降序排列的，除了最后一个数字，我们可以应用线性反转。这意味着结果是 623**178**。这就是要搜索的数字。

这个算法可以很容易地实现，如下所示：

```java
public static void findNextGreater(int arr[]) {
  int min = -1;
  int len = arr.length;
  int prevDigit = arr[arr.length - 1];
  int currentDigit;
  // Step 1: Start from the rightmost digit and find the 
  // first digit that is smaller than the digit next to it. 
  for (int i = len - 2; i >= 0; i--) {
    currentDigit = arr[i];
    if (currentDigit < prevDigit) {
      min = i;
      break;
    }
  }
  // If 'min' is -1 then there is no such digit. 
  // This means that the digits are in descending order. 
  // There is no greater number with same set of digits 
  // as the given one.
  if (min == -1) {
    System.out.println("There is no greater number with "
     + "same set of digits as the given one.");
  } else {
    // Steps 2 and 3: Swap 'min' with 'len-1'
    swap(arr, min, len - 1);
    // Step 4: Sort in ascending order all the digits 
    // to the right side of the swapped 'len-1'
    reverse(arr, min + 1, len - 1);
    // print the result
    System.out.print("The next greater number is: ");
    for (int i : arr) {
      System.out.print(i);
    }
  }
}
private static void reverse(int[] arr, int start, int end) {
  while (start < end) {
    swap(arr, start, end);
    start++;
    end--;
  }
}
private static void swap(int[] arr, int i, int j) {
  int aux = arr[i];
  arr[i] = arr[j];
  arr[j] = aux;
}
```

这段代码运行时间为 O(n)。完整的应用程序称为*NextElementSameDigits*。

## 编码挑战 11 - 数字可被其数字整除

**亚马逊**，**谷歌**，**Adobe**，**微软**

如果给定数字可以被其数字整除，则返回`true`。

`true`，因为 412 可以被 2、1 和 4 整除。另一方面，如果*n*=143，那么输出应该是`false`，因为 143 不能被 3 和 4 整除。

如果你认为这个问题很简单，那么你是完全正确的。这些问题被用作*热身*问题，并且有助于快速筛选出很多候选人。大多数情况下，你应该在规定的时间内解决它（例如，2-3 分钟）。

重要说明

建议对待这些简单的问题与对待任何其他问题一样认真。一个小错误可能会让你提前退出比赛。

因此，对于这个问题，算法包括以下步骤：

1.  获取给定数字的所有数字。

1.  对于每个数字，检查*给定数字* *%数字*是否为 0（这意味着可被整除）。

1.  如果其中任何一个不为零，则返回`false`。

1.  如果对于所有数字，*给定数字%数字*都是 0，则返回`true`。

在代码方面，我们有以下内容：

```java
public static boolean isDivisible(int n) {
  int t = n;
  while (n > 0) {
    int k = n % 10;
    if (k != 0 && t % k != 0) {
      return false;
    }
    n /= 10;
  }
  return true;
}
```

完整的应用程序称为*NumberDivisibleDigits*。

## 编码挑战 12 - 打破巧克力

**亚马逊**，**谷歌**，**Adobe**，**微软**，**Flipkart**

**问题**：考虑到你已经得到了尺寸为*宽度* x *高度*的矩形巧克力条和一些瓷砖。通常情况下，巧克力由许多小瓷砖组成，因此*宽度*和*高度*给出了我们的瓷砖数量（例如，巧克力尺寸为 4 x 3，包含 12 块瓷砖）。编写一小段代码，计算我们需要对给定的巧克力施加多少次断裂（切割）才能获得具有完全所需数量的瓷砖的一块。您可以通过单个垂直或水平断裂（切割）将给定的巧克力切成两个矩形块。

**解决方案**：让我们考虑以下图像中显示的巧克力（一个 3 x 6 的巧克力条，有 18 块瓷砖）：

![图 15.12 – 一个 3 x 6 巧克力条](img/Figure_15.12_B15403.jpg)

图 15.12 – 一个 3 x 6 巧克力条

前面的图像显示了七种情况，可以带我们找到解决方案，如下：

+   情况 1、2 和 3：如果给定瓷砖的数量大于 3 x 6 或者我们无法将瓷砖与巧克力的*宽度*或*高度*排列在一起，则无法获得解决方案。对于无解，我们返回-1。

+   情况 4：如果给定瓷砖的数量等于 3 x 6 = 18，则这就是解决方案，所以我们不需要切割。我们将返回 0。

+   情况 5：如果给定瓷砖的数量可以与巧克力条的*宽度*排列在一起，则只需要一次切割。我们将返回 1。

+   情况 6：如果给定瓷砖的数量可以与巧克力条的*高度*排列在一起，则只需要一次切割。我们将返回 1。

+   情况 7：在所有其他情况下，我们需要 2 次切割。我们将返回 2。

让我们看看代码：

```java
public static int breakit(int width, int height, int nTiles) {
  if (width <= 0 || height <= 0 || nTiles <= 0) {
    return -1;
  }
  // case 1
  if (width * height < nTiles) {
    return -1;
  }
  // case 4
  if (width * height == nTiles) {
    return 0;
  } 
  // cases 5 and 6
  if ((nTiles % width == 0 && (nTiles / width) < height)
     || (nTiles % height == 0 && (nTiles / height) < width)) {
    return 1;
  }
  // case 7
  for (int i = 1; i <= Math.sqrt(nTiles); i++) {
    if (nTiles % i == 0) {
      int a = i;
      int b = nTiles / i;
      if ((a <= width && b <= height)
          || (a <= height && b <= width)) {
        return 2;
      }
    }
  }
  // cases 2 and 3
  return -1;
}
```

完整的应用程序称为*BreakChocolate*。

## 编码挑战 13 – 时钟角度

**谷歌**，**微软**

**问题**：考虑到你已经以*h:m*格式给出时间。编写一小段代码，计算模拟时钟上时针和分针之间的较短角度。

**解决方案**：从一开始，我们必须考虑几个公式，这些公式将帮助我们得出解决方案。

首先，时钟被分成 12 个相等的小时（或 12 个相等的部分），因为它是一个完整的圆，所以有 360o。因此，1 小时有 360o/12 = 30o。因此，在 1:00 时，时针与分针形成 300 的角度。在 2:00 时，时针与分针形成 60o 的角度，依此类推。以下图像阐明了这一方面：

![图 15.13 – 12 小时的 360 度分割](img/Figure_15.13_B15403.jpg)

图 15.13 – 12 小时的 360 度分割

进一步推理，1 小时有 60 分钟和 30o，因此 1 分钟有 30/60 = 0.5o。因此，如果我们只参考时针，那么在 1:10 时，我们有 30o + 10*0.5o = 30o + 5o = 35o。或者，在 4:17 时，我们有 4*30o + 17*0.5o = 120o + 8.5o = 128.5o。

到目前为止，我们知道可以计算给定*h:m*时间的时针角度为*h**300 + *m**0.5o。对于计算分针的角度，我们可以认为，在 1 小时内，分针需要完成 360o 的旋转，因此 360o/ 60 分钟 = 每分钟 6o。因此，在*h*:24 时，分针形成 144o 的角度。在*h*:35 时，分针形成 210o 的角度，依此类推。

因此，时针和分针之间的角度是 abs((*h**30o + *m**0.5o) - *m**6o)。如果返回的*result*大于 180o，则我们必须返回(360o - *result*)，因为问题要求我们计算时针和分针之间的较短角度。

现在，让我们尝试计算以下图像中显示的时钟所需的角度：

![图 15.14 – 三个时钟](img/Figure_15.14_B15403.jpg)

图 15.14 – 三个时钟

**时钟 1，10:10**：

+   时针：10*30o + 10*0.5o = 300o + 5o = 305o

+   分针：10 * 6o = 60o

+   结果：abs(305o - 60o) = abs(245o) = 245o > 180o，因此返回 360o - 245o = 115o

**时钟 2，9:40**：

+   时针：9*30o + 40*0.5o = 270o + 20o = 290o

+   分针：40 * 6o = 240o

+   结果：abs(290o - 240o) = abs(50o) = 50o

**时钟 3，4:40**：

+   时针：4*30o + 40*0.5o = 120o + 20o = 140o

+   分钟：40 * 6o = 240o

+   结果：abs(140o - 240o) = abs(-100o) = 100o

根据这些陈述，我们可以编写以下代码：

```java
public static float findAngle(int hour, int min) {
  float angle = (float) Math.abs(((30f * hour) 
    + (0.5f * min)) - (6f * min));
  return angle > 180f ? (360f - angle) : angle;
}
```

完整的应用程序称为*HourMinuteAngle*。

## 编码挑战 14-勾股定理三元组

**谷歌**，**Adobe**，**微软**

**问题**：勾股定理三元组是一组三个正整数{*a，b，c*}，使得*a*2 = *b*2 + *c*2。假设你得到了一个正整数数组*arr*。编写一小段代码，打印出这个数组的所有勾股定理三元组。

**解决方案**：可以通过三个循环实现蛮力方法，尝试给定数组中的所有可能三元组。但这将在 O(n3)的复杂度时间内工作。显然，蛮力方法（通常称为*naive*方法）不会给面试官留下深刻印象，所以我们必须做得比这更好。

实际上，我们可以在 O(n2)的时间内解决这个问题。让我们看看算法的步骤：

1.  对输入数组中的每个元素进行平方（O(n)）。这意味着我们可以将*a*2 = *b*2 + *c*2 写成*a* = *b* + *c*。

1.  按升序对给定数组进行排序（O(n log n)）。

1.  如果*a* = *b* + *c*，那么*a*始终是*a*、*b*和*c*之间的最大值。因此，我们固定*a*，使其成为这个排序数组的最后一个元素。

1.  固定*b*，使其成为这个排序数组的第一个元素。

1.  固定*c*，使其成为元素*a*之前的元素。

1.  到目前为止，*b<a*且*c<a*。要找到勾股定理三元组，执行一个循环，从 1 增加*b*到*n*，从*n*减少*c*到 1。当*b*和*c*相遇时，循环停止：

a. 如果*b + c < a*，则增加*b*的索引。

b. 如果*b + c > a*，则减少*c*的索引。

c. 如果*b + c*等于*a*，则打印找到的三元组。增加*b*的索引并减少*c*的索引。

1.  从*步骤 3*开始重复下一个*a*。

假设*arr*={3, 6, 8, 5, 10, 4, 12, 14}。经过前两步，*arr*={9, 16, 25, 36, 64, 100, 144, 196}。经过*步骤 3*、*4*和*5*，我们有*a*=196，*b*=9，*c*=144，如下所示：

![图 15.15-设置 a、b 和 c](img/Figure_15.15_B15403.jpg)

图 15.15-设置 a、b 和 c

由于 9+144 < 196，*b*的索引增加 1，符合*步骤 6a*。对于 16+144，25+144 和 36+144，同样的步骤适用。由于 64+144 > 196，*c*的索引减少 1，符合*步骤 6b*。

由于 64 +100 < 196，*b*的索引增加 1，符合*步骤 6a*。循环在这里停止，因为*b*和*c*相遇，如下所示：

![图 15.16-循环结束时的 b 和 c](img/Figure_15.16_B15403.jpg)

图 15.16-循环结束时的 b 和 c

接下来，根据*步骤 7*，我们设置*a*=144，*b*=9，*c*=100。对每个*a*重复此过程。当*a*变为 100 时，我们找到了第一个勾股定理三元组；即*a*=100，*b*=36，*c*=64，如下所示：

![图 15.17-勾股定理三元组](img/Figure_15.17_B15403.jpg)

图 15.17-勾股定理三元组

让我们把这个算法写成代码：

```java
public static void triplet(int arr[]) {
  int len = arr.length;
  // Step1
  for (int i = 0; i < len; i++) {
    arr[i] = arr[i] * arr[i];
  }
  // Step 2
  Arrays.sort(arr);
  // Steps 3, 4, and 5
  for (int i = len - 1; i >= 2; i--) {  
    int b = 0;
    int c = i - 1;
    // Step 6
    while (b < c) {
      // Step 6c
      if (arr[b] + arr[c] == arr[i]) {
        System.out.println("Triplet: " + Math.sqrt(arr[b]) 
          + ", " + Math.sqrt(arr[c]) + ", " 
              + Math.sqrt(arr[i]));
        b++;
        c--;
      }
      // Steps 6a and 6b
      if (arr[b] + arr[c] < arr[i]) {
        b++;
      } else {
        c--;
      }
    }
  }
}
```

完整的应用程序称为*PythagoreanTriplets*。

## 编码挑战 15-调度一个电梯

**亚马逊**，**谷歌**，**Adobe**，**微软**，**Flipkart**

**问题**：假设你得到了一个表示*n*个人目的地楼层的数组。电梯的容量为给定的*k*。最初，电梯和所有人都在 0 楼（底楼）。电梯从当前楼层到达任何连续楼层（向上或向下）需要 1 个时间单位。编写一小段代码，安排电梯，以便我们获得将所有人到达目的地楼层所需的最小总时间，然后返回到地面楼层。

**解决方案**：让我们考虑给定的目的地数组为*floors* = {4, 2, 1, 2, 4}，*k*=3。所以，我们有五个人：一个人去一楼，两个人去二楼，两个人去四楼。电梯一次可以搭载三个人。那么，我们如何安排电梯以最短的时间将这五个人送到他们的楼层呢？

解决方案包括按降序将人们送到各自的楼层。让我们根据以下图片来处理这个场景：

![图 15.18 - 调度电梯示例](img/Figure_15.18_B15403.jpg)

图 15.18 - 调度电梯示例

让我们遍历这个场景的步骤：

1.  这是初始状态。电梯在地面层，有五个人准备搭乘。让我们假设最小时间为 0(所以，0 个时间单位)。

1.  在电梯中，我们带上了要去四楼的人和要去二楼的一个人。记住我们一次最多可以带三个人。到目前为止，最小时间为 0。

1.  电梯上升并停在二楼。一个人下去。因为每层代表一个时间单位，我们有一个最小时间为 2。

1.  电梯上升并停在四楼。剩下的两个人下去。最小时间变为 4。

1.  在这一步，电梯是空的。它必须下到地面层去接更多的人。因为它下降了四层，最小时间变为 8。

1.  我们接上剩下的两个人。最小时间保持为 8。

1.  电梯上升并停在一楼。一个人下去。最小时间变为 9。

1.  电梯上升并停在二楼。一个人下去。最小时间变为 10。

1.  在这一步，电梯是空的。它必须下到地面层。因为它下降了两层，最小时间变为 12。

因此，总最小时间为 12。基于这个场景，我们可以详细说明以下算法：

1.  按目的地降序对给定的数组进行排序。

1.  创建*k*人的组。每组所需的时间为 2 * *floors*[*group*]。

因此，对我们的测试数据进行排序将得到*floors* = {4, 4, 2, 2, 1}。我们有两组。一组包含三个人(4, 4, 2)，而另一组包含两个人(2, 1)。总最小时间为(2 * *floors*[0]) + (2 * *floors*[3]) = (2 * 4) + (2 * 2) = 8 + 4 = 12。

在代码方面，我们有以下内容：

```java
public static int time(int k, int floors[]) {
  int aux;
  for (int i = 0; i < floors.length - 1; i++) {
    for (int j = i + 1; j < floors.length; j++) {
      if (floors[i] < floors[j]) {
        aux = floors[i];
        floors[i] = floors[j];
        floors[j] = aux;
      }
    }
  }
  // iterate the groups and update 
  // the time needed for each group 
  int time = 0;
  for (int i = 0; i < floors.length; i += k) {
    time += (2 * floors[i]);
  }
  return time;
}
```

当然，你可能最终选择了一个更好的排序算法。完整的应用程序称为*ScheduleOneElevator*。这是本章的最后一个编码挑战。

### 调度多部电梯

但是如何安排多部电梯和任意数量的楼层呢？嗯，在面试中，你可能不需要为多部电梯实现解决方案，但你可能会被问到如何设计一个解决方案。

调度多部电梯和算法的问题是著名且困难的。对于这个问题并没有最佳算法。换句话说，创建一个可以应用于现实世界电梯调度的算法是非常困难的，而且显然已经被专利保护。

电梯算法(https://en.wikipedia.org/wiki/Elevator_algorithm)是一个很好的起点。在考虑如何为多部电梯设计解决方案之前，你必须列出你想要考虑的所有假设或约束条件的清单。每个可用的解决方案/算法都有一个关于楼层数、电梯数量、每部电梯的容量、平均人数、高峰时间、电梯速度、装载和卸载时间等的假设或约束条件的清单。主要有三种解决方案，如下：

+   **区域**：每部电梯分配到一个区域(它服务一部分楼层)。

+   **最近的电梯**：每个人被分配到最近的电梯（这是基于电梯的位置、呼叫的方向和电梯当前的方向）。

+   **考虑容量的最近电梯**：这类似于最近电梯选项，但它考虑了每部电梯的负载。

#### 部门

例如，一个有八层楼和三部电梯的建筑可以这样服务：

+   电梯 1 服务 1 楼、2 楼和 3 楼。

+   电梯 2 服务 1 楼、4 楼和 5 楼。

+   电梯 3 服务 1 楼、6 楼、7 楼和 8 楼。

每部电梯都服务一楼，因为一楼的到达率最高。

#### 最近的电梯

为每部电梯分配一个分数。这个分数代表了新人到来时电梯的适用性评分：

+   *朝呼叫方向，相同方向*：*FS* = (*N +* 2) - *d*

+   *朝呼叫方向，相反方向*：*FS* = (*N*+1) - *d*

+   *远离呼叫*：*FS* = 1

其中，*N* = #楼层 - 1，*d* = 电梯和呼叫之间的距离。

#### 考虑容量的最近电梯

这与最近电梯的情况完全相同，但它考虑了电梯的多余容量：

+   *朝呼叫方向，相同方向*：*FS* = (*N* + 2) - *d* + *C*

+   *朝呼叫方向，相反方向*：*FS* = (*N* + 1) - *d* + *C*

+   *远离呼叫*：*FS* = 1 + *C*

这里，*N*是#楼层 - 1，*d*是电梯和呼叫之间的距离，*C*是多余容量。

我强烈建议你搜索和学习这个问题的不同实现，并尝试学习你认为最适合你的那个。我建议你从这里开始：

+   [`github.com/topics/elevator-simulation`](https://github.com/topics/elevator-simulation)

+   [`austingwalters.com/everyday-algorithms-elevator-allocation/`](https://austingwalters.com/everyday-algorithms-elevator-allocation/).

现在，让我们总结一下这一章。

# 总结

在本章中，我们涵盖了最受欢迎的数学和谜题类问题。虽然许多公司避免这类问题，但仍然有像谷歌和亚马逊这样的主要参与者在面试中依赖这类问题。

练习这些问题对我们的大脑是一个很好的锻炼。除了数学知识，这些问题还能够支持基于推理和直觉的分析思维，这意味着它们对任何程序员都是很好的支持。

在下一章中，我们将讨论面试中的一个热门话题：并发（多线程）。