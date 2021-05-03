set(SOURCE_CODE objectTracking CACHE NAME "Target object name")

cmake_minimum_required(VERSION 2.8)

project( ${SOURCE_CODE} )

find_package( OpenCV REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( ${SOURCE_CODE} ${SOURCE_CODE}.cpp )

target_link_libraries( ${SOURCE_CODE} ${OpenCV_LIBS} )