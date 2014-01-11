Features
====

Local Feature Detectors
---

###MSER

Maximally Stable Extremal Regions (MSER) finds correspondences between image elements from two images with different viewpoints. This method of extracting a comprehensive number of corresponding image elements contributes to the wide-baseline matching, and it has led to better stereo matching and object recognition algorithms.

**Papers:**
Matas, Chum, Urban, Pajdla, “*Robust wide-baseline stereo from maximally stable extremal regions*”, BMVC’02.


###DoG

Difference of Gaussians (DoG) is a feature enhancement algorithm used by SIFT. It involves the subtraction of one blurred version of an original image from another, less blurred version of the original. The Laplacian of Gaussian is useful for detecting edges that appear at various image scales or degrees of image focus.

**Papers:**
Lowe, “*Distinctive image features from scale-invariant keypoints*”, IJCV’04.  [[view]](../files/ijcv04.pdf)


###Hessian-Affine

The Hessian affine detector is typically used as a preprocessing step to algorithms that rely on identifiable, characteristic interest points. It relies on interest points detected at multiple scales using the Harris corner measure on the second-moment matrix. The Hessian affine also uses a multiple scale iterative algorithm to spatially localize and select scale & affine invariant points.

**Papers:**
Mikolajczyk, Schmid, “*Scale and affine invariant interest point detectors*”, IJCV’04.

Mikolajczyk et al., “*A comparison of affine region detectors*”, IJCV’05.


----------


Local Descriptors
---

###SIFT
####Original Lowe's algorithm

 - **DoG detection**: The first stage of computation searches over all scales
and image locations. It is implemented efficiently by using a difference-of-Gaussian
function to identify potential interest points that are invariant to scale and orientation.

 - **Scale-space pyramid**: At each candidate location, a detailed model is fit to determine
location and scale. Keypoints are selected based on measures of their stability.

 - **Orientation assignment**: One or more orientations are assigned to each keypoint lo-
cation based on local image gradient directions. All future operations are performed
on image data that has been transformed relative to the assigned orientation, scale, and
location for each feature, thereby providing invariance to these transformations.

####Keypoint descriptor

The local image gradients are measured at the selected scale in the region around each keypoint. These are transformed into a representation that allows for significant levels of local shape distortion and change in illumination.

 1. Computing the gradient magnitude and orientation at each image sample point in a region around the keypoint location, as shown on the left of a 8x8 set of samples.

 2. These samples are then accumulated into orientation histograms summarizing the contents over 2x2 subregions, as shown on the right.

 3. The feature vector contains 2x2x8 elements in this example. In the actually implementation, the feature vector is computed on a 4x4 histogram array of a 16x16 sample array. Therefore the dimension of a SIFT keypoint is 4x4x8 = 128.

![sift](../images/sift.png)

####Dense SIFT (DSIFT)

The most major difference between dense SIFT and traditional SIFT is that, with dense SIFT, a SIFT descriptor is calculated at every location, while with traditional SIFT, descriptions are only calculated at the locations determined by Lowe's algorithm. There are scenarios that the dense SIFT descriptor achieves better performance than normal SIFT, especially in recognition tasks, including face recognition.

![sift](../images/dsift-geom.png)

**Papers:**
Lowe, “*Distinctive image features from scale-invariant keypoints*”, IJCV’04.  [[view]](../files/ijcv04.pdf)

A. Bosch, A. Zisserman, and X. Munoz. Image classifcation using random forests and ferns. In Proc. ICCV, 2007.


###FREAK

Fast Retina Keypoint (FREAK) is inspired by the human visual system and more precisely the retina. A cascade of binary strings is computed by efficiently comparing image intensities over a retinal sampling pattern. It is designed for faster computation, more compact while remaining robust to scale, rotation and noise.



**Papers:**
A. Alahi, R. Ortiz, and P. Vandergheynst. FREAK: Fast Retina Keypoint. In CVPR, 2012. [[view]](../files/freak.pdf)

----------


Face Descriptors
---

###LBP

**Papers:**

###HOG

**Papers:**


----------


Global Descriptors
---

Global descriptors are pixel statistics of the whole image. They are often highly efficient to compute and match, but not very informative.

###Color Histogram

A color histogram is a representation of the distribution of colors in an image. For digital images, a color histogram represents the number of pixels that have colors in each of a fixed list of color ranges, that span the image's color space, the set of all possible colors.

**Papers:**
Swain, Ballard, “*Color indexing*”, IJCV’91.


###GIST

The GIST descriptor use a set of perceptual dimensions (naturalness, openness, roughness, expansion, ruggedness) that represent the dominant spatial structure of a scene. The image is divided into a 4-by-4 grid for which orientation histograms are extracted.

**Papers:**
Oliva, Torralba, “*Modeling the shape of the scene: A holistic representation of the spatial envelope*”, IJCV’01.
Douze, Jegou, Sandhawalia, Amsaleg, Schmid, “*Evaluation of GIST descriptors for web-scale image search*”, CIVR’09.



###CENTRIST

CENsus Transform hISTogram (CENTRIST) mainly encodes the structural properties within an image and suppresses detailed textural information. It is designed for place and scene recognition tasks.

**Papers:**
Wu, Rehg, “*CENTRIST: a visual descriptor for scene categorization*”, TPAMI’11.









Tutorials
---
1. Florent Perronnin's lecture in CVPR 2012 Large Scale Visual Recognition Tutorial:

    ***Features for Large-Scale Visual Recognition*** [[view]](../files/step1-feature.pdf)
