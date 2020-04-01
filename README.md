# OpenStreetMap Route Planner
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

A* is the name of an algorithm that was created as part of the [Shakey project](https://en.wikipedia.org/wiki/Shakey_the_robot). Mainly this algorithm is a graph path search that is often used in computer science due to its completeness, optimality, and optimal efficiency.
In this project, I have implemented a routing application for finding path between two points on the OpenStreetMap. For building and using this project follow by below steps:

### Building and Running
When cloning this project, be sure to use the `--recurse-submodules` flag. Using HTTPS:
```bash
git clone https://github.com/PooyaAlamirpour/OpenStreetMapRoute.git --recurse-submodules
```
Before you start to build this project you should consider preparing some dependencies. 
* cmake >= 3.11.3
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 7.4.0
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same instructions as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* IO2D
  * Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
	```bash
	Refresh apt: sudo apt update
	Install GCC: sudo apt install build-essential
	Install CMake: sudo apt install cmake
	Install Cairo: sudo apt install libcairo2-dev
	Install graphicsmagick: sudo apt install libgraphicsmagick1-dev
	Install libpng: sudo apt install libpng-dev
	
	git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
	cd P0267_RefImpl
	mkdir Debug
	cd Debug
	cmake --config Debug "-DCMAKE_BUILD_TYPE=Debug" ..
	cmake --build .
	sudo make install
	```
  * This library must be built in a place where CMake `find_package` will be able to find it

To compile the project, first, create a `build` directory and change to that directory:
```bash
mkdir build && cd build
cmake ..
make
```

### Running
The executable will be placed in the `build` directory. From within `build`, you can run the project as follows:
```
./OSM_A_star_search
```
Once the project run successfully you should see the result as below image:

![Output](https://github.com/PooyaAlamirpour/OpenStreetMapRoute/blob/master/images/Output.png)

## References
- [A* Algorithm](https://en.wikipedia.org/wiki/A*_search_algorithm)
- [OpenStreetMap](https://www.openstreetmap.org/)
