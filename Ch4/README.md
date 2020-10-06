# Tagger

# Tagger 0.6.1.3

Tagger is an interactive software tool and workflow to visualise, characterise, sample and tag 1d time-variant geoscientific datasets from both local and cloud-based repositories. It uses an animated interface and human-computer interaction to utilise the capacity of human expert observers to identify features via enhanced visual analytics. 

Tagger is alpha release research software. Your performance may vary.

Please read these instructions in full before attempting to install the software.

System requirements:

# Hardware

1] A fast Apple Mac Computer: recommended Mac Pro with 6GB+ VRAM.

2] A large screen capable of displaying 1920x1200px or more

# Software

1] MacOS 10.7 to 10.12.3

2] Quartz Composer 4.6.2 or greater, available here (requires developer account login): https://developer.apple.com/download/more/ - look for Additional_Tools_for_Xcode_8.dmg if you are running MacOS 10.11 or later; look for Additional_Tools_for_Xcode_7.dmg on MacOS 10.10 or earlier. Quartz Composer is located inside the 'Graphics' folder.

3] Quartz Composer plugins/patches: 
__Versions are supplied with this repository that ~may~ work on your MacOS version (tested up to MacOS 10.12.3)__
Use the supplied versions from the attached zip files in this repository. This bundles necessary plugins/patches that may not be currently available (precompiled) online. Kineme ChartTools, Data Tools, GLTools, and FileTools will be 30 day demo versions that will require an end-user license to be purchased after the end of the trial period. Licenses may be purchased from Kineme (http://kineme.net/downloads) or the plugins can be compiled from souce if available on github (see below URLs). Kineme Core may be installed optionally. 
 __Bundled plugin/patches are indicated by an asterisk, below.__

4] Quartz Composer plugins/patches download URLs:

  *ChartTools.plugin http://kineme.net/product/ChartTools
  
  *DataTools.plugin https://github.com/kineme/DataTools
  
  *FileTools.plugin https://github.com/kineme/FileTools
  
  *FreeboardPatch.plugin http://kineme.net/release/FreeboardPatch/01

  *GLTools.plugin https://github.com/kineme/GLTools
  
  
  *1024_StructureTools.plugin https://1024d.wordpress.com/qc-plugins/ __seems to be unavailable online__

  *Climb CSV Importer.plugin http://www.climbapp.com/plugin/csvimporter/index.html

  
  FXFactory Patches.plugin https://fxfactory.com/download/ (installed as part of FxFactory)
  
  jQC 1.0 http://qcdesigners.com/index.php/forums/topic/100/it-s-finally-here-j-qc-1-0-a-u/

  Origami.plugin https://github.com/facebookarchive/origami (note: this is now deprecated, but required for Tagger)

  QCGUI.plugin https://github.com/nenghuo/QCGUI

  
Note - to work on versions of MacOS later than 10.8 some of the plugins/patches hosted on github may require compiling from source using Xcode 7 or later. This has been done for bundled versions, though these are not guaranteed to work, depending upon your system configuration.

If compiling from source, some plugins/patches require the QCPatchXcodeTemplate available here https://github.com/kineme/QCPatchXcodeTemplate or here http://kineme.net/QCPatchXcodeTemplate

Some plugins ~may~ have become unavailable or difficult to locate online (eg. _1024_StructureTools.plugin)_.  

________________________________

# Installation

The EASIEST way to correctly install all patches and plugins is to use the QC Plugin Manager: http://imimot.com/qc-plugin-manager/ This will correctly install plugins & patches in their correct locations.

Quartz Composer can install plugins/patches in two key locations:

##1.

"/Users/****/Library/Graphics/Quartz Composer Patches" (if you don’t have this folder, create one)

"/Users/****/Library/Graphics/Quartz Composer Plugins" (if you don’t have this folder, create one)

##2.

"Macintosh HD/Library/Graphics/Quartz Composer Patches" (if you don’t have this folder, create one)

"Macintosh HD/Library/Graphics/Quartz Composer Plugins" (if you don’t have this folder, create one)

Confusingly, some '.plugin' files need to be placed in the 'patches' directory, NOT the plugins directory.

See here for more information: http://kineme.net/HowtoInstallCustomPatches or here: https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/QuartzComposer_Patch_PlugIn_ProgGuide/plugin_1/plugin_1.html


_________________________________

# Instructions:

Once Quartz Composer has been installed, as well as all custom patches/plugins, please run the file QCGUI_test.qtz to confirm that Tagger interface buttons are performing correctly and not causing non-specific OpenGL crashes. From testing, running this small program will overcome a temporary OpenGL problem that may cause Tagger to crash under MacOS 10.11/10.12, earlier versions (10.7-10.10) are not affected. This program may be left open in the background whilst Tagger is running.

Open Tagger_v0.6.1.3.qtz in Quartz Composer and follow this video for user instructions and demonstration:

https://vimeo.com/113643647 (long version: 12 mins)
https://vimeo.com/205325366 (short version: 7 mins)

This repository includes an example WaveRider buoy data file: cpso2001_h1.csv 

For demonstration purposes, this is a non-THREDDS-capable version of Tagger that works with local .csv/.txt data files.

_________________________________

# Data

Tagger can be used with any .csv file that meets the following criteria:

1] The first 6 fields (0-5) contain timestamp data in the format:

DD, MM, YYYY, HH, MN, SS, (Day, Month, Year, Hour, Minute, Second). 

2] It is currently hard-coded for the WaveRider Buoy data - meaning that its GUI nomenclature for other variables after the timestamp will not change, i.e. it is hard-coded to

DD, MM, YYYY, HH, MN, SS, Hs, Hrms, Hmax, Tz, Ts, Tc, THMax, EPS, T02, Tp, Hrms.1, EPS.1 - e.g.

7,1,1998,14,20,8,2.1,1.45,3.87,7.26,9.8,4.05,9.84,0.83,7.33,11.31,1.55,0.87

Other field values after the 6 timestamp fields (up to 12) can be read and graphed, but will not be assigned field names other than pre-existing ones.

Field-name Header interpretation may be implemented in a later version of the software - but there is nothing stopping inquisitive users to implement this themselves.


