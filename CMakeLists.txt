cmake_minimum_required(VERSION 3.16)
project(BedrockFinderCpp)

find_package(wxWidgets REQUIRED COMPONENTS core)
include(${wxWidgets_USE_FILE})

find_package(OpenCL REQUIRED)

add_executable(${PROJECT_NAME}
	BFFApp.cpp
	BFFGui.cpp
	PrecomputedRandAdvance.cpp
)

target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
