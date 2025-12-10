---
title: "MathJax 测试"
date: 2025-10-24
image: 
description: 测试公式编号
categories:
    - Test
tags:
    - Math
math: true
---

## 2. LaTeX 数学公式测试

FixIt 主题内置了对数学公式的支持（通常通过 KaTeX 或 MathJax 实现）。我们在本文的头部（Front Matter）已经设置了 `math: enable: true` 来启用它。

### 行内公式 (Inline)

你可以将公式嵌入在段落文本中。

例如：著名的质能方程是 $E = mc^2$，欧拉恒等式是 $e^{i\pi} + 1 = 0$。

### 块级公式 (Block)

对于复杂的公式，通常使其独占一行居中显示。

**高斯积分：**

$$
\int_{-\infty}^{\infty} e^{-x^2} \, dx = \sqrt{\pi}
$$

**矩阵示例：**

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

**多行公式对齐：**

$$
\begin{aligned}
f(x) &= (x+a)(x+b) \\
&= x^2 + (a+b)x + ab
\end{aligned}
$$

---

## 3. 图片测试

图片是博客的重要组成部分。

### 方式 A：使用网络图片链接

这是最简单的方式，直接引用一个外部 URL。下面是一张来自 Unsplash 的随机图片：

![示例网络图片](https://source.unsplash.com/random/800x400/?landscape)
*图注：这是一张网络图片*

### 方式 B：使用本地图片 (重要!)

在 Hugo 中使用本地图片通常有两种最佳实践。为了方便起见，我们先介绍最简单的一种：**`static` 目录法**。

**操作步骤：**

1. 在你的项目根目录下，找到或创建一个名为 `static` 的文件夹。
2. 在 `static` 里面再创建一个 `images` 文件夹。
3. 将你的一张图片（比如 `my-cat.jpg`）上传到 `static/images/` 目录中。
4. 在文章中使用下面的语法引用它（注意路径以 `/` 开头，并且**不包含** `static`）：

我们要引用当前文件夹里的emoji：

{{< image src="random.jpg" caption="随机表情包" id="fig-emoji" width="20%" >}}

如 [图 1](#fig-emoji) 所示。

$$
\varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$

测试自动编号：
$$
\begin{equation}
  E = mc^2 \label{eq:energy}
\end{equation}
$$


引用公式 \eqref{eq:energy}.

Hugo 非常快[^hugo]。Stack 主题很好看[^stack]。

[^hugo]: Steve Francia. "Hugo Docs". https://gohugo.io
[^stack]: CaiJimmy. "Stack Theme". https://github.com/CaiJimmy/hugo-theme-stack