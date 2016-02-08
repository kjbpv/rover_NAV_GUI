cmake_minimum_required(VERSION 2.8)

PROJECT(NAV_GUI_1)

find_package(OpenCV REQUIRED core features2d imgproc flann highgui video ml)

include_directories(${OpenCV_INCLUDE_DIRS})

ADD_EXECUTABLE(NAV_GUI_1 main.cpp rover.h rover.cpp waypoint.h waypoint.cpp patch.h patch.cpp screenshot.h screenshot.cpp display.h display.cpp)
TARGET_LINK_LIBRARIES(NAV_GUI_1 ${OpenCV_LIBS})
