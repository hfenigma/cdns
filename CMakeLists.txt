cmake_minimum_required (VERSION 3.0)
project (cdns)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

add_executable(cdns main.cpp)
set_property(TARGET cdns PROPERTY CXX_STANDARD 17)
target_link_libraries (cdns pthread)
# installs to /usr/local/bin as intended
install (TARGETS cdns DESTINATION bin)
