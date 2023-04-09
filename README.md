## Urho3D Simple Multiplayer Shooter
It's simple deathmatch shooter game on Urho3D game engine, it supports multiplayer and custom AIs.

**Engine:** Urho3D.

**Programming languages:** C++ (server, constants and launcher) and AngelScript (client and AIs), AngelScript **!=** ActionScript.

## Features:
* Client-server multiplayer support.
* Custom scriptable AI support.
* Server leaderboard.

## How to build (legacy)

Step 1. Download [U3D](https://github.com/u3d-community/U3D) source and build it.
Recommended version -- current master (tested with U3D commit id: 8e9c11f7febfd36b382f4c391b3d3747e800a63e).
Previously tested with Urho3D commit id: 255f04681a80478b65dbf65ab9e5f4e7fc139a50

Step 2. Set `URHO3D_HOME` environment var equal to the U3D engine build directory:

```bash
export URHO3D_HOME=/home/$USER/Projects/U3D/build
```

Step 3. Clone repository:
```bash
git clone https://github.com/KonstantinTomashevich/urho3d-simple-multiplayer-shooter.git
```
Step 4. Copy the CoreData, Module and Toolchain folders from Urho3D to urho3d-simple-multiplayer-shooter
```bash
mkdir -p urho3d-simple-multiplayer-shooter/bin/CoreData
cp -r U3D/bin/CoreData/* urho3d-simple-multiplayer-shooter/bin/CoreData
mkdir -p urho3d-simple-multiplayer-shooter/cmake
cp -r U3D/cmake/* urho3d-simple-multiplayer-shooter/cmake
```

Step 5. Generate build directory via CMake:
```bash
cd urho3d-simple-multiplayer-shooter && mkdir build && cd build && cmake ..
```
Step 6. Build.
```bash
make
```
Step 7. Executables will be in urho3d-simple-multiplayer-shooter/build/bin folder.

## How to build (DBE)

Build the U3D engine using DBE using the flavor you prefer (web below):

```bash
git clone https://github.com/urho3d/Urho3D.git
cd Urho3D
# Install Urho3D library to a default install location
script/dockerized.sh web rake build install
```

Now that we have a docker image with U3D build, we can use that env to build our project:

```bash
git clone https://github.com/frobino/urho3d-simple-multiplayer-shooter.git
cd urho3d-simple-multiplayer-shooter.git
# The command below requires cmake, script, rakefile to be in place. See CMakefile
script/dockerized.sh web
```

## Screenshots:
![1](https://s30.postimg.org/hxgjgbs8h/image.png)
![2](https://s7.postimg.org/tyiiums4r/image.png)
![3](https://s30.postimg.org/bl1e6hp69/image.png)
![4](https://s30.postimg.org/uen73hne9/image.png)
![5](https://s30.postimg.org/tqeckjooh/image.png)
