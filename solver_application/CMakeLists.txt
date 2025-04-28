cmake_minimum_required(VERSION 3.4)

project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(solver equation.cpp)

target_include_directories(solver PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
  /home/mapilsey/lab03/solver_lib
)

target_link_libraries(solver PRIVATE
  /home/mapilsey/lab03/formatter_ex_lib/build/libformatter_ex.a
  /home/mapilsey/lab03/formatter_lib/build/libformatter.a
  /home/mapilsey/lab03/solver_lib/build/libsolver.a
)


