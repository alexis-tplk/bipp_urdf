cmake_minimum_required(VERSION 3.8)
project(V1_Robot_Mobil_description)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)

install(
  DIRECTORY urdf launch rviz
  DESTINATION share/${PROJECT_NAME}/
)
install(DIRECTORY meshes
  DESTINATION share/${PROJECT_NAME}
)
ament_package()
