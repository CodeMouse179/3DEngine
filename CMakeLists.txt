cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 17)

project(3DEngine)

add_executable(3d
    src/3DEngine/olcPixelGameEngine.h
    src/3DEngine/main.cpp
)

find_library(X11_LIBRARY X11)
target_link_libraries(3d ${X11_LIBRARY})

find_library(GL_LIBRARY GL)
target_link_libraries(3d ${GL_LIBRARY})

find_library(PTHREAD_LIBRARY pthread)
target_link_libraries(3d ${PTHREAD_LIBRARY})

find_library(PNG_LIBRARY png)
target_link_libraries(3d ${PNG_LIBRARY})
