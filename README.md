# Chaos-Equations
Simple mathematical art – macOS port of https://github.com/HackerPoet/Chaos-Equations

**Video:** https://youtu.be/fDSIRXmnVvk

## Build Instructions

Tested on macOS 15.1 with AppleClang 16.0.0

Install required dependencies:

```bash
brew install cmake sfml
```

In the projects directory:

```bash
mkdir build
cd build
cmake ..
make
./chaosequations
```

The program sometimes causes significant lag.