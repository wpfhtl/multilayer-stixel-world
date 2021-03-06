# multilayer-stixel-world
An implementation of multi-layered stixel computation

![stixel-world](https://github.com/gishi523/multilayer-stixel-world/wiki/images/multilayer-stixel-world.png)

## Description
- An implementation of the Multi-Layered Stixel computation based on [1].
- Extracts the Stixels from the input disparity map.
- Allows for multiple Stixels along every column.

## References
- [1] [The Stixel World - A Compact Medium-level Representation for Efficiently Modeling Three-dimensional Environments](https://www.mydlt.de/david/page/publications.html)

## Demo
- <a href="https://www.youtube.com/watch?v=Ibc8FJ1H024" target="_blank">Demo1</a>
- <a href="https://www.youtube.com/watch?v=ko4bfnN7RpM" target="_blank">Demo2</a>

## Requirement
- OpenCV
- OpenMP (optional)

## How to build
```
$ git clone https://github.com/gishi523/multilayer-stixel-world.git
$ cd multilayer-stixel-world
$ mkdir build
$ cd build
$ cmake ../
$ make
```

## How to run
```
./stixelworld left-image-format right-image-format camera.xml
```
- left-image-format
    - the left image sequence
- right-image-format
    - the right image sequence
- camera.xml
    - the camera intrinsic and extrinsic parameters

### Example
 ```
./stixelworld images/img_c0_%09d.pgm images/img_c1_%09d.pgm ../camera.xml
```

### Data
- I tested this work using the Daimler Ground Truth Stixel Dataset
- http://www.6d-vision.com/ground-truth-stixel-dataset

## Performance(Update 2019/1)
- Setup

Key|Value
---|---
CPU|Core-i7 6700K(4.00 GHz/4Core/8T)
Disparity size|64
Stixel width|7
Scale down factor in image height|2
OpenMP|ON

- Stixel computation time

Image size|Time[milli seconds]
---|---
1024 x 333|11
1024 x 440|18
  
## Author
gishi523
