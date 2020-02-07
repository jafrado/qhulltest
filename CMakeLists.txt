cmake_minimum_required(VERSION 3.15)

project (qhull_gpf_test)

if (MSVC)
  add_definitions(-D_CRT_SECURE_NO_WARNINGS)
  set_source_files_properties(qhull.cpp PROPERTIES COMPILE_FLAGS /bigobj)
endif()

add_definitions( -DHAVE_QHULL  -DHAVE_QHULL_2011 -DPCL_NO_PRECOMPILE)

find_package(PCL 1.7.1 CONFIG REQUIRED)
find_package(VTK CONFIG REQUIRED)
find_package(Qhull CONFIG REQUIRED)

set(project_SOURCES qhull.cpp)

add_executable(${PROJECT_NAME} ${project_SOURCES})
target_link_libraries(${PROJECT_NAME} ${PCL_LIBRARIES} ${QHULL_LIBRARIES})

