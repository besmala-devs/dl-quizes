# DL Quizzes

Practice quizzes for my Deep Learning chapters: true/false, single choice, multiple answers, open questions and a midterm-style quiz for each chapter.

**Open the site:** [Study quizzes](https://besmala-devs.github.io/dl-quizes/)

## Add a chapter

1. Generate the chapter quiz as a JSON file, for example `ch7_quiz.json`.
2. Upload it to the root of this repo, next to `index.html`.
3. A GitHub Action updates `manifest.json` and the site picks up the new chapter after Pages rebuilds, usually within a minute or two.

## Files

| File | Purpose |
|---|---|
| `index.html` | The quiz app (reads every `.json` quiz file in this folder) |
| `chX_quiz.json` | One file per chapter |
| `manifest.json` | List of quiz files, generated automatically |
| `.github/workflows/manifest.yml` | Regenerates `manifest.json` on each push |

## Run locally

Open the page through a local server (double-clicking `index.html` blocks loading the JSON files):

```
python -m http.server
```

Then visit http://localhost:8000.
