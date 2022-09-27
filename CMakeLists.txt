cmake_minimum_required(VERSION 3.10.2)

project(NSP)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(external/ScaLAPACK)

target_include_directories(${PROJECT_NAME}
  PUBLIC external/ScaLAPACK
)

target_link_directories(${PROJECT_NAME}
  PRIVATE external/ScaLAPACK/lib
)

target_link_libraries(${PROJECT_NAME} scalapack)
