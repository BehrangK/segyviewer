# segyviewer [![Build Status](https://travis-ci.org/equinor/segyviewer.svg?branch=master)](https://travis-ci.org/equinor/segyviewer)

conda create --name test_segyviewer --clone base_clone_0
activate test_segyviewer
conda update --all
pip install segyio PyQt5 pyqtwebengine matplotlib


git clone https://github.com/BehrangK/segyviewer
cd segyviewer
python setup.py build
python setup.py install
cd applications
python segyviewer "D:/test.sgy"
python segyviewer -i 1 -x 1 ..\tests\testdata\small.sgy



Segyviewer is a small LGPL licensed python library for easy viewing of
SEG-Y files. It uses the
**[segyio library](https://github.com/equinor/segyio)**
for reading files.

This project also provides the
[`segyviewlib`](https://pypi.org/project/segyviewlib/)
which is a collection of views that can be used in other Python
projects.


![segyviewer](https://raw.githubusercontent.com/equinor/segyviewer/master/assets/segyviewer.png)


## Getting started

Segyviewer is available on [PyPI](https://pypi.org/project/segyviewer/)
through pip and installed with

```bash
pip install segyviewer
```

to open segyviewer with your chosen <file.segy>
```bash
segyviewer <file.segy>
```

### Configuring the view

You can select from a multitude of **colormaps** (see the
[documentation from Matplotlib](https://matplotlib.org/users/colormaps.html)
for an overview).  The default color is the industry standard
"`seismic`" color.

![segyviewer colormaps](https://raw.githubusercontent.com/equinor/segyviewer/master/assets/segyviewer-all-the-colormaps.png)


The optimal **layout** (the position of the tiles) of the
crossline/inline/depth windows depends on the SEG-Y file.  It is
therefore possible to configure the layout.

![segyviewer general settings](https://raw.githubusercontent.com/equinor/segyviewer/master/assets/segyviewer-tile.png)


Finally, it is possible to configure various settings such as the
current cube, colormap interpolation, export, etc.

![segyviewer general settings](https://raw.githubusercontent.com/equinor/segyviewer/master/assets/segyviewer-general-settings.png)



## Build Segyviewer

To build segyviewer you need:

 * [Python](https://www.python.org/) 2.7 or 3.x.
 * [numpy](http://www.numpy.org/) version 1.10 or greater
 * [setuptools](https://pypi.python.org/pypi/setuptools) version 28 or greater
 * [setuptools-scm](https://pypi.python.org/pypi/setuptools_scm)
 * [PyQt5](https://pypi.org/project/PyQt5/)
 * [segyio](https://github.com/equinor/segyio)
 * [matplotlib](https://matplotlib.org/)

To build and install segyviewer, perform the following actions in your console:

```bash
git clone https://github.com/BehrangK/segyviewer
cd segyviewer
python setup.py build
python setup.py install
```

Modified to work with PyQt5
