cmake_minimum_required(VERSION 2.8.3)
project(genty)

# Minimal Python module setup - catkin is assumed preinstalled along with ROS
# This assume catkin is installed along with a minimal ROS system.
find_package(catkin REQUIRED COMPONENTS
    catkin_pip
)

# defining current package as a package that should be managed by pip (not catkin - even though we make it usable with workspaces)
catkin_pip_package(genty)

## Unit tests
if (CATKIN_ENABLE_TESTING)

    ############
    # NoseTests
    ############

    catkin_add_pytests(test)
    #TODO : use tox directly

endif()
