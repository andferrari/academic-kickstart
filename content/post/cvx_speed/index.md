---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Conv. rate with Pluto 🎈"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2021-03-01T10:56:39+01:00
lastmod: 2021-03-01T10:56:39+01:00
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
Convergence rate vs Hessian condition number using a [Pluto.jl](https://github.com/fonsp/Pluto.jl) notebook:
![sigmoid_fit](conv.gif)

```julia
using Plots, LinearAlgebra, PlutoUI
```

```julia
begin
  f(x) = x[1]^2 + γ*x[2]^2
  ∇f(x) = [2*x[1], 2*γ*x[2]]
  opt_step(x, Δ) = - (x[1]*Δ[1] + γ*x[2]*Δ[2])/(Δ[1]^2 + γ*Δ[2]^2)

  function grad_desc(; n_itermax = 40, x0 = [10, 1], ϵ = 1e-1)
    x = zeros(2, n_itermax)
    x[:,1] = x0
    k = 1
    while (norm(∇f(x[:,k])) > ϵ) && (k < n_itermax)
        Δ = - ∇f(x[:,k])
        x[:, k+1] = x[:, k] + opt_step(x[:,k], Δ)*Δ
        k += 1
    end
    x, k
  end
end
```

```julia
@bind γ Slider(1:0.1:15, default=5)
``` 

```julia 
begin	
x, k_max = grad_desc()
x1_, x2_ = LinRange(-10, 10, 64), LinRange(-5, 5, 64)
contour(x1_, x2_, (x,y)->f([x, y]), xlab="x₁", ylab= "x₂", rat=:equal, cb=false);
plot!(x[1, 1:k_max], x[2,1:k_max], m=:circle, label="")
title!("f(x) = x₁² + $γ.x₂²,  $(k_max-1) iterations", titlefontsize=10)
end
```