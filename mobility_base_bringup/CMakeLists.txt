cmake_minimum_required(VERSION 2.8.3)
project(mobility_base_bringup)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch)

#install(PROGRAMS scripts/install 
#        DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#)

install(DIRECTORY launch udev yaml
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
