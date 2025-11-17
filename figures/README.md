# Figures Directory

Place your presentation figures and images in this directory.

## Supported Formats

- **PNG** - Recommended for screenshots and photos
- **PDF** - Best for vector graphics and plots
- **JPG/JPEG** - For photographs
- **EPS** - For older vector graphics (will be converted)

## Usage

In your LaTeX file:

```latex
\begin{frame}{Example Figure}
    \begin{figure}
        \centering
        \includegraphics[width=0.6\textwidth]{figures/your_image.png}
        \caption{Your caption here}
    \end{figure}
\end{frame}
```

## Best Practices

1. **Resolution**: Use at least 300 DPI for images
2. **File size**: Optimize images to keep PDF size reasonable
3. **Naming**: Use descriptive names without spaces (use underscores)
4. **Format**: Prefer PNG for plots, PDF for vector graphics

## Example File Structure

```
figures/
├── framework_diagram.pdf
├── results_plot.png
├── architecture.png
└── comparison_chart.pdf
```

## Tips

- Keep images high-quality but reasonably sized
- Use vector formats (PDF) for scalable graphics
- Test image visibility on projectors
- Ensure sufficient contrast for visibility
