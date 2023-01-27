<h1 align="center">
    Logseq-Hugo-Template
</h1>

<p align="center">
    <a href="https://github.com/CharlesChiuGit/Logseq-Hugo-Template/stargazers">
    <img
        alt="GitHub Repo stars"
        src="https://img.shields.io/github/stars/CharlesChiuGit/Logseq-Hugo-Template?color=957FB8&logo=starship&style=for-the-badge">
    </a>
    <a href="https://github.com/CharlesChiuGit/Logseq-Hugo-Template/issues">
    <img
        alt="GitHub issues"
        src="https://img.shields.io/github/issues-raw/CharlesChiuGit/Logseq-Hugo-Template?color=DCA561&logo=gitbook&logoColor=d9e0ee&style=for-the-badge">
    <a href="https://github.com/CharlesChiuGit/Logseq-Hugo-Template/contributors">
    <img
        alt="GitHub contributors"
        src="https://img.shields.io/github/contributors/CharlesChiuGit/Logseq-Hugo-Template?color=%2398BB6C&logo=opensourceinitiative&logoColor=d9e0ee&style=for-the-badge">
    </a>
    <img
        alt="GitHub code size in bytes"
        src="https://img.shields.io/github/languages/code-size/CharlesChiuGit/Logseq-Hugo-Template?color=%237E9CD8&logo=gitlfs&logoColor=d9e0ee&style=for-the-badge">
</p>

<p align="center">
    <img
        alt="HTML"
        src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white">
    <a href="https://logseq.com/#/">
    <img
        alt="Logseq"
        src="https://img.shields.io/static/v1?label=&message=LOGSEQ&color=002B35&style=for-the-badge">
    </a>
</a>

## Description

