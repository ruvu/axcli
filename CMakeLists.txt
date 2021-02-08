cmake_minimum_required(VERSION 2.8.3)
project(axcli)

find_package(catkin REQUIRED)

catkin_package()

catkin_add_env_hooks(20.axcli SHELLS bash DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

catkin_install_python(PROGRAMS
  bin/axcli
  DESTINATION ${CATKIN_GLOBAL_BIN_DESTINATION}
)
