cmake_minimum_required(VERSION 3.5)
project(gdb)

# set(CMAKE_BUILD_TYPE Debug)

set(CMAKE_CXX_STANDARD 14)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

add_executable(gdb src/gdb.cpp)
ament_target_dependencies(gdb rclcpp std_msgs)

install(TARGETS
  gdb
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()
