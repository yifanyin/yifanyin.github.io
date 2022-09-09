---
title: "Latex how-to"
aliases:
- Latex how-to
tags:
- how-to
---

I may not use a micro-filled Latex package ever again after the [[notes/How to graduate in D-ERDW|doctoral thesis]]. But here are some pretty neat tricks I learned along the way. First, acknowledgement to the [awesome template](https://github.com/uio-latex/phduio-article-based) provided by Uni Oslo.

# Bibliography
- Add page references after the bibliography entries: `\usepackage[backref=true]{biblatex}`
- Add doi links
```latex
\RequirePackage{doi} % Ignore LaTeX syntax in DOI links
\renewcommand{\doitext}{doi:\space}
```