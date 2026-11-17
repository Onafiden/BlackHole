cmake_minimum_required(VERSION 3.15)
project(BlackHole)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(GLFW_DIR "C:/Users/Matvey/Documents/libs/glfw")
set(GLEW_DIR "C:/Users/Matvey/Documents/libs/glew")

add_executable(${PROJECT_NAME} src/main.cpp)

target_include_directories(${PROJECT_NAME} PRIVATE 
    "${GLFW_DIR}/include"
    "${GLEW_DIR}/include"
)

target_link_directories(${PROJECT_NAME} PRIVATE 
    "${GLFW_DIR}/libs"
    "${GLEW_DIR}/libs/Release/x64"
)

target_link_libraries(${PROJECT_NAME} PRIVATE 
    "${GLEW_DIR}/libs/Release/x64/libglew32.a"
    glfw3
    opengl32
    gdi32
    user32
    kernel32
)
