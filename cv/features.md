Global Descriptors
=====

Global descriptors are pixel statistics of the whole image. They are often highly efficient to compute and match, but not very informative.

Color Histogram
---
A color histogram is a representation of the distribution of colors in an image. For digital images, a color histogram represents the number of pixels that have colors in each of a fixed list of color ranges, that span the image's color space, the set of all possible colors.

Swain, Ballard, “*Color indexing*”, IJCV’91.


GIST
---
The GIST descriptor use a set of perceptual dimensions (naturalness, openness, roughness, expansion, ruggedness) that represent the dominant spatial structure of a scene. The image is divided into a 4-by-4 grid for which orientation histograms are extracted.

Oliva, Torralba, “*Modeling the shape of the scene: A holistic representation of the spatial envelope*”, IJCV’01.

Douze, Jegou, Sandhawalia, Amsaleg, Schmid, “*Evaluation of GIST descriptors for web-scale image search*”, CIVR’09.



CENTRIST
---
CENsus Transform hISTogram (CENTRIST) mainly encodes the structural properties within an image and suppresses detailed textural information. It is designed for place and scene recognition tasks.

Wu, Rehg, “*CENTRIST: a visual descriptor for scene categorization*”, TPAMI’11.



Local Detectors
=====

MSER
---

DoG
---

Hessian-Affine
---


Local Descriptors
=====

SIFT/SURF
---

DSIFT
---

FREAK
---

Face Descriptors
=====

LBP
---

HOG
---


Tutorials
====

