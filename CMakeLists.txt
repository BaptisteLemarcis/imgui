cmake_minimum_required(VERSION 3.17)

project(Imgui VERSION 1.0 LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(IMGUI_HEADERS 
    imconfig.h
    imgui.h
    imgui_internal.h
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h
)
set(IMGUI_SRC 
    imgui.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
    imgui_demo.cpp
)

include_directories(.)

source_group(TREE "${CMAKE_CURRENT_SOURCE_DIR}" FILES ${IMGUI_SRC} ${IMGUI_HEADERS})

add_library(imgui STATIC ${IMGUI_SRC} ${IMGUI_HEADERS})