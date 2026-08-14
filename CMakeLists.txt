cmake_minimum_required(VERSION 3.10.0)
project(Philips-Robotic-Hand VERSION 0.1.0 LANGUAGES C CXX)

add_executable(Philips-Robotic-Hand main.cpp)


if(BUILD_TESTS)
  add_subdirectory(external/googletest)
  include(CTest)
  enable_testing()
endif()

add_subdirectory(modules)
