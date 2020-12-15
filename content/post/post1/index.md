---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "How to use Python for scientific research"
subtitle: "Maintaining a personal Python package for scientific research"
summary: ""
authors: []
tags: []
categories: [Scientific Computing]
date: 2020-12-14T21:44:52Z
lastmod: 2020-12-14T21:44:52Z
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "python.png"
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

The world seems to be split into two types of projects. The ones maintained by software engineers committed to maintaining usability, robustness and efficiency of a package. Then there are those entitiled `simulation-2_old.py` with cut and pasted code from previous versions which has only been looked at by one person. It might seem ovbious which is the better project but the word *better* here is important. 

The context of what the code is for is crucial. If all was needed was a short simulation to demonstrate some result then perhaps the second type is a more efficient use of time. The importance of changeability and speed of implementation is an important factor in scientific research. 

This article tries to present to you a way of balancing these two extremes. There are always more things you can add to a project and this is what I have found works for me but my opinion may also change on what it necessary. 

## General things we want our project to do ##

- save our simulations: don't want to lose data
- separate visualising results from the simulation or preprocessing
- good documentation for us or someone familiar with the field
- ability for someone else to download and run our code to verify the results and believe what we say is true.


## Why Python? ##

python is pretty but also it's flexible and has good support for various features. Depending on the situation others may be more appropriate and when it comes down to it, language choice for small packages like this is just personal preference.

I know python a lot more than other possibilities such as MATLAB or R though so I will stick to this. A lot of the advice will be transferrable in some respect though.

## How to Structure your Python project ##
This is how I've chosen to layout my projects, it follows the standard for python packages but has some tweaks for using as a personal project which may not be considered best practice but is relatively easy to use.
```
exampleproject
│   README.md
│   setup.py
│
├───data
├───exampleproject
│   │   __init__.py
│   │
│   ├───environment
│   │       base.py
│   │       derived.py
│   │       __init__.py
│   │
│   └───otherfiles
│           utils.py
│           __init__.py
│
├───notebooks
│       01-feature1.ipynb
│       02-feature2.ipynb
│
└───scripts
        feature1.py
```

## Documentation and Commenting ##


## Presenting your findings ##

number them so there's some structure but maybe not necessary

load in results, can then just plot it and convert it to some other format to be plotted professionally like pgfplots.