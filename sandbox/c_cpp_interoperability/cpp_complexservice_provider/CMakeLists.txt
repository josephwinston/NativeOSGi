cmake_minimum_required(VERSION 2.8)

project(org_nativeosgi_cppcomplexserviceprovider)

set(src_files
  private/src/ComplexService.cpp
  private/src/ComplexServiceBindings.cpp
)

set(public_headers
  public/include/complex_service.h
  public/include/IComplexService.h
)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/public/include)

add_library(${PROJECT_NAME} SHARED ${src_files} ${public_headers})
target_link_libraries(${PROJECT_NAME}
                      nativeosgi_cpp_framework
                      )

