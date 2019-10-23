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
