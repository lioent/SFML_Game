cmake_minimum_required(VERSION 3.11)
project( SFML_Game CXX )

set(CMAKE_CXX_STANDARD 20)

set(SFML_DIR SFML-2.5.1\\lib\\cmake\\SFML)

# executable
add_executable(SFML_Game _main.cpp)

# link SFML
find_package(SFML 2.5 COMPONENTS graphics window system REQUIRED)
target_link_libraries(SFML_Game PRIVATE sfml-graphics sfml-window sfml-system)
