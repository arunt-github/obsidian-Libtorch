
`cmake_minimum_required(VERSION 3.2)`
`project(torch_test)         #project name`
`set(CMAKE_PREFIX_PATH "/libtorch")`
`find_package(Torch REQUIRED)`
`set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}")`
`add_executable(${PROJECT_NAME} main.cpp)`
`target_link_libraries(${PROJECT_NAME} "${TORCH_LIBRARIES}")`
`set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 14)`

project --> name of project 
set --> setting path of lib
find_package --> Locate LibTorch Libraries and Headers using `"${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}"`
add_executable --> creating .exe file for mentioned cpp
target_link_libraries --> targeting lib by the location stored
set_property --> setting properties for code (here setting cpp as cpp 14 for our project name)

