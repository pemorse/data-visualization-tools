Gradient Designer (GD) is a real-time interactive 3D gradient design and colour mapping application for global geoscientific data on the MacOS platform. 
It is specifically designed for designing colourmaps for continuous data, such as global seismic data.

It addresses these requirements through the following key features:

Data Handling:

•	Large local or remote datasets maybe be rapidly explored through an interactive 3D interface, that allows sequential overview of an entire dataset as well as zooming and panning to features of interest.

•	UI features a robust and clear relationship to known incoming data values and ranges.

•	Export of high-resolution colourised images derived from these large datasets.

•	Live real-time video sharing of colour gradient data to external client applications for display (e.g. on immersive visualisation systems).



Colour Control:

•	Four companion colour-space visualisation apps that provide live monitoring of gradient path traversal in CIELAB, RGB, HSL and HCL colour spaces.

•	Simple HSL slider UI manipulates RBG/sRGB (D65) gamut colours in 3D CIELAB/RGB/HSL/HCL colour spaces

•	Complex gradients may be designed that target specific values and ranges, including continuous linear, stepped-linear and non-continuous/non-contiguous ranges.

•	Import and export predefined gradients from other sources in a variety of formats (e.g. png, .cpt)

•	The ability to re-colourise imported gradients in part or in whole, addressing specific ranges and metrics

•	Alpha transparency control for 3D compositing/tomography

Application Aims and Development Framework

Gradient Designer (GD) provides an intuitive interface for a range of colour-mapping tasks, as it is agnostic about the nature of the incoming data: the assumption is that data has been pre-processed into whole-globe equirectangular 8-bit RGB JPEG or PNG black and white images, with known data ranges (where 0-255 represent known minima and maxima, linearly mapped to the underlying data, including alpha channel data if desired). The application is programmed in the MacOS Quartz Composer VPL, using a mixture of pre-defined QC processing nodes as well as custom routines programmed in C++, Javascript, OpenCL and OpenGL. It has been compiled into a stand-alone application using Kineme QuartzBuilder and Apple Xcode 9, targeting MacOS 10.13.6 (High Sierra) and MacOS 10.14 (Mojave). As of MacOS 10.14 OpenGL has been deprecated: future iterations of the software may require porting to Metal or platforms supporting OpenGL compatibility profiles.
