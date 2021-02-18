---
title: "How to use Python for scientific research"
summary: "Maintaining a personal Python package for scientific research"
authors: [admin]
tags: [Scientific Computing]
categories: [Scientific Computing]
date: 2020-12-14T21:44:52Z
lastmod: 2020-12-14T21:44:52Z
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: night
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula
plugins: ["plugin/chalkboard/plugin.js","plugin/chart/plugin.js","plugin/menu/plugin.js"]
plotly: true
math: true

---

## How to use Python for scientific research

### Maintaining a personal Python package for scientific research

---

## Our project should

- Save data
- Separate plotting from time-consuming code
- Have good documentation
- Be Distributable 

---

## Why Python?

It is personal preference however...

## test

---

<section data-no-process>

<section data-auto-animate>
  <h3>Auto-Animate</h3>
</section>
<section data-auto-animate>
  <h3 style="margin-top: 100px; color: red;">Auto-Animate</h3>
</section>

</section data-no-process>

---
## Layout

Root directory
```
exampleproject
│   README.md
│   setup.py
│
├───data
├───docs
├───exampleproject
├───notebooks
└───scripts
```

---

{{< chart data="annealing" >}}

---