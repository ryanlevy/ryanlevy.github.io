---
layout: single
title:  "Magic of NUTS"
categories:
  - programming
tags:
  - NUTS
  - Monte Carlo
header:
  overlay_image: assets/images/nuts_dist.png
  overlay_filter: 0.7
  overlay_color: "#333"
excerpt: The No U-Turn Sampler is a powerful Monte Carlo Technique
#categories: programming 
---

Often we want to sample from a probability distribution, but we don't have direct access to the distribution only something proportional to it.
A well known standard, using the Metropolis method, can easily get stuck or take a while to equilibrate in its random walk. 
Hamiltonian Monte Carlo was introduced to _flow_ through space instead of a random walk. However, in exchange for the improved sampling there are many (naively) hard to tune hyperparameters - enter the No-U Turn Sampler (NUTS) to adaptively determine many of the important hyperparameters. 
 

Check out [**my presentation**](http://algorithm-interest-group.me/algorithm/Magic-Of-NUTS-Ryan-Levy/) on the powerful No-U Turn Sampler (NUTS) technique for the Algorithm Interest Group over at UIUC. 
{: .notice--info}

I also wrote up a short ipython notebook with some implementations:<br/> [**nbviewer**](https://nbviewer.jupyter.org/urls/paul-st-young.github.io/algorithms/assets/notebooks/HMC_noan.ipynb) / [**ipynb**](https://paul-st-young.github.io/algorithms/assets/notebooks/HMC_noan.ipynb).
{: .notice--primary}
