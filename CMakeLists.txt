cmake_minimum_required(VERSION 3.0.0)
project(glbase-4.1core VERSION 0.1.0)

enable_language(CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(glbase src/main.cpp)

find_package(glm REQUIRED)
target_link_libraries(glbase glm::glm)
find_package(GLEW REQUIRED)
target_link_libraries(glbase GLEW::GLEW)
find_package(GLFW3 REQUIRED)
target_link_libraries(glbase glfw)
