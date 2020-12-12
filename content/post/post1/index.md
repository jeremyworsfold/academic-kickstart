---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "kepler.gl Mortality"
subtitle: "Life expectancies at LSOA level in London, animated using kepler.gl"
summary: ""
authors: []
tags: []
categories: [mortality, modelling, statistics]
date: 2020-11-06T21:01:52Z
lastmod: 2020-11-06T21:01:52Z
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
Provisional results. This is just a test. It's really slow. The *compressed* html is 73MB for LSOA London and 123MB for MSOA e0 in England. This is with super-generalised shapefiles too, never mind if we want to get things at 20m resolution for LSOAs. Other annoying things:
- kepler.gl is slow
- MSOA England level takes even longer to load
- It is slow
- It flashes between frames sometimes because it uses a rolling window to animate rather than a point for each year
- The year comes up with minutes and seconds and milliseconds and picoseconds
- The file sizes are too big to put on github without lfs

I probably need to find a more practical solution for the full result.

Have a play. Show the legend at the side. I would like to make this full screen too.