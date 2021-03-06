# Toolchain to convert PLY point clouds to Potree (javascript).


## Building

Make sure that PotreeConverter submodule is initialized by running:

    > git submodule update --init --recursive

The PotreeConverter submodule differs from the official PotreeConverter 
package as it includes libLAS/LAZ and have some build-related modifications 
for better portability. Build has been tested on Linux and OSX.

*The compiler must support C++11, so GCC > 6 is needed.*
Running 

    > make

launches the compilation using the default system compiler, or use

    > CC=gcc-8 CXX=g++-8 make 

to specify the compiler which compiler to use.



## Testing

Run the sample script

    > test_toolchain.sh

to convert a PLY (testdata/cloud.ply) to potree (testdata/testPotree.html).
To see the result go to the output directory and run 

    > python -m SimpleHTTPServer &
       or
    > python3 -m http.server &

then open a browser and go to: http://127.0.0.1:8000/testPotree.html

