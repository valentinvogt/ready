## Ready solver
This is a fork of [Ready](https://github.com/GollyGang/ready) to be used as a standalone solver.

### Changes from the original repository
- Added the ability to write snapshots when using the solver: see arguments `snapshot-path` and `num-snapshots` in `src/cmd/main.cpp`.

### Building
In principle:
```sh
mkdir build
cd build
cmake ..
make rdy
```

#### Fix on mac
Some errors relating to Qt can be fixed by installing Qt via Homebrew and specifying the paths its CMake files:
```sh
cmake .. \                 
  -DQt6_DIR="/opt/homebrew/opt/qtbase/lib/cmake/Qt6" \
  -DQt6Quick_DIR="/opt/homebrew/opt/qt/lib/cmake/Qt6Quick"
```
