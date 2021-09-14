cmake_minimum_required(VERSION 2.8.3)
project(teleop_twist_keyboard_cpp)

set(CMAKE_CXX_STANDARD 17)

# Find ignition dependencies
set(IGN_COMMON_VER 4)
set(IGN_MSGS_VER 8)
set(IGN_TRANSPORT_VER 11)

find_package(ignition-msgs${IGN_MSGS_VER})
find_package(ignition-transport${IGN_TRANSPORT_VER})


add_executable(teleop_twist_keyboard src/teleop_twist_keyboard.cpp)
target_link_libraries(teleop_twist_keyboard
        ignition-transport${IGN_TRANSPORT_VER}::ignition-transport${IGN_TRANSPORT_VER}
        ignition-msgs${IGN_MSGS_VER}::ignition-msgs${IGN_MSGS_VER})


