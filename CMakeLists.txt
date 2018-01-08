cmake_minimum_required(VERSION 2.8.0)

project(swigmake)

# older approach has no effect:
#install(DIRECTORY swig DESTINATION share)
#install(DIRECTORY cmake DESTINATION share)

find_package(catkin)
catkin_package()

file(MAKE_DIRECTORY ${CMAKE_INSTALL_PREFIX})
file(MAKE_DIRECTORY ${CMAKE_INSTALL_PREFIX}/share)

file( COPY swig DESTINATION ${CMAKE_INSTALL_PREFIX}/share)
file( COPY cmake DESTINATION ${CMAKE_INSTALL_PREFIX}/share)