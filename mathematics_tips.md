# Mathematics tips for LaTeX

## Matrix transpose

$A^\intercal$

```latex
\[A^\intercal\]
```

[reference](https://tex.stackexchange.com/questions/30619/what-is-the-best-symbol-for-vector-matrix-transpose)

## Vector bold representation

```latex
...
\usepackage{bm}

...
\[\bm{\theta}\]
...
```

[reference](https://tex.stackexchange.com/questions/3238/bm-package-versus-boldsymbol)

If the `bm` package is not available, you can use `\boldsymbol{\theta}` alternatively.

## Cases

```latex
...
\usepackage{amsmath}
...
\[
I_A = 
\begin{cases}
0 & \text{if } A \text{ does not occur}\\
1 & \text{if } A \text{ occurs}
\end{cases}
\]
```

[reference](https://tex.stackexchange.com/questions/262079/typesetting-a-function-defined-by-case-analysis/262081)

## The not sign

Often we want to achieve a 'centered not' sign. Use `centernot`!

```latex
...
\usepackage{centernot}
...
\[X \centernot = Y\]
```

## The empty set sign

The `\emptyset` produces an ugly sign: $\emptyset$. It's preferred by many to use `\varnothing` from the `amssymb` package.

[reference](https://tex.stackexchange.com/a/22799)

## Vector norm 2

```latex
...
\usepackage{mathtools}
...
\DeclarePairedDelimiter\norm{\lVert}{\rVert}
...
\[\norm{x}\]
```

## Underbrace

```latex
\[\underbrace_{x + y}_{\text{the text}} + z = 1\]
```

## Prefered \operatorname

When we have to type some function in math mode, we may want the function name to remain normal text rather than rendered as math mode. `\operatorname{}` is prefered among the options.

`\operatorname{sin} x` produces $\operatorname{sin} x$

`\mathrm{sin} x` produces $\mathrm{sin} x$

`\text{sin} x` produces $\text{sin} x$

## The `argmax` function

```latex
\[
\operatorname{\underset{\theta}{\arg\max}} f(\theta)
\]
```

$\operatorname{\underset{\theta}{\arg\max}} f(\theta)$

## Auto linebreaks in `align` equations

`breqn` and `autobreak`

## Package conflicts between `amssymb` and `unicode-math`

- https://tex.stackexchange.com/questions/549933/symbol-eth-already-defined-when-using-libertinus-otf-and-lualatex-pandoc/549938#549938
- https://github.com/sjtug/SJTUThesis/issues/502

## Placing the equation numbers level with the last line

If you use `split` environments, then you need to pass `tbtags` option to the `amsmath` package:
```latex
\usepackage[tbtags]{amsmath} % For placing the equation numbers level with the last line when using split environment
```

However, this often cause the "option clash" error, since many other packages like `mathtools` and `amsthm` load `amsmath` as well. Thus, it is recommended to put the above line at the top, before loading other packages.

If you use `aligned` environments, then passing `[b]` option will be enough:
```latex
\begin{equation}\label{eq:test}
  \begin{aligned}[b]
    a &= b\\
    &= c\\
    &= d.
  \end{aligned}
\end{equation}
```

References:
- [equations - What's the difference between split and aligned? - TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/187938/whats-the-difference-between-split-and-aligned)
