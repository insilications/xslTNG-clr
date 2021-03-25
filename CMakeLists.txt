message(STATUS "cmake version ${CMAKE_VERSION}")
project (gradle)
cmake_minimum_required (VERSION 3.20.0)

set(OPT_INSTALL_DIR /opt/xslTNG/ CACHE STRING "Install location of /opt files" FORCE)
set(LIB_INSTALL_DIR /usr/lib/ CACHE STRING "Install location of libraries" FORCE)
set(BIN_INSTALL_DIR bin CACHE STRING "Install location of executables" FORCE)
set(CMAKE_INSTALL_LIBDIR /usr/lib/ FORCE)
set(LIBDIR /usr/lib/ FORCE)
set(LIB_INSTALL_DIR /usr/lib/ FORCE)

#install(CODE "execute_process(COMMAND ../gradle zipStage)")

install(DIRECTORY ${PROJECT_SOURCE_DIR}/build/stage/zip/ DESTINATION ${OPT_INSTALL_DIR} USE_SOURCE_PERMISSIONS)
