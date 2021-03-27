---
layout: single
title:  "Randomized SVD Presentation"
categories:
  - programming
tags:
  - SVD
header:
  overlay_image: assets/images/SVD.png
  overlay_filter: 0.7
  overlay_color: "#333"
excerpt: Improving low-rank SVD speeds and scaling by exploiting randomization
#categories: programming 
---

Singular value decomposition (SVD) is a powerful tool but can be very slow for large dense matrices that may be stored on disk rather than in memory. Over the past decade or so, new algorithms have been proposed that allow for a speed up by first assuming we only want $$k$$ singular values, and then exploiting randomization.

Check out [**my presentation**](http://algorithm-interest-group.me/algorithm/Randomized-SVD-Ryan-Levy/) on Randomized SVDs for the Algorithm Interest Group over at UIUC. 
{: .notice--info}

I also wrote up a short ipython notebook with some implementations:<br/> [**html**](https://paul-st-young.github.io/algorithms/assets/notebooks/randomizedSVD.html) / [**ipynb**](https://paul-st-young.github.io/algorithms/assets/notebooks/randomizedSVD.ipynb).
{: .notice--primary}
