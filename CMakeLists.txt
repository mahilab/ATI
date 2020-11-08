cmake_minimum_required(VERSION 3.7)

# create project
project(ATI VERSION 0.1.0 LANGUAGES CXX)

# fetch mahi libs
include(FetchContent) 

FetchContent_Declare(mahi-robo GIT_REPOSITORY https://github.com/mahilab/mahi-robo.git) 
FetchContent_MakeAvailable(mahi-robo)

FetchContent_Declare(mahi-daq GIT_REPOSITORY https://github.com/mahilab/mahi-daq.git) 
FetchContent_MakeAvailable(mahi-daq)

FetchContent_Declare(mahi-gui GIT_REPOSITORY https://github.com/mahilab/mahi-gui.git) 
FetchContent_MakeAvailable(mahi-gui)

add_executable(ati main.cpp)
target_link_libraries(ati mahi::gui mahi::daq mahi::robo)