---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Waterfall"
subtitle: ""
summary: ""
authors: []
tags: ["julia"]
categories: []
date: 2022-01-19T10:32:07+01:00
lastmod: 2022-01-19T10:32:07+01:00
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
Simple [Plots.jl](https://github.com/JuliaPlots/Plots.jl) receipe for waterfall plots 
(a la [Unknown Pleasures](https://gist.github.com/andferrari/3e254ffd67629078c1aaad95caf23079) 😀). Install using:
```julia
pkg> add https://github.com/andferrari/WaterFall.jl
```
and
```julia
using WaterFall
x = [exp(-(n - 1e-2*τ^2)^2/τ)  for n in 0:300, τ in 40:10:160]
plotfall(x, w=2)
```
