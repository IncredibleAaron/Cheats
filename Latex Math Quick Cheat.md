## Latex Math Quick Cheat



**For all** | $ \forall $ -- `\forall`

# Math Formatting on Markdown

This page is to test a new feature of [FSharp.Formatting](http://tpetricek.github.io/FSharp.Formatting/)
which can use [mathjax](http://www.mathjax.org/) to render mathematical formulas written in LaTeX. 
The extended FSharp.Formatting markdown supports two styles:

- inline math: using `$ {latex} $`
- block mode math: start a block by first line `$$$`

The source of this page can be found [here](https://github.com/soloman817/CUDALab/blob/master/source/02.CUDALab%20Usage/01.Math%20Formatting%20on%20Markdown.md).

## Inline Math

A simple inline equation looks like $ \alpha + \beta + x^{2} = z^{2} $ or $ \frac{1}{2^{-32} - 1} $.

Some more examples:

- $ \forall x \in X, \quad \exists y \leq \epsilon $
- $ \alpha, A, \beta, B, \gamma, \Gamma, \pi, \Pi, \phi, \varphi, \Phi $
- $ \cos (2\theta) = \cos^2 \theta - \sin^2 \theta $
- $ \lim_{x \to \infty} \exp(-x) = 0 $
- $ a \bmod b $
- $ x \equiv a \pmod b $
- $ k_{n+1} = n^2 + k_n^2 - k_{n-1} $
- $ f(n) = n^5 + 4n^2 + 2 |_{n=17} $
- $ \frac{n!}{k!(n-k)!} = {n \choose k} $
- $ \frac{\frac{1}{x}+\frac{1}{y}}{y-z} $
- $ \sqrt{\frac{a}{b}} $
- $ \sqrt[n]{1+x+x^2+x^3+\ldots} $
- $ \sum_{i=1}^{10} t_i $
- $ \int_0^\infty \mathrm{e}^{-x}\,\mathrm{d}x $
- $ \int\limits_a^b $
- $ ( a ), [ b ], \{ c \}, | d |, \| e \|, \langle f \rangle,
  \lfloor g \rfloor, \lceil h \rceil, \ulcorner i \urcorner $
- $ ( \big( \Big( \bigg( \Bigg( $

## Block Math

To write compilcated math, use block math. The first line must be `$$$`, followed by the LaTex code.
All block math is centered.

$$$
\begin{equation}
f(x)=3x^{2}+6(x-2)-1
\end{equation}

$$$
\begin{equation}
  x = a_0 + \cfrac{1}{a_1
          + \cfrac{1}{a_2
          + \cfrac{1}{a_3 + \cfrac{1}{a_4} } } }
\end{equation}

LaTex array environments are also supported:

$$$
\begin{equation}
A=\left(\begin{array}{c|c}
a_{11} & a_{12} \\ \hline
a_{21} & a_{22}
\end{array}\right)
\end{equation}

$$$
\begin{equation*}
\left.%
\begin{array}{>{\kaishu} r c@{}l@{}l}
\text{constant})	& y & = & c  \\
\text{line})		& y & = & cx + d  \\
\text{parabola})	& y & = & bx^{2} + cx + d  \\
\end{array}\right\} \text{polynomial}
\end{equation*}

To make multiplication visually similar to a fraction, a nested array can be used,
for example multiplication of numbers written one below the other.

$$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      \left( x_1 x_2 \right)\\
      \times \left( x'_1 x'_2 \right)
    \end{array}
  }{
    \left( y_1y_2y_3y_4 \right)
  }
\end{equation}

Matrices:

$$$
\begin{matrix}
  a & b & c \\
  d & e & f \\
  g & h & i
\end{matrix}

$$$
\begin{matrix}
  -1 & 3 \\
  2 & -4
 \end{matrix}
 =
 \begin{matrix}
  -1 & 3 \\
  2 & -4
 \end{matrix}

$$$
A_{m,n} =
 \begin{pmatrix}
  a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
  a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
  \vdots  & \vdots  & \ddots & \vdots  \\
  a_{m,1} & a_{m,2} & \cdots & a_{m,n}
 \end{pmatrix}

$$$
M = \begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\[0.3em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.3em]
       0           & \frac{5}{6} & \frac{1}{6}
     \end{bmatrix}

$$$
\begin{equation}
f(n) = \left\{ 
  \begin{array}{l l}
    n/2 & \quad \text{if $n$ is even}\\
    -(n+1)/2 & \quad \text{if $n$ is odd}
  \end{array} \right\}
\end{equation}

## Escape

- If you only have one $ in one paragraph, you don't need to escape it.
- If you have two \$ in one paragraph, like here another \$ here, then you need use `\$`
  to escape.
- Escape \$ in inline mode: $ \$ $, $ \$var $
- Other escapes: $ \& \% \$ \# \_ \{ \} $
- Using < or >: $ x > 1 $, $ y < 1 $, $ x >= 1 $, $ y <= 1 $, $ x = 1 $
- Using <tag>: $ <p>something</p> $




