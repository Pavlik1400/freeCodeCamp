---
title: Np Completeness
localeTitle: Np完整性
---
## Np完整性

NP-Complete是某些类型问题的属性。如果问题是NP-Complete，则意味着没有有效的（多项式）算法来快速找到解决方案。但是，如果给我们一个解决方案，我们可以快速（在多项式时间内）验证它是否正确。

更具体一点，让我们检查一个已知的NP-Complete问题 - 子集和问题。假设我们有一组整数{-7，-3，-2,5,8}。我们想要找到这些整数的子集，其元素总和为0.我们怎么能这样做？

一种方法是简单地枚举所有可能的子集并检查它们的元素是否总和为0.这将是指数级复杂的。

事实上，没有更好的已知算法，它可以改善指数时间限制。这就是为什么它被归类为NP-Complete问题。

除了已知为NP-Complete的子集和问题之外，存在许多这样的已知问题。如果找到一个有效的算法，则意味着我们可以为所有NP-Complete问题设计一个有效的算法。

如果你有一个可以被证明是NP完全的问题，你应该停止尝试为它找到更有效的算法，而是使用启发式方法来解决大多数测试用例的问题，或者解决问题的近似版本。或者也许检查你正在解决的问题，看看它是否不能简化为不完全NP的东西。

#### 更多信息：

https://www.ics.uci.edu/~eppstein/161/960312.html https://stackoverflow.com/questions/210829/what-is-an-np-complete-in-computer-science