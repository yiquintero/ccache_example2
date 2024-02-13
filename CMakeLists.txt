cmake_minimum_required(VERSION 3.16)

project(hello)

#find_program(ccache_exe ccache)
#if(ccache_exe)
#   file(COPY_FILE
#     ${ccache_exe} ${CMAKE_BINARY_DIR}/cl.exe
#     ONLY_IF_DIFFERENT)

  # By default Visual Studio generators will use /Zi which is not compatible
  # with ccache, so tell Visual Studio to use /Z7 instead.
  #message(STATUS "Setting MSVC debug information format to 'Embedded'")
  #set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<$<CONFIG:Debug,RelWithDebInfo>:Embedded>")

#   set(CMAKE_VS_GLOBALS
#     "CLToolExe=cl.exe"
#     "CLToolPath=${CMAKE_BINARY_DIR}"
#     "TrackFileAccess=false"
#     "UseMultiToolTask=true"
#     "DebugInformationFormat=OldStyle"
#   )
#endif()

add_executable(hello main.cpp)

install(TARGETS hello)
