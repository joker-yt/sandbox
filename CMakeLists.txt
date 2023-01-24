project("sandbox")

cmake_minimum_required(VERSION 3.2.2)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_INSTALL_PREFIX ${CMAKE_CURRENT_BINARY_DIR})

message("current source dir: ${CMAKE_CURRENT_SOURCE_DIR}")
message("current binary dir: ${CMAKE_CURRENT_BINARY_DIR}")

set(TARGET sandbox-application)
add_executable(${TARGET})
target_sources(${TARGET} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp)
install(TARGETS ${TARGET}
        RUNTIME DESTINATION install)