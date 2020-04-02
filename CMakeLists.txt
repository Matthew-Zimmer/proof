cmake_minimum_required(VERSION 3.13)

project(proof)

add_library(proof INTERFACE)
add_executable(proof_test)

add_subdirectory(include)
add_subdirectory(src)
add_subdirectory(test)

target_compile_features(proof INTERFACE cxx_std_20)
target_compile_features(proof_test PUBLIC cxx_std_20)

set(CMAKE_CXX_FLAGS "-fmax-errors=1")

install(TARGETS proof EXPORT proof DESTINATION lib/proof)
install(EXPORT proof DESTINATION lib/proof)
install(FILES proof-config.cmake DESTINATION lib/proof)

#libs
#find_package(random REQUIRED)
#target_link_libraries(proof INTERFACE random)