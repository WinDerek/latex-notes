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
