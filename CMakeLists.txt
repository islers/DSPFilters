cmake_minimum_required(VERSION 2.8.6)

project(DspFilters)

find_package(catkin REQUIRED)

catkin_package(
  INCLUDE_DIRS include
  LIBRARIES ${PROJECT_NAME})

include_directories(include)
add_library(DspFilters
  source/Bessel.cpp
  source/Butterworth.cpp
  source/ChebyshevI.cpp
  source/Custom.cpp
  source/Documentation.cpp
  source/Filter.cpp
  source/Param.cpp
  source/RBJ.cpp
  source/State.cpp
  source/Biquad.cpp
  source/Cascade.cpp
  source/ChebyshevII.cpp
  source/Design.cpp
  source/Elliptic.cpp
  source/Legendre.cpp
  source/PoleFilter.cpp
  source/RootFinder.cpp)

install(DIRECTORY include/${PROJECT_NAME}
  DESTINATION include
)

install(TARGETS DspFilters
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
)  

