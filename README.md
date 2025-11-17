# Academic Beamer Presentation Template

A clean and professional LaTeX Beamer template designed for academic presentations, featuring a 16:9 aspect ratio, customizable footline, and support for mathematical content, algorithms, and figures.

## Features

- **16:9 Aspect Ratio** - Modern widescreen format suitable for contemporary displays
- **Customizable Footline** - Shows author, title, and slide numbers
- **Clean Design** - Minimal distractions with a focus on content
- **Mathematical Support** - Full support for equations, algorithms, and mathematical notation
- **Figure Management** - Includes `subfigure`, `graphicx` for multi-panel figures
- **Bibliography Support** - Integrated `natbib` for citations
- **Algorithm Typesetting** - `algorithm` and `algpseudocode` packages included
- **Handout Mode** - Easy toggle between presentation and handout versions

## Quick Start

### Prerequisites

A LaTeX distribution with Beamer installed:
- **macOS**: MacTeX
- **Windows**: MiKTeX or TeX Live
- **Linux**: TeX Live

### Basic Usage

1. Clone or download this repository
2. Edit `slide_template.tex` with your content
3. Compile with:
   ```bash
   pdflatex slide_template.tex
   ```
   Or use `latexmk` for automatic recompilation:
   ```bash
   latexmk -pdf -pvc slide_template.tex
   ```

### File Structure

```
.
├── slide_template.tex          # Main template file
├── example_presentation.tex    # Complete working example
├── algorithm.sty              # Algorithm environment support
├── figures/                   # Directory for images
│   └── example_figure.png
└── README.md                  # This file
```

## Customization

### Author and Title

Edit the following lines in the preamble:

```latex
\author{Your Name}
\title{Your Presentation Title}
\date{Date or Event}
```

### Colors

The template uses default Beamer colors. To customize:

```latex
% Change title background color
\setbeamercolor{frametitle}{bg=blue!10, fg=black}

% Change bullet colors
\setbeamercolor{itemize item}{fg=blue}
```

### Aspect Ratio

The template uses 16:9 by default. To change:

```latex
% For 4:3 format (remove aspectratio option or use 43)
\documentclass[aspectratio=43, dvipsnames, handout]{beamer}
```

### Handout Mode

Remove `handout` from the document class to enable pause effects:

```latex
\documentclass[aspectratio=169, dvipsnames]{beamer}
```

## Template Structure

### Preamble

The template includes:
- Line spacing adjustment (1.15)
- Margins (12mm left/right)
- Custom footline with navigation symbols removed
- Essential packages for academic content

### Content Sections

```latex
% Title slide
\begin{frame}
    \titlepage
\end{frame}

% Table of contents
\begin{frame}{Outline}
    \tableofcontents
\end{frame}

% Regular content slides
\section{Your Section}
\begin{frame}{Frame Title}
    Your content here
\end{frame}
```

## Examples

### Equations

```latex
\begin{frame}{Mathematical Content}
    Inline equation: $E = mc^2$
    
    Display equation:
    \begin{equation}
        \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
    \end{equation}
\end{frame}
```

### Algorithms

```latex
\begin{frame}{Algorithm Example}
    \begin{algorithm}[H]
        \caption{Your Algorithm}
        \begin{algorithmic}[1]
            \State Initialize parameters
            \For{$i = 1$ to $n$}
                \State Process step $i$
            \EndFor
        \end{algorithmic}
    \end{algorithm}
\end{frame}
```

### Figures

```latex
\begin{frame}{Figure Example}
    \begin{figure}
        \centering
        \includegraphics[width=0.6\textwidth]{figures/example.png}
        \caption{Your figure caption}
    \end{figure}
\end{frame}
```

### Two-Column Layout

```latex
\begin{frame}{Two Columns}
    \begin{columns}
        \column{0.48\textwidth}
        Left column content
        
        \column{0.48\textwidth}
        Right column content
    \end{columns}
\end{frame}
```

## Included Packages

| Package | Purpose |
|---------|---------|
| `xcolor` | Color support |
| `graphicx` | Image inclusion |
| `subfigure` | Multi-panel figures |
| `booktabs` | Professional tables |
| `multirow` | Table cell spanning |
| `algorithm` | Algorithm floating environment |
| `algpseudocode` | Pseudocode typesetting |
| `natbib` | Bibliography management |
| `amsmath`, `amsfonts`, `amssymb` | Mathematical symbols and environments |
| `dsfont` | Double-stroke fonts (blackboard bold) |
| `tikz` | Graphics and diagrams |
| `mathtools` | Extended math environments |

## Tips and Best Practices

### Content Guidelines
- **One main idea per slide** - Keep slides focused
- **Use bullet points** - Break down complex ideas
- **Limit text** - Aim for 5-7 lines maximum per slide
- **Visual aids** - Use figures and diagrams to illustrate concepts

### Design Tips
- **Consistent formatting** - Maintain uniform style throughout
- **Readable fonts** - Ensure text is visible from the back of the room
- **High contrast** - Use sufficient color contrast for visibility
- **Progressive reveal** - Use `\pause` to build content gradually

### Technical Tips
- **Test compilation** - Always test-compile before your presentation
- **PDF compatibility** - Verify animations work in your PDF viewer
- **File organization** - Keep figures in a separate directory
- **Version control** - Use Git to track changes to your slides

## Compilation

### Using pdflatex

```bash
pdflatex slide_template.tex
pdflatex slide_template.tex  # Run twice for references
```

### Using latexmk (Recommended)

```bash
# Compile once
latexmk -pdf slide_template.tex

# Continuous preview mode
latexmk -pdf -pvc slide_template.tex

# Clean auxiliary files
latexmk -c
```

### Common Issues

**Problem**: Bibliography not appearing
- **Solution**: Run `bibtex` after first `pdflatex` compile
  ```bash
  pdflatex slide_template.tex
  bibtex slide_template
  pdflatex slide_template.tex
  pdflatex slide_template.tex
  ```

**Problem**: Images not found
- **Solution**: Check file paths and ensure images are in the correct directory

**Problem**: Font size warnings
- **Solution**: These are usually harmless - LaTeX substitutes the closest available size

## License

This template is provided as-is for academic and personal use. Feel free to modify and distribute.

## Contributing

Suggestions and improvements are welcome! Please feel free to:
- Report issues
- Submit pull requests
- Share your customizations

## Credits

Originally adapted from academic presentation best practices. Modified for clarity and modern LaTeX standards.

## Contact

For questions or suggestions, please open an issue in the repository.

---

**Version**: 1.0  
**Last Updated**: November 2025
