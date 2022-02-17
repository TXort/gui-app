cmake_minimum_required(VERSION 3.7)
project(gui_app)

set(CMAKE_CXX_STANDARD 23)

set(wxWidgets_ROOT_DIR </usr/local/include/wx-3.1>)
set(wxWidgets_CONFIGURATION mswu)
find_package(wxWidgets COMPONENTS core base REQUIRED)
include(${wxWidgets_USE_FILE})

set(SOURCE_FILES main.cpp)
add_executable(FirstC ${SOURCE_FILES})

target_link_libraries(FirstC ${wxWidgets_LIBRARIES})