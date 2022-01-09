cmake_minimum_required(VERSION 3.22)

# set the project name
project(FIVE_POINT_EIGEN VERSION 1.0)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add Eigen
include_directories(include /usr/local/include/)

# list(APPEND EXTRA_LIBS Polynomial)
# list(APPEND EXTRA_LIBS Mblock)
# list(APPEND EXTRA_LIBS Rpoly)

# list(APPEND EXTRA_INCLUDES "${PROJECT_SOURCE_DIR}/Polynomial")
# list(APPEND EXTRA_INCLUDES "${PROJECT_SOURCE_DIR}/Mblock")
# list(APPEND EXTRA_INCLUDES "${PROJECT_SOURCE_DIR}/Rpoly")
# list(APPEND EXTRA_INCLUDES "${PROJECT_SOURCE_DIR}/5point")

#Add Rpoly and 5point library
add_library(Rpoly Rpoly.cpp)
add_library(5point 5point.cpp)
# add_library(Mblock)
# add_library(Polynomial)


# add the executable
add_executable(Main main.cpp 5point.cpp Rpoly.cpp)

# target_link_libraries(FIVE_POINT_EIGEN PUBLIC ${EXTRA_LIBS})
