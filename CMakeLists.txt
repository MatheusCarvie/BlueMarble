cmake_minimum_required(VERSION 3.12)

project(BlueMarble)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenGL REQUIRED)

add_executable(${PROJECT_NAME} 
    main.cpp
    deps/glad/src/glad.c
)

target_include_directories(${PROJECT_NAME} PRIVATE 
    deps/glad/include
    deps/glfw/include
    deps/glm/include
)

target_link_directories(${PROJECT_NAME} PRIVATE 
    deps/glfw/lib
)

target_link_libraries(${PROJECT_NAME} PRIVATE 
    glfw3.lib
    OpenGL::GL
)