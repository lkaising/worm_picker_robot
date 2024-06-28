cmake_minimum_required(VERSION 3.10.2)
project(motoman_gp4_support)
find_package(ament_cmake REQUIRED)

ament_package()

if(BUILD_TESTING)
  find_package(launch_testing_ament_cmake REQUIRED)
  add_launch_test(test/roslaunch_test_gp4.xml)
endif()

install(DIRECTORY config launch meshes urdf DESTINATION share/${PROJECT_NAME})
