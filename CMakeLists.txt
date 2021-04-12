project(plotTrajectory)
include_directories("/usr/include/eigen3")
add_executable(coordinateTransform coordinateTransform.cpp)

find_package(Pangolin REQUIRED)
find_package( OpenCV REQUIRED )
include_directories(${Pangolin_INCLUDE_DIRS})
add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES} ${OpenCV_LIBS})
