# Miscellaneous tips

## Double quotes

```latex
``quoted text''
```

## Indent a block of text

```latex
\documentclass{article}
\usepackage{scrextend}
\usepackage{lipsum}% for demo only!
\begin{document}

\lipsum[1]
\begin{addmargin}[1em]{2em}% 1em left, 2em right
\lipsum[2]
\end{addmargin}
\lipsum[3]
\end{document}
```

[https://tex.stackexchange.com/questions/37080/how-can-i-indent-a-block-of-text-for-a-specified-amount/37084](https://tex.stackexchange.com/questions/37080/how-can-i-indent-a-block-of-text-for-a-specified-amount/37084)

## Dash symbols

- Hyphen: `-`
- En-dash: `--`, `\textendash` (`\textendash{}` in case there is text after this)
- Em-dash: `---`, `\textemdash{}`, (`\textemdash{}` in case there is text after this)

## Math fonts

Including some packages may implicitly change the math font globally. For example, usage of `\usepackage{fdsymbol}` in IEEE conference will change the math font to the ACM-like style.

## Spacing

```latex
\, thin space (normally 1/6 of a quad);
\> medium space (normally 2/9 of a quad);
\; thick space (normally 5/18 of a quad);
\! negative thin space (normally 1/6 of a quad).
```

[reference](https://tex.stackexchange.com/a/9092/216629)

## `\input` v.s. `\include`

[reference](https://tex.stackexchange.com/a/250)

## Always put `\label` after `\caption`

[reference](https://tex.stackexchange.com/questions/32325/why-does-an-environments-label-have-to-appear-after-the-caption)
