# CV

Simple Markdown → PDF CV workflow.

## Edit from your phone

1. Open `cv.md` on GitHub.
2. Tap **Edit**.
3. Change the content.
4. Commit the change.
5. Open the **Actions** tab.
6. Open the latest `Build CV` run.
7. Download the `cv-pdf` artifact.

You can also run the build manually from:

**Actions → Build CV → Run workflow**

## Local build

If you have Docker installed:

```bash
docker run --rm -v "$PWD:/data" pandoc/latex:latest   cv.md --standalone --pdf-engine=xelatex -o cv.pdf
```
