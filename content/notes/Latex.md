---
title: "Latex"
alias: Latex
DocumentClass: manual
tags:
- how-to
- math
---

I may not use a micro-filled Latex package ever again after the [[notes/How to graduate in D-ERDW|doctoral thesis]]. But here are some pretty neat tricks I learned along the way. First, acknowledgement to the [awesome template](https://github.com/uio-latex/phduio-article-based) provided by Uni Oslo.

Beside serious documents, there are other flavors of Latex math in web applications. [[notes/Obsidian|Obsidian]] use MathJax instead of Katex for equation rendering. Some syntax are different.

# Greek alphabet
|alphabet|spelling|
|---|---|
|$\alpha$ | alpha |
|$\beta$|beta|
|$\gamma$|gamma
|$\delta$|delta
|$\epsilon$|epsilon
|$\zeta$|zeta
|$\eta$|eta
|$\lambda$|lambda
|$\mu$|mu
|$\nu$|nu
|$\xi$|xi
|$\chi$|chi|


# Equations
|symbol|latex|
|---|---|
|$\sim$|sim|
|$\approx$|approx|
|$\lesssim$|lesssim|
|$\gtrsim$|gtrsim|
|$\leq$|leq|
|$\geq$|geq|
|$\propto$|propto|

# Bibliography
- Add page references after the bibliography entries: `\usepackage[backref=true]{biblatex}`
- Add doi links
```latex
\RequirePackage{doi} % Ignore LaTeX syntax in DOI links
\renewcommand{\doitext}{doi:\space}
```

# Producing document
- To remove the `hyperref` colored frames, change the package settings to `colorlinks=true`
- 