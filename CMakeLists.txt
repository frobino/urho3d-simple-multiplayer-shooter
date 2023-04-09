cmake_minimum_required (VERSION 3.10.2)
project (SimpleMultiplayerShooter)

if (NOT EXISTS "${CMAKE_SOURCE_DIR}/cmake/")
    message (STATUS "Copying U3D's CMake modules...")
    file (COPY "$ENV{URHO3D_HOME}/../cmake/" DESTINATION "${CMAKE_SOURCE_DIR}/cmake")
endif ()

if (NOT EXISTS "${CMAKE_SOURCE_DIR}/bin/CoreData")
    message (STATUS "Copying U3D's CoreData asset...")
    file (COPY "$ENV{URHO3D_HOME}/../bin/CoreData/" DESTINATION "${CMAKE_SOURCE_DIR}/bin/CoreData")
endif ()

# The following lines are used to copy build scripts to be used with BDE
#
# if (NOT EXISTS "${CMAKE_SOURCE_DIR}/script/")
#     message (STATUS "Copying U3D's build script...")
#     file (COPY "$ENV{URHO3D_HOME}/../script/" DESTINATION "${CMAKE_SOURCE_DIR}/script")
# endif ()
#
# if (NOT EXISTS "${CMAKE_SOURCE_DIR}/rakefile")
#     message (STATUS "Copying U3D's rakefile...")
#     file (COPY "$ENV{URHO3D_HOME}/../rakefile" DESTINATION "${CMAKE_SOURCE_DIR}/rakefile")
# endif ()

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake/Modules)
include (UrhoCommon)

add_subdirectory (app/src)
