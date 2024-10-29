---
layout: post
title:  "multilightning"
date:   2024-10-25
categories: lightning update
---

In addition to the development build of [lightning.py](/2024/10/25/lightningpy) released today, we release the ``multilightning`` wrapper, which
provides a framework for jointly fitting multiple regions of a galaxy with different star formation histories (SFH). Due to
differing resolutions of telescopes across the electromagnetic spectrum, it is common to resolve a galaxy in only a
subset of the available bandpasses (e.g. optical) and have it unresolved in the remainder (e.g., far-infrared; FIR). Since
the FIR places a valuable constraint on the total star formation it is undesirable to discard those bands when estimating
the SFH of the resolved regions.

In multilightning, we define a joint likelihood for fitting multiple resolved regions, under the assumption that the
unresolved photometry is described by the sum of the models for each resolved region. In Lehmer et al. (2024, ApJ, in press)
this method is applied to a number of nearby galaxies, jointly fitting the galactic disk and the X-ray crowded regions at their
centers, where counting individual X-ray binaries is not possible. By doing so, we are able to estimate the SFH of only
the regions in which we can constrain the X-ray binary luminosity function, without losing the valuable FIR constraint
on the normalization of the SFH.

## Links
- [multilightning](https://github.com/ebmonson/multilightning)
- Documentation ([web](https://multilightning.readthedocs.io/en/latest/) / [pdf](https://github.com/ebmonson/multilightning/blob/main/docs/multilightning.pdf))
