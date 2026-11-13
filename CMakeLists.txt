cmake_minimum_required(VERSION 3.15)
project(MyApp CXX)

set(CMAKE_CXX_STANDARD 17)

add_executable(MyApp src/main.cpp)

target_include_directories(MyApp PRIVATE "C:/Libraries/glfw/include")
target_link_directories(MyApp PRIVATE "C:/Libraries/glfw/libs")
target_link_libraries(MyApp PRIVATE glfw3 opengl32 gdi32 user32 shell32)
