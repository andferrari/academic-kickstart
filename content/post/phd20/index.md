---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "PhD scholarship"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-05-07T12:35:59+02:00
lastmod: 2020-05-07T12:35:59+02:00
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

## Line by line Deep Learning algorithm for detection of artifacts in uncalibrated multispectral satellite images

The aim of artifact detection satellite image is to detect and locate pixels or set of pixels that are decorrelated from the statistically representative background. For instance, in forestry applications, infected trees are considered as artifacts, as well as water pollution in coastal clear waters. Contrarily to the target detection problem where the spectra of the target must be known, artifact detection methods generally assume no prior information about the spectra of the pixels, in both nominal and abnormal cases. State-of-the-art algorithms use reference data either from a local neighborhood around the pixel/spectrum to be tested, either using all or part of the HSI data possibly at a different time instant. The most popular among these algorithms are the Reed-Xiaoli Detector (RXD) [1] and its many variations. More recently algorithms using deep convolutional neural networks have proved their effectiveness for this task [2].

All these approaches rely on pairs of learning and testing spectra sets which are performed on images processed on ground and geometrically, spectrally and radiometrically calibrated. Moreover, these algorithms consist of a learning step and a testing step on two set of patches acquired at different time instant and so don’t allow a fully (learning and testing) line by line processing in order to process a continuous flow of data. The objectives of this PhD will be to develop an artifact detection algorithm, computationally efficient and compatible with data as acquired by the pushbroom sensor i.e. line by line and before radiometrically, spectral and geometric corrections and calibrations, which takes advantage of recent advances in machine learning.

We propose to develop anomaly line by line artifact detection algorithm which processes sensor output data flow compatible with the pushbroom acquisition: a new line of ground swath is processed at each iteration of the algorithm in order to decide, and to localize if needed, whether one or more artifacts are present. The decision will take into account spatial and spectral information acquired across the past scanned line swaths and the new line swath. Note that a similar approach was recently proposed for online deconvolution of hyperspectral images acquired using a fixed industrial imaging system above a conveyor belt in [3].

We propose to address the lack of data calibration using a learning algorithm which gives more weight to measurements acquired near the decision zone. The first approach we will investigate is an adaptive strategy where two classifiers are learned simultaneously using two distinct learning rates: the rationale behind this idea is that the classifier with the larger learning rate gives “more importance” to recent samples than the other classifier, so the distance between the two classifiers outputs should increase in case of a spatially localized change. The principle of comparing two classifiers outputs with different learning rates is well-known in the field of time series processing, see for example [4]. It has recently been proposed in [5] for change point detection in time series data in conjunction with more recent machine learning techniques. In [6] this strategy is applied to the problem of change point detection in signals on graphs.
To our knowledge, these approaches have not yet been applied for detecting artifacts in multispectral images acquired by pushbroom systems. A particular effort will be made to develop appropriate classifiers that take into account information related to the spatial and spectral coherence of an artifact. In this context, kernel-based models and convolutional neural network models are candidates that will be studied.

To our knowledge, these approaches have not yet been applied for detecting artifacts in multispectral images acquired by pushbroom systems. A particular effort will be made to develop appropriate classifiers that take into account information related to the spatial and spectral coherence of an artifact. In this context, kernel-based models and convolutional neural network models are candidates that will be studied.

An important part of the thesis will consist of evaluating the effect of processing uncalibrated data. For this purpose, Thales Alenia Space will provide for the same scene both: raw camera data sets and fully calibrated datasets. These datasets will make it possible to quantify the performance degradation associated with processing of uncalibrated data. The dataset foreseen are of 2 types : Sentinel 3/OLCI data acquired during the In Orbit Commissioning Review, and simulated CHIME data performed for the CHIME phase A/B1 per-development study. ESA has already agreed to the use of these data for a research purpose.

- [1] Adaptive multiple-band CFAR detection of an optical pattern with unknown spectral distribution. Reed, I.S.; Yu, X., IEEE Trans. Acoust. Speech Signal Process. 1990,38, 1760–1770.
- [2] Unsupervised Learning of Robust Representations for Change Detection on Sentinel-2 Earth Observation Images. Aubrun, M.; Troya-Galvis, A.; Albughdadi, M. ; Hugues, R. and Spigai, M., 13th IFIP WG 5.11 International Symposium, ISESS 2020, Wageningen, The Netherlands, February 5–7, 2020.
- [3] Online deconvolution for industrial hyperspectral imaging systems. Song, Y.; Djermoune, E.; Chen, J.; Richard, C.; and Brie, D. SIAM Journal on Imaging Sciences, 12(1): 54-86. 2019.
- [4] Control Chart Tests Based on Geometric Moving Averages. S. W., Technometrics, 1(3):239–250, 1959.
- [5] Newma: a new method for scalable model-free online change-point detection, Keriven, N.; Garreau, D. and Poli, I., 2018, https://arxiv.org/abs/1805.08061.
- [6] Distributed change detection in streaming graph signals. Ferrari, A. ; Richard C. ; Verducci L., 2019 IEEE 7th International Workshop on Computational Advances in Multi-Sensor Adaptive Processing (CAMSAP)

