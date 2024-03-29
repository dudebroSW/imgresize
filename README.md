﻿## Image Resizer - imgresize.py

This is a python script that takes images from a directory, resizes them, and then places them in a new output 
directory. This works best running through the command line. Directions are below.

## Usage

Begin by using `git clone https://github.com/ThisJustin-code/imgresize.git` to download the repo.

If using conda you can now create a new virtual environment and use `pip install requirements.txt` to download necessary
libraries.

Here is the `--help` page from imgresize.py:

```
usage: imgresize.py [-h] -x int -y int [-p str] datapath output

Resize images according to user input

positional arguments:
  datapath              the directory path containing the images to be resized
  output                the output directory that will contain the resized
                        images

optional arguments:
  -h, --help            show this help message and exit
  -x int, --resize_x int
                        px value for image height resize (Required)
  -y int, --resize_y int
                        px value for image height resize (Required)
  -p str, --prefix str  rename images with custom prefix (Optional)
```

An example is shown below that resizes the images in `.\imgs` to 512x512 resolution and then outputs those 
images with the prefix `my-image` to `.\resized`:

`python .\imgresize.py -x 512 -y 512 -p my-image ".\imgs" ".\resized"`

Output in the `.\resized` directory would look like the following:

```
my-image000000.jpg
my-image000001.jpg
my-image000002.jpg
my-image000003.jpg
...
```
