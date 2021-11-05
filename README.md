## Urho3D Simple Multiplayer Shooter
It's simple deathmatch shooter game on Urho3D game engine, it supports multiplayer and custom AIs.

**Engine:** Urho3D.

**Programming languages:** C++ (server, constants and launcher) and AngelScript (client and AIs), AngelScript **!=** ActionScript.

## Features:
* Client-server multiplayer support.
* Custom scriptable AI support.
* Server leaderboard.

## How to build
Step 1. Download [Urho3D](https://github.com/urho3d/urho3d) source and build it.
Recommended version -- current master.
Also you can build Urho3D from source, for more information visit [Urho3D Site](https://urho3d.github.io).
Tested with Urho3D commit id: 255f04681a80478b65dbf65ab9e5f4e7fc139a50

Step 2. Set `URHO3D_HOME` environment var equal to the Urho3D engine build directory (the one containing the bin/ folder).

Step 3. Clone repository:
```bash
git clone https://github.com/KonstantinTomashevich/urho3d-simple-multiplayer-shooter.git
```
Step 4. Copy the CoreData, Module and Toolchain folders from Urho3D to urho3d-simple-multiplayer-shooter
```bash
mkdir -p urho3d-simple-multiplayer-shooter/bin/CoreData
cp -r Urho3D/bin/CoreData/* urho3d-simple-multiplayer-shooter/bin/CoreData
mkdir -p urho3d-simple-multiplayer-shooter/urho3d-cmake
cp -r Urho3D/cmake/* urho3d-simple-multiplayer-shooter/urho3d-cmake
```

Step 5. Generate build directory via CMake:
```bash
cd urho3d-simple-multiplayer-shooter && mkdir build && cd build && cmake ..
```
Step 6. Build.
```bash
make
```
Step 7. Executables will be in ${BINARY_DIR}/bin folder.

## Screenshots:
![1](https://s30.postimg.org/hxgjgbs8h/image.png)
![2](https://s7.postimg.org/tyiiums4r/image.png)
![3](https://s30.postimg.org/bl1e6hp69/image.png)
![4](https://s30.postimg.org/uen73hne9/image.png)
![5](https://s30.postimg.org/tqeckjooh/image.png)
