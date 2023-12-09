# Libtorch and Opencv

A minimal example of how to use OpenCV and Libtorch in the same project.

The project expects libtorch/ in the top-level direcotry. I have not included this in the repository to keep it light. 

Download here (It's importatnt that you use the `cxx11 ABI` version, which works with OpenCV):

## Getting started:

The project expects `libtorch/` in the top-level directory. I have not included this because its 727MB. 

#### Mac M1 Chips

Pre-built binaries of pytorch for for Mac M2 can be found here [libtorch-mac-m1/releases](https://github.com/mlverse/libtorch-mac-m1/releases) (no official builds at the point of writing this.) 

#### Linux

Just download [this version from pytorch.org](https://download.pytorch.org/libtorch/cpu/libtorch-cxx11-abi-shared-with-deps-1.13.0%2Bcpu.zip), rename the folder to 'libtorch' and put it in the repository at top level.
 
### OpenCV

Install OpenCV for development.

Then, in the example-app, the first time you might have to run these commands. 
 `DCMAKE_PREFIX_PATH` is required to be an absolute path!
 
```bash
mkdir build
cd build
cmake -DCMAKE_PREFIX_PATH=/path/to/libtorch ..
cmake --build . --config Release
```
Note the `..` after the command! This references the parent directory.

For subsequent builds you can just type: 

## Run:
```
make
```

For first time install troubleshooting, see the [pytorch cppdocs](https://pytorch.org/cppdocs/installing.html), which this information is based on.
