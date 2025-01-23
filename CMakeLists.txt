cmake_minimum_required(VERSION 3.11.0)

cmake_minimum_required(VERSION 3.16)
project(acc_fuel_calculator LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(EXECUTABLE_NAME main)
 
enable_testing()

add_subdirectory(app)
add_subdirectory(src)
add_subdirectory(tests)
