# Quick Start Guide

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/beamer-academic-template.git
   cd beamer-academic-template
   ```

2. **Verify LaTeX installation:**
   ```bash
   pdflatex --version
   ```

3. **Compile the example:**
   ```bash
   pdflatex example_presentation.tex
   ```

## Creating Your First Presentation

### Method 1: Start from Template

1. Copy `slide_template.tex` to a new file:
   ```bash
   cp slide_template.tex my_presentation.tex
   ```

2. Edit the preamble with your information:
   ```latex
   \title{Your Title}
   \author{Your Name}
   \date{Your Date}
   ```

3. Add your content between `\begin{document}` and `\end{document}`

4. Compile:
   ```bash
   pdflatex my_presentation.tex
   ```

### Method 2: Start from Example

1. Copy `example_presentation.tex`:
   ```bash
   cp example_presentation.tex my_presentation.tex
   ```

2. Edit sections and replace with your content

3. Compile as above

## Basic Structure

```latex
\documentclass[aspectratio=169, dvipsnames]{beamer}
\usetheme{default}

% ... preamble settings ...

\title{Your Title}
\author{Your Name}
\date{Date}

\begin{document}

% Title slide
\begin{frame}
    \titlepage
\end{frame}

% Content slides
\section{Introduction}
\begin{frame}{Frame Title}
    Your content here
\end{frame}

\end{document}
```

## Common Tasks

### Adding a New Slide

```latex
\begin{frame}{Your Title}
    \begin{itemize}
        \item Point 1
        \item Point 2
        \item Point 3
    \end{itemize}
\end{frame}
```

### Adding an Equation

```latex
\begin{frame}{Equations}
    \begin{equation}
        E = mc^2
    \end{equation}
\end{frame}
```

### Adding an Image

```latex
\begin{frame}{Figure}
    \begin{figure}
        \centering
        \includegraphics[width=0.6\textwidth]{figures/image.png}
        \caption{Caption text}
    \end{figure}
\end{frame}
```

### Two-Column Layout

```latex
\begin{frame}{Two Columns}
    \begin{columns}
        \column{0.48\textwidth}
        Left content
        
        \column{0.48\textwidth}
        Right content
    \end{columns}
\end{frame}
```

### Progressive Reveal

Add `\pause` between items:

```latex
\begin{frame}{Incremental}
    \begin{itemize}
        \item First point
        \pause
        \item Second point (appears after click)
        \pause
        \item Third point (appears after another click)
    \end{itemize}
\end{frame}
```

## Customization

### Change Colors

```latex
% Title background
\setbeamercolor{frametitle}{bg=blue!10, fg=black}

% Block colors
\setbeamercolor{block title}{fg=white, bg=cyan!50!black}
\setbeamercolor{block body}{bg=cyan!10}
```

### Handout vs. Presentation Mode

**Presentation mode** (with pauses):
```latex
\documentclass[aspectratio=169, dvipsnames]{beamer}
```

**Handout mode** (no pauses):
```latex
\documentclass[aspectratio=169, dvipsnames, handout]{beamer}
```

### Change Aspect Ratio

**16:9 (default):**
```latex
\documentclass[aspectratio=169]{beamer}
```

**4:3 (traditional):**
```latex
\documentclass[aspectratio=43]{beamer}
```

## Compilation Tips

### Single Compilation
```bash
pdflatex my_presentation.tex
```

### With Bibliography
```bash
pdflatex my_presentation.tex
bibtex my_presentation
pdflatex my_presentation.tex
pdflatex my_presentation.tex
```

### Using latexmk (Recommended)
```bash
# Compile once
latexmk -pdf my_presentation.tex

# Continuous preview (auto-recompile on save)
latexmk -pdf -pvc my_presentation.tex

# Clean auxiliary files
latexmk -c
```

## Directory Structure

Organize your files:

```
my_project/
├── my_presentation.tex      # Your main file
├── algorithm.sty            # Algorithm support
├── figures/                 # Images
│   ├── figure1.png
│   └── figure2.pdf
└── bibliography.bib         # References (if needed)
```

## Troubleshooting

### Images Not Found
- Ensure images are in the correct directory
- Use relative paths: `figures/image.png`
- Check file extensions match actual files

### Font Warnings
- Usually safe to ignore
- LaTeX substitutes closest available size

### Bibliography Issues
- Run `bibtex` after first `pdflatex`
- Ensure `.bib` file exists
- Run `pdflatex` twice after `bibtex`

## Next Steps

1. Check `example_presentation.tex` for more examples
2. Read full documentation in `README.md`
3. Customize colors and layout to your preference
4. Practice compiling and viewing your presentation

## Getting Help

- Check the example file for syntax
- Consult [Beamer documentation](https://ctan.org/pkg/beamer)
- Search for specific LaTeX commands online
- Open an issue in the repository

Happy presenting! 🎉
