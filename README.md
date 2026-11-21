# Personal website

A minimal Quarto website with five sections. The original notes were copied into this project; editing the originals elsewhere will not automatically update these copies.

## Preview and update

From this folder, run:

```sh
quarto preview
```

To rebuild the published files after editing:

```sh
quarto render
```

The generated website is in `docs/`. Commit both the source files and `docs/` when publishing an update. Keep `docs/.nojekyll` in the repository. Quarto's `_freeze/` folder preserves executed output and can also be committed.

The current notes use the R packages `knitr`, `rmarkdown`, `sortedvector`, `dslabs`, and `tidyverse`. These are installed on the computer used for the initial build. GitHub Pages serves the already rendered files and does not need R or these packages.

## Publish with GitHub Pages

Use this folder as the root of a dedicated GitHub repository (not the surrounding cycling project or home directory).

The repository is `AustinCo03/personal_website`. In **Settings → Pages**, set the source to **GitHub Actions**. The included Publish website workflow deploys `docs/` whenever changes are pushed to `main`. It can also be run manually from the Actions tab.

Site address: https://AustinCo03.github.io/personal_website/

Official publishing guide: https://quarto.org/docs/publishing/github-pages.html

## Add content

- **LeetCode:** add a `.qmd` file in `leetcode/`, link it from `leetcode/index.qmd`, and add it to the LeetCode sidebar in `_quarto.yml`.
- **Textbooks:** create a folder for each book under `textbooks/`, with an `index.qmd` and notes. Link the book from `textbooks/index.qmd`, and add a book section and note links to the Textbooks sidebar in `_quarto.yml`.
- **training, ramblings, research papers:** their `index.qmd` pages currently contain only a title. Add text or links to future `.qmd` posts there.

Run `quarto render` after changes, then publish the updated files.
