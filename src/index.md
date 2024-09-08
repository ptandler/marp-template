---
title: Marp template
author: Peter Tandler
description: Introduction how to start writing presentations with Marp, the Markdown Presentation Ecosystem. Including a default project setup.
keywords: marp, presentation, template, tutorial, guide
lang: en
license: CC BY-NC-SA 4.0
marp: true
paginate: true
#theme: weber
theme: king
#theme: uncover
options:
  looseYAML: false
  markdown:
    breaks: false
    typographer: true
    quotes: "„“‚‘"
    xhtmlOut: true
bespoke:
  osc: true
  progress: true
pdf-outlines: true
pdf-notes: true
---

<!-- _class: titlepage -->

# Writing presentations with Marp, the Markdown Presentation Ecosystem

## Tutorial and Project Template

### Peter Tandler

#### 08.09.2024

---

# Overview

- Used tools
- First steps
- Folder structure of the Marp template
- Important files you need to work with Marp
- Scripts provided in `package.json5`

---

# Used Tools

- Marp VS Code extension: used for writing presentation in VS Code
- Marp CLI: for final rendering of HTML, PDF, PPTX
- [`git`](https://git-scm.com/) for versioning your presentation
- [`pnpm`](https://pnpm.io/) as package manager (I prefer it over npm, but you don't have to use it)
- [`prettier`](https://prettier.io/) for applying default formatting
- [`json5`](https://json5.org/) for configuration (as I can add comments and use a simpler syntax)
- [Creative Commons License](https://creativecommons.org/share-your-work/): so you know how you may use this template <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-SA 4.0 <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a>

---

# Setup

- VS Code setup: add link to doc###
- Ensure you have the necessary tools installed: git, pnpm
  - For Linux I prefer [`mise`](https://mise.jdx.dev/) to install tools & manage tool versions
  - `mise i git node pnpm`
- clone this repo: `git clone ....`
- install packages & local tools: `pnpm i`

---

# Brief Introduction of the Markdown Presentation Ecosystem

The [Marp family consists of 4 parts](https://github.com/marp-team/marp/)

1. [Marpit](https://github.com/marp-team/marpit): The framework for creating slide deck from Markdown
   - [Marp internally uses](https://marpit.marp.app/?id=features) [`markdown-it`](https://github.com/markdown-it/markdown-it) for processing markdown
   - `markdown-it` extensions can be used with marp
     - **TODO: add link to doc ###**
     - example: `markdown-it-include`
2. [Marp Core](https://github.com/marp-team/marp-core): The core of Marp converter with practical features and built-in themes
3. [Marp CLI](https://github.com/marp-team/marp-cli): Command-line interface to run the above tools
4. [Marp for VS Code](https://github.com/marp-team/marp-vscode): A VS Code extension to preview the slide deck written in Marp Markdown.

You actually interact only with the VS Code extension and the CLi _directly_, they use all other tools internally.

---

# Getting Starting

Make yourself familiar with [how to write slides with  Marpit Markdown](https://marpit.marp.app/markdown), basically: Marpit splits pages of the slide deck by horizontal ruler (e.g. `---`). It’s very simple:

```markdown
# Title of Slide 1

Slide content

---

# Title of Slide 2

And more interesting slide content
```

You can look at [source code of this sample presentation, starting with `src/index.md`](index.md)

---

# Folder Structure of the template

- root dir: configuration files for tools & README
- `src`: all files that belong to the presentation
  - `style`: Marp templates that can be used
- `.vscode`: config for VS Code

---

# Files in the template

- ... **TODO: continue here###**

---

# Scripts provided in `package.json5`

- ... **TODO: continue here###**

---

# Other things to cover

** TODO: ##**
- how to publish the generated presentation to github pages
- config: where can I tweak what
- how to find & install & use templates
- how to customize templates
- find & install & use markdown-it extension
- where to find which resources
