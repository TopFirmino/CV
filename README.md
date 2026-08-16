# CV

Modern Markdown → PDF CV workflow based on Pandoc and GitHub Actions.

This version uses `pdflatex` instead of `xelatex` and avoids `fontspec`, `titlesec`, and other extra LaTeX packages. It is intended to work better with the minimal `pandoc/latex:latest` Docker image.

## Edit from your phone

1. Open `cv.md` on GitHub.
2. Tap **Edit**.
3. Change the text.
4. Commit the change.
5. Open **Actions → Build CV**.
6. Download the `cv-pdf` artifact from the latest successful run.

## Files

```text
cv.md
template.tex
.github/workflows/build-cv.yml
```

## Change accent color

Edit this line in `cv.md`:

```yaml
accentcolor: "0A66C2"
```

Examples:

```yaml
accentcolor: "2563EB" # blue
accentcolor: "059669" # green
accentcolor: "7C3AED" # purple
accentcolor: "EA580C" # orange
```
