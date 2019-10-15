**Gradient Designer**

[![DOI](https://zenodo.org/badge/194572076.svg)](https://zenodo.org/badge/latestdoi/194572076)
=======

[![VIDEO DEMO](/Support_files/GD_LAB_CM_GV_LAB_demo.png "Video Demo")](https://vimeo.com/366616654)

=======

**Gradient Designer** (GD)is an interactive gradient design and colour mapping application for geoscientific data on the MacOS platform. 

It is intended for designing colourmaps for continuous data, such as global seismic data.

Four companion colour-space visualisation apps provide live monitoring of gradient path traversal in CIELAB, RGB, HSL and HCL colour spaces.

Note: For multi-monitor systems, GD and companion apps must operate on monitors using the same ICC profile.

Functions:
======

**Data Handling**:

* Local or remote datasets maybe be explored through an interactive 3D interface, allowing sequential overview of an entire dataset as well as zooming and panning to features of interest.
* UI controls for a robust and clear relationship to incoming data values and ranges
* Export of high-resolution colourised images (GPU dependent)
* Live real-time video sharing of colour-mapping to external client applications for display (e.g. on immersive visualisation systems)

**Colour Control**:

* Establish reproducible colour difference and luminosity metrics
* Optimise colour difference and luminosity for colour maps
* Alpha transparency control for 3D compositing/tomography

* Match RGB gradient termini and interpolate in CIELAB, monitoring sRGB gamut constraints
* Four companion colour-space visualisation apps provide live monitoring of gradient path traversal in CIELAB, RGB, HSL and HCL colour spaces
* Simple HSL slider UI manipulates RBG/sRGB (D65) gamut colours in 3D CIELAB/RGB/HSL/HCL colour spaces
* Complex gradients may be designed that target specific values and ranges, including continuous linear, stepped-linear and non-continuous/non-contiguous ranges
* Import/Export predefined gradients from external sources
* Re-colourise imported gradients in part or in whole, addressing specific ranges and metrics



**Application Aims and Development Framework**

**GD** and its companion apps aim to provide an intuitive interface for a range of colour-mapping tasks.

It is agnostic about the nature of the incoming data: the assumption is that data has been pre-processed into whole-globe equirectangular 8-bit RGB JPEG or PNG black and white images, with known data ranges (where 0-255 represent known minima and maxima, linearly mapped to the underlying data, including alpha channel data if desired). 

The application is programmed in the MacOS **Quartz Composer (QC)** [link][https://developer.apple.com/documentation/quartz/quartz_composer] VPL, using a mixture of pre-defined QC processing nodes as well as custom routines programmed in Objective-C, Javascript, OpenCL and OpenGL. 


**Limitations**

The software targets average color perception and does not currently compensate for users with color vision deficiencies.

GD and companion apps have been compiled into a stand-alone applications using Kineme QuartzBuilder and Apple Xcode 10.1, targeting **MacOS 10.13.6 (High Sierra) and MacOS 10.14 (Mojave). 

As of MacOS 10.14 OpenGL has been deprecated: future iterations of the software may require porting to Metal or platforms supporting OpenGL compatibility profiles. 



