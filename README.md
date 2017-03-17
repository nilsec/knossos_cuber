knossos_cuber
=============

A Python application that converts images into a **KNOSSOS**-readable format.

Prerequisites
-------------

You can choose either one or both of the following two installation methods:

### 1. System-wide installation ###

You can install **knossos_cuber** directly from Github by running

    pip3 install https://github.com/knossos-project/knossos_cuber/archive/master.zip

This should provide the executables `knossos_cuber` and `knossos_cuber_gui` on your `PATH`.

Note: If you need to use a Python version older than 3.5, `pyqt5` has to be separately installed using your operating system's package manager (`apt`, `brew`, etc.).


### 2. Running directly from the code directory ###

**knossos_cuber** depends on the following Python packages:

*   `numpy`
*   `scipy`
*   `pillow`
*   `pyqt5` (only if you want to use the GUI)
*   `future` (only if you need to use Python 2 - in this case, use `pip2`/`python2` instead of `pip3`/`python3` in the following instructions)

These dependencies can be installed using pip:

    pip3 install numpy scipy pillow pyqt5

After downloading the source code from https://github.com/knossos-project/knossos_cuber/, you can then run the scripts `knossos_cuber.py` and `knossos_cuber_gui.py` directly with your Python interpreter.

Usage
-----

These usage examples assume that you have installed **knossos_cuber** with the first method ("system-wide installation").

If you prefer to run the scripts directly out of the code folder, replace the following mentions of
`knossos_cuber` by `python3 knossos_cuber.py` and
`knossos_cuber_gui` by `python3 knossos_cuber_gui.py`, respectively.

### Commandline ###


If you run `knossos_cuber` without any arguments, you get the following output:

    usage: knossos_cuber [-h] [--format FORMAT] [--config CONFIG]
                         source_dir target_dir
    knossos_cuber: error: too few arguments

`knossos_cuber` expects at least 3 arguments:

*   `--format`/`-f`: The format of your image files. Currently, the options `png`, `tif` and `jpg` are supported.
*   `source_dir`: The path to the directory where your images are located in.
*   `target_dir`: Path to the output directory.

For example: `knossos_cuber -f png input_dir output_dir`

If you run it like this, `knossos_cuber` will use sane default parameters for dataset generation. These parameters can be found in `config.ini`, and can be overridden by supplying an own configuration file using the `--config`/`-c` argument:

For example: `knossos_cuber -f png -c my_conf.ini input_dir output_dir`

### GUI ###

For a GUI version of this program, run `knossos_cuber_gui`. It accepts an additional argument, `--config`/`-c`, that should be the path to another configuration file.


Afterword
---------

**knossos_cuber** is part of **KNOSSOS**. Head to **KNOSSOS'** [main site](http://www.knossostool.org) or our [Github Repository](https://github.com/knossos-project/knossos) for more information.
