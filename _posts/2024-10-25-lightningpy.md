---
layout: post
title:  "lightning.py"
date:   2024-10-25
categories: lightning update
---

Today my collaborators and I have published our in-development python version of the Lightning spectral energy
distribution (SED) code. Full release is expected later this year, accompanying a paper by Monson et al.

This version builds on the IDL version of Lightning published alongside [Doore et al. (2023)](https://ui.adsabs.harvard.edu/abs/2023ApJS..266...39D/abstract), and is intended to make
the process of SED-fitting more user-friendly while also taking advantage of the large volume of python libraries already
available from the astronomy community.

In addition to the shift to python, this version of the code moves to an object-oriented architecture and includes
a number of new models, including:
- New nebular models generated using Cloudy in combination with stellar models from PEGASE and BPASS.
- Active galactic nucleus (AGN) polar dust attenuation model based on the [X-Cigale](https://ui.adsabs.harvard.edu/abs/2020MNRAS.491..740Y/abstract) recipe, which de-couples the AGN
  attenuation from the host galaxy attenuation, allowing more flexibility especially in fitting Type-1 AGN.

We also release today the [multilightning](/2024/10/25/multilightning) wrapper for ``lightning.py``, which implements multi-region SED fits, accounting
for variable resolution of the data across the electromagnetic spectrum.

## Links
- [lightning.py](https://github.com/ebmonson/lightningpy)
- Documentation ([web](https://lightningpy.readthedocs.io) / [pdf](https://github.com/ebmonson/lightningpy/blob/main/docs/lightningpy.pdf))
- [IDL Lightning](https://github.com/rafaeleufrasio/lightning) / [Documentation](https://lightning-sed.readthedocs.io)
