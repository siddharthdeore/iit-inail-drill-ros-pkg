cmake_minimum_required(VERSION 3.0)

set(ROBOT_NAME inail-drill)
project(iit-${ROBOT_NAME}-ros-pkg VERSION 1.0.0)
find_package(catkin REQUIRED COMPONENTS)

catkin_package()

# mark urdf, meshes and launch files for installation
install(DIRECTORY meshes
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
include(GenerateXrdf.cmake)

## add sub-packages
add_subdirectory(inail_drill_urdf)

