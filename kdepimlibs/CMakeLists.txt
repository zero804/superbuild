cmake_minimum_required(VERSION 2.8.4)
project(KDEPimLibs)

find_package(Qt4 REQUIRED)

include (../SuperBuild.cmake)

sb_add_project(kdepimlibs  GIT_REPOSITORY ${SB_GIT_URL}kdepimlibs )

set(CPACK_PACKAGE_VERSION ${SB_PACKAGE_VERSION_NUMBER})
set(CPACK_PACKAGE_NAME ${PROJECT_NAME} )
set(CPACK_SYSTEM_NAME "src")
set(CPACK_GENERATOR "TGZ")
set(CPACK_SET_DESTDIR FALSE)

include(CPack)
