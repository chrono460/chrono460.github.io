---
title: "MathJax Test"
date: 2025-10-24
image: 
description: Testing formula numbering
categories:
    - Test
tags:
    - Math
math: true
---

## 2. LaTeX Math Formula Test

The FixIt theme has built-in support for mathematical formulas (usually implemented via KaTeX or MathJax). We have enabled it by setting `math: enable: true` in the header (Front Matter) of this article.

### Inline Formulas

You can embed formulas within paragraph text.

For example: The famous mass-energy equivalence is $E = mc^2$, and Euler's identity is $e^{i\pi} + 1 = 0$.

### Block Formulas

For complex formulas, they are usually displayed centered on their own line.

**Gaussian Integral:**

$$
\int_{-\infty}^{\infty} e^{-x^2} \, dx = \sqrt{\pi}
$$

**Matrix Example:**

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

**Multi-line Equation Alignment:**

$$
\begin{aligned}
f(x) &= (x+a)(x+b) \\
&= x^2 + (a+b)x + ab
\end{aligned}
$$

---

## 3. Image Test

Images are an important part of a blog.

### Method A: Using Network Image Links

This is the simplest way, directly referencing an external URL. Below is a random image from Unsplash:

![Example Network Image](https://source.unsplash.com/random/800x400/?landscape)
*Caption: This is a network image*

### Method B: Using Local Images (Important!)

There are usually two best practices for using local images in Hugo. For convenience, we will first introduce the simplest one: the **`static` directory method**.

**Steps:**

1. In your project root directory, find or create a folder named `static`.
2. Create an `images` folder inside `static`.
3. Upload one of your images (e.g., `my-cat.jpg`) to the `static/images/` directory.
4. Use the following syntax to reference it in the article (note the path starts with `/` and **does not include** `static`):

We want to reference an emoji in the current folder:

{{< image src="random.jpg" caption="Random Emoji" id="fig-emoji" width="20%" >}}

As shown in [Figure 1](#fig-emoji).

Interactive demo presentation:
{{< demo-collapsible src="/demos/pbr.html" height="500px" title="Physical Lighting">}}

$$
\varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$

Testing automatic numbering:
$$
\begin{equation}
  E = mc^2 \label{eq:energy}
\end{equation}
$$

Referencing formula \eqref{eq:energy}.

Hugo is very fast[^hugo]. The Stack theme is very beautiful[^stack].

[^hugo]: Steve Francia. "Hugo Docs". https://gohugo.io
[^stack]: CaiJimmy. "Stack Theme". https://github.com/CaiJimmy/hugo-theme-stack