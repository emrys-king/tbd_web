---
layout: project
title: 'Neural Surrogate Methods for Spatial Statistics'
author-profile: true
collection: projects
sort_date: 2026.09
display_date: "2026"
preprint: "https://scholarship.claremont.edu/pomona_theses/347/"
preprintdisplay: "MSc Thesis"
github: "https://github.com/emrys-king/mscthesis"
---

<figure>
  <img src="{{site.url}}/images/poster-imperial.jpg" alt="Emrys, a short brown-haired person with glasses, is wearing a button down and standing next to their research poster. The poster title reads 'SM-DeepRV: A Neural Surrogate for Geospatial Gaussian Processes'"/>
  <figcaption>Me and my research poster at the Imperial MSc Statistics Research Fair in July 2026.</figcaption>
</figure>

A common problem in Bayesian inference is computational tractability. The computational cost of exact inference tends to limit scalability, which in turn limits the applicability of Bayesian methods to settings where dimensionality rapidly increases scale. For example, Gaussian processes are are a popular framework by which to model time series, spatial statistics, and spatiotemporal models, due to their flexibility, encoding of prior knowledge via the covariance function, and robust treatment of model uncertainty. They are also difficult to scale, since exact inference requires Cholesky decomposition of the $$n\times n$$ covariance matrix, with an associated computational cost $$\mathcal{O}(n^3)$$.

To make such inference frameworks tractable, approximate methods are necessary. One such family of methods is the neural surrogate, in which a neural network is trained to approximate some stage of the inferential workflow. My research focused on the DeepRV neural surrogate (introduced by [Navott et al. 2025](http://arxiv.org/abs/2503.21473)), which is trained to approximate a prior, thus allowing for amortization of neural training across multiple possible inferential problems. I extended the method to account for kernel functions with increasingly high-dimensional hyperparameters, mainly the spectral mixture kernel (see [Wilson & Adams 2013](https://proceedings.mlr.press/v28/wilson13.html) and [Wilson et al. 2014](https://proceedings.neurips.cc/paper_files/paper/2014/hash/f1b9324dd8d5843502953afb5efa289e-Abstract.html)). The spectral mixture kernel is notoriously difficult to sample from precisely due to its high-dimensionality, and DeepRV is the first tool to provide a full sampling workflow that could accommodate such limitations.