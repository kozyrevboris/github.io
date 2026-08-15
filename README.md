# Boris Kozyrev — academic job-market website template

This is a static HTML/CSS website inspired by the clean, minimal structure of Tanja Linta's academic site, adapted to the navigation:

**Boris Kozyrev | CV | Research | Policy Work**

It does not require Quarto, Jekyll, R, Python, or a database. GitHub Pages can serve these files directly.

## 1. Files in this template

```text
boris_job_market_tanja_style/
├── index.html                # Home page
├── cv.html                   # Short CV panel + full local PDF link
├── research.html             # JMP, working papers, work in progress
├── policy.html               # Policy work
├── styles.css                # Site appearance
├── .nojekyll                 # Makes GitHub Pages serve files as-is
├── assets/
│   └── profile-placeholder.svg
└── files/
    └── README.txt
```

## 2. Where to put your photo

Put your headshot in:

```text
assets/profile.jpg
```

Then, in `index.html`, change:

```html
src="assets/profile-placeholder.svg"
```

to:

```html
src="assets/profile.jpg"
```

A portrait-oriented JPG around 800×1000 px is more than sufficient.

## 3. Where to put your CV

Copy your CV PDF to:

```text
files/Boris_Kozyrev_CV.pdf
```

The Home and CV pages already link to this exact path. No Dropbox link is used.

When the site is published at, for example, `https://boriskozyrev.com`, the browser will access the PDF directly as:

```text
https://boriskozyrev.com/files/Boris_Kozyrev_CV.pdf
```

## 4. Where to put the Job Market Paper

Copy the paper to:

```text
files/Boris_Kozyrev_JMP.pdf
```

Optional associated files:

```text
files/Boris_Kozyrev_JMP_Slides.pdf
files/Boris_Kozyrev_JMP_Appendix.pdf
```

The Home page and Research page already point to these paths.

This means the JMP can be opened directly from your website without Dropbox or another third-party document host.

## 5. Other research PDFs

The draft uses these example filenames:

```text
files/Working_Paper_1.pdf
files/Working_Paper_1_Slides.pdf
files/Working_Paper_2.pdf
```

Either use those filenames or edit the corresponding `href` values in `research.html`.

For a new paper, duplicate one `<article class="paper"> ... </article>` block and change the title, metadata, abstract, and file links.

## 6. Policy work PDFs

Put them in the same `files/` directory, for example:

```text
files/Policy_Work_1.pdf
files/Policy_Work_2.pdf
```

Then edit `policy.html`.

## 7. What to replace

Search all HTML files for these strings:

- `YOUR`
- `PASTE`
- `COAUTHOR`
- `EXPECT`
- `SELECTED`

Those mark content that still needs your information.

## 8. Recommended filenames

Use stable, human-readable filenames. Avoid spaces and temporary version labels.

Recommended:

```text
Boris_Kozyrev_CV.pdf
Boris_Kozyrev_JMP.pdf
Boris_Kozyrev_JMP_Slides.pdf
Kozyrev_Coauthor_Forecast_Combinations.pdf
```

Avoid:

```text
CV_final_FINAL_v4.pdf
jmp_new_august_14.pdf
paper(7).pdf
```

## 9. Publishing on GitHub Pages

A simple setup is a public repository named:

```text
YOURGITHUBUSERNAME.github.io
```

Upload the *contents* of this folder to the root of that repository, so `index.html` is at the repository root.

In GitHub:

1. Open **Settings** → **Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/ (root)`.
4. Save.

GitHub Pages will then serve `index.html` as the homepage and everything in `files/` as normal static files.

## 10. Custom domain

Later you can connect a personal domain such as `boriskozyrev.com`. The PDF URLs then remain on that same domain.

The important principle is: keep papers *inside this repository* under `files/`. That avoids institutional restrictions on Dropbox and similar services.

## 11. Job-market homepage logic

The Home page intentionally stays short:

1. Name and affiliation
2. One-sentence research identity
3. Email + CV
4. Job-market statement
5. Direct JMP link

More detailed paper information belongs on the Research page.
