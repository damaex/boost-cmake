# HowTo Boost in CMake

[![Build Status](https://travis-ci.org/damaex/boost-cmake.svg?branch=master)](https://travis-ci.org/damaex/boost-cmake)

## install Boost dev libraries
### Ubuntu
    sudo apt-get install libboost-all-dev
### Mac
#### using [Homebrew](http://brew.sh/index_de.html "Howto install Homebrew")
    brew install boost
#### using [MacPorts](https://www.macports.org/install.php "Howto install MacPorts")
    sudo port install boost
    
## use project

Just run CMake and make how you usually would do.

    mkdir build
    cd build
    cmake .. && make
