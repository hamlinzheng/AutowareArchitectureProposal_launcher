cmake_minimum_required(VERSION 2.8.3)
project(sensing_launch)

find_package(catkin REQUIRED)

# Force Tier IV's fork version
find_package(velodyne_driver REQUIRED)
find_package(velodyne_pointcloud REQUIRED)

catkin_package()

install(
  DIRECTORY
    launch
    data
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
