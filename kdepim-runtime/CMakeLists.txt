cmake_minimum_required(VERSION 2.8.4)
project(KDEPimRuntime)

find_package(Qt4 REQUIRED)

include (../SuperBuild.cmake)

sb_add_project(kdepim-runtime  GIT_REPOSITORY ${SB_GIT_URL}kdepim-runtime)

set(CPACK_PACKAGE_VERSION ${SB_PACKAGE_VERSION_NUMBER})
set(CPACK_PACKAGE_NAME ${PROJECT_NAME} )
set(CPACK_SYSTEM_NAME "src")
set(CPACK_GENERATOR "TGZ")
set(CPACK_SET_DESTDIR FALSE)

include(CPack)