This is a [HUGO](https://gohugo.io/) website template for [Logseq](https://logseq.com/#/) users who want their published posts to look more like a personal website, using [GitHub Pages](https://pages.github.com/) to host the website and [logseq-schrodinger](https://github.com/sawhney17/logseq-schrodinger) to export your Logseq pages.

<p align="center">
        <img src="./src/thanos_logseq_hugo.svg" style="width:50%"/>
</p>

## Credits

Credits to [Alex QWxleA](https://github.com/QWxleA) and [Aryan Sawhney](https://github.com/sawhney17) for inspiring this template.

---

## Why use [Logseq-Hugo-Template](https://github.com/CharlesChiuGit/Logseq-Hugo-Template) to build a website?

Although the native publish function in Logseq is very convenient, it's output result is more like a read-only Logseq, rather than a personal website.

### Why HUGO?

You can use [Markdown](https://www.markdownguide.org/) to write your posts/contents in HUGO.

### Why GitHub Pages?

You can host your website directly from your GitHub repo, and it cost you nothing.

---

## 🧱 Template Structure

```bash
├── archetypes/    # A piece of content that's common to all of the content on your website.
│   └── default.md
├── content/    # Where you store all the content for your website.
│   ├── assets/    # Things from LogseqGraph/assets, used in posts.
│   │   └── test.png
│   ├── pages/    # Revised Logseq pages with metadata sections for Hugo.
│   │   └── random page from logseq.md
│   ├── archives.md
│   └── search.md
├── .github/    # Define GitHub action to help deploy in one click.
│   └── workflows/
│       └── publish.yml
├── layouts/    # Where you define your layout for your website.
│   ├── partials/
│   │   └── backlinks.html    # Simulate backlinks function in Hugo.
│   └── shortcodes/
│       ├── logseq/    # Translation between Logseq and Hugo.
│       │   ├── mark.html
│       │   ├── orgCAUTION.html
│       │   ├── orgEXAMPLE.html
│       │   ├── orgIMPORTANT.html
│       │   ├── orgNOTE.html
│       │   ├── orgPINNED.html
│       │   ├── orgQUOTE.html
│       │   ├── orgTIP.html
│       │   └── orgWARNING.html
│       ├── contact.html
│       ├── hint.html
│       └── search.html
├── themes/    # Where you can apply pre-build themes or your own theme.
│   └── random-theme/   # In this repo, PaperMod is the default theme.
├── config.yml    # The main settings page for your website.
└── .gitignore    # This is to prevent unwanted files be tracked by Git.
```

## 🪜 Workflow

This workflow assumes your know something about GitHub.

1. Click the green `Use this template` button to fork this template repo.
2. Rename the forked repo to `{your-GitHub-username}.github.io`, e.g. GitHubUser.github.io.
3. Clone the repo.
4. Configure `config.yml`.
5. Export your Logseq pages to `content/pages`, using [logseq-schrodinger](https://github.com/sawhney17/logseq-schrodinger).
6. Push it to `git@github.com:{username}/{username}.github.io.git`.
7. After it's pushed, go to "Settings" > "Pages" > "Source" > Choose "gh-pages" branch. (auto-created by [GitHub actions](https://github.com/features/actions))
8. Wait few minutes for GitHub to deploy.
9. You should now see your website in `https://{username}.github.io/`, e.g. `https://githubuser.github.io/`! 🍻

## ✨ Things you MUST modify

### In `config.yml`

```yml
baseURL: https://githubuser.github.io # 1. All lowercase. 2. Don't put `/` after `.io`.
languageCode: en-us
title: Linus Torvalds # Your name or the website title.
theme: 'PaperMod'

params:
  homeInfoParams:
    Title: Sup bruh 😎 # homepage title.
    Content: This is something shows in your homepage. # homepage content.

  socialIcons: # optional
    - name: 'github'
      url: 'https://github.com/XXX'
    # - name: "youtube"
    #   url: "https://www.youtube.com/channel/XXX"
    - name: 'twitter'
      url: 'https://twitter.com/XXX'
    # - name: "kofi"
    #   url: "https://buymeacoffee.com/XXX"
    # - name: "rss"
    #   url: "https://XXX.github.io/index.xml"
  ShowReadingTime: true
  author: 'Linus Torvalds' # Your name.
  contact: 'LinusT@example.com' # Your email.
  feedlinks: true
  copyright: '<!--Creative Commons License-->This site is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).<!--/Creative Commons License-->'
  mobileMenu: true

  #Google Analytics 4 optional
  env: #production
  GoogleAnalytics: "G-00000XXXXX" 
  sitemap:
    changefreq: daily
    filename: sitemap.xml
    priority: 0.5
```

### In `content/pages` and `content/assets`

1. Make pages public.
2. Click on the three dots in the top right corner in Logseq and click `Export public pages to hugo`, via [logseq-schrodinger](https://github.com/sawhney17/logseq-schrodinger).
3. Unzip the file and move the contents into `content/`.

※ Noted: The marketplace version of logseq-schrodinger might have some file permission issues. Use the GitHub version one instead.

## How to set the Google Analytics 4?

1. Apply [Google Analytics 4](https://analytics.google.com/)
2. Write the GA4-ID to config.yml
3. Set[Google Search Console](https://search.google.com/search-console/welcome)and add sitemap

## How to change theme?

HUGO provides lots of prebuild themes.

1. [Install HUGO and Go](https://gohugo.io/getting-started/installing/).
2. [Follow the steps](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme).

※ Noted: Structure and configurations might vary from theme to theme.

## ⚠️ Limitations

[logseq-schrodinger](https://github.com/sawhney17/logseq-schrodinger) is very much a work-in-progress. Please check if there's anything wrong about your post after exported. File an issue if you think something is a bug.

### [What works on logseq-schrodinger so far](https://github.com/sawhney17/logseq-schrodinger#what-works)

- Local Hugo links (but Logseq uses one folder for everything, so Hugo does too)
- Block refs(!) — On conversion the block is pulled from the other location
- Images
  - Notice that the uppercase filenames might be transformed to lowercase, making the remote images invalid, please double-check that.
- Basic Markdown styling (including highlighting!)

## Issues

[Issues for logseq-schrodinger](https://github.com/sawhney17/logseq-schrodinger#issues)

[Issues for this template](https://github.com/CharlesChiuGit/Logseq-Hugo-Template/issues)

## Sample Sites

- <https://aryansawhney.com>
- <https://charleschiugit.github.io/>

## License

Distributed under the MIT License. See `LICENSE` for more information.
