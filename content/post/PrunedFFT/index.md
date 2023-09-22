---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "PrunedFFT"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2023-09-21T16:55:40+02:00
lastmod: 2023-09-21T16:55:40+02:00
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
You need to compute a **subset** of the outputs of a 2D FFT 
with a **large zero padding**? Try [PrunedFFT.jl](https://github.com/andferrari/PrunedFFT.jl). It works also on GPU🔥

```julia
using PrunedFFT

n = 128
x = rand(n, n)
n_pad = 1024
k_span = collect(512:612)

f = pruned_fft(x, n_pad, k_span)
```

If `CUDA.jl` is installed
```julia
using CUDA

xc = cu(x)
f = pruned_fft(xc, n_pad, k_span)
```

For a very large zero padding, GPU🔥 acceleration is a must!
```
julia> @time f1 = pruned_fft(xc, n_pad^2, k_span);
 0.713510 seconds (78.25 k allocations: 1.792 GiB, 17.73% gc time)

julia> @time f1 = pruned_fft(x, n_pad^2, k_span);
19.362908 seconds (2.25 k allocations: 9.985 GiB, 3.82% gc time)
``````
