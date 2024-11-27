---
layout: single
title:  "Compressing multivariate functions with tree tensor networks"
toc: false
categories: 
  - papers
header:
  overlay_image: /assets/images/compressing.png
  overlay_color: "#333"
  overlay_filter: 0.75
excerpt: Continuous functions represented as tree tensor networks with a little help from TCI
---

Another paper out on [arXiv](https://arxiv.org/abs/2410.03572)! Titled _Compressing multivariate functions with tree tensor networks"_, Joey, Miles, and I at Flatiron CCQ developed a new library and methodology for compressing continuous multi-dimensional functions as tree tensor networks. Thanks to [ITensorNetworks.jl](https://github.com/ITensor/ITensorNetworks.jl/) underpinning, we can easily manipulate any tree topology and bit ordering you can dream of (hopefully), along with some intergral and differential equation tools.

Also checkout the [GitHub Repo](https://github.com/JoeyT1994/ITensorNumericalAnalysis.jl). 


<details>
  <summary>Abstract
</summary>
  
  <div class="notice--info"><p>
Joseph Tindall, Miles Stoudenmire, <b>Ryan Levy</b> <br /><br />
Tensor networks are a compressed format for multi-dimensional data. One-dimensional tensor networks -- often referred to as tensor trains (TT) or matrix product states (MPS) -- are increasingly being used as a numerical ansatz for continuum functions by "quantizing" the inputs into discrete binary digits. Here we demonstrate the power of more general tree tensor networks for this purpose. We provide direct constructions of a number of elementary functions as generic tree tensor networks and interpolative constructions for more complicated functions via a generalization of the tensor cross interpolation algorithm. For a range of multi-dimensional functions we show how more structured tree tensor networks offer a significantly more efficient ansatz than the commonly used tensor train. We demonstrate an application of our methods to solving multi-dimensional, non-linear Fredholm equations, providing a rigorous bound on the rank of the solution which, in turn, guarantees exponentially scaling accuracy with the size of the tree tensor network for certain problems.
</p></div>

</details>
[arXiv:2410.03572](https://arxiv.org/abs/2410.03572){: .btn .btn--success}
