# Generate header-file template for build number
configure_file( build_number.h.in ${CMAKE_BINARY_DIR}/generated/build_number.h )
include_directories( ${CMAKE_BINARY_DIR}/generated/ )

add_library(hello hello.cpp)

target_include_directories(hello PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_features(hello PUBLIC cxx_std_17)
