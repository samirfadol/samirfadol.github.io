# Updating Your Website

Your site is built from simple text files. After you edit and push to `main`, GitHub Actions rebuilds and publishes the site within about two minutes.

## Add a new paper

1. Open `data/papers.yaml` in the GitHub editor (or locally).
2. Add a new entry at the top of the list:

```yaml
- title: "Your Paper Title"
  authors: ["Samir A. Fadol", "Coauthor Name"]
  year: 2026
  status: "working paper"
  venue: ""
  pdf: "files/your-paper.pdf"
  link: ""
  abstract: ""
  job_market_paper: false
  tags: ["keyword"]
```

3. Upload the PDF to `static/files/your-paper.pdf`.
4. Commit and push.

**Status options:** `working paper`, `work in progress`, `under review`, `revise and resubmit`, `accepted`, `published`

## Mark a paper as published

Edit the paper's entry in `data/papers.yaml`:
- Change `status` to `"published"`
- Add the journal name in `venue`

## Designate your job market paper

Set `job_market_paper: true` on one entry in `data/papers.yaml`. Only one paper should have this flag.

## Update your bio

Edit `content/_index.md`. The text under the front matter (`---`) is your About section.

## Update your CV

Replace `static/files/cv.pdf` with your new CV. Keep the filename exactly `cv.pdf` so the navigation link keeps working.

## Change your photo

Replace `static/images/photo.jpg` with a new headshot (square or portrait works best).

## Add a teaching entry

Edit `data/teaching.yaml`:

```yaml
- course: "Course Name"
  role: "Teaching Fellow"
  institution: "University Name"
  term: "Fall 2026"
```

## Add an award

Edit `data/awards.yaml`:

```yaml
- title: "Award Name"
  institution: "Institution"
  year: 2026
  description: "Optional one-line description."
```

## Add a blog post

Create a new folder and file: `content/blog/your-post-slug/index.md`

```yaml
---
title: "Post Title"
date: 2026-03-15
description: "One-sentence summary."
---
Your post content here.
```

Then add a Blog item to the menu in `hugo.yaml` if you want it in the navigation.

## Change site settings

Edit `hugo.yaml` for your name, email, tagline, social links, and navigation menu.

## Remove the footer credit

In `hugo.yaml`, set:

```yaml
params:
  mysite:
    credit: false
```

## Need help?

Push your changes to `main` and check the **Actions** tab in GitHub if the site doesn't update. A failed build usually means a typo in a YAML file — check indentation (use spaces, not tabs).
