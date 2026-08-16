# CV

Modern Markdown → PDF CV workflow based on Pandoc and GitHub Actions.

## How to edit from your phone

1. Open `cv.md` on GitHub.
2. Tap **Edit**.
3. Change the text.
4. Commit the change.
5. Open **Actions → Build CV**.
6. Download the `cv-pdf` artifact from the latest successful run.

## Main files

```text
cv.md
template.tex
.github/workflows/build-cv.yml
```

## Change the accent color

Edit this line in `cv.md`:

```yaml
accentcolor: "0A66C2"
```

Examples:

```yaml
accentcolor: "0A66C2" # blue
accentcolor: "2563EB" # modern blue
accentcolor: "059669" # green
accentcolor: "7C3AED" # purple
accentcolor: "DC2626" # red
accentcolor: "EA580C" # orange
```

## Local build with Docker

```bash
docker run --rm -v "$PWD:/data" pandoc/latex:latest \
  cv.md --standalone --template=template.tex --pdf-engine=xelatex -o cv.pdf
```
