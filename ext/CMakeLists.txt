set(GLFW_BUILD_TESTS
        OFF
        CACHE BOOL "" FORCE)
set(GLFW_BUILD_DOCS
        OFF
        CACHE BOOL "" FORCE)
set(GLFW_INSTALL
        OFF
        CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES
        OFF
        CACHE BOOL "" FORCE)
add_subdirectory(glfw)

set(CATCH_BUILD_TESTING OFF CACHE BOOL "" FORCE)
set(CATCH_ENABLE_WERROR OFF CACHE BOOL "" FORCE)
set(CATCH_INSTALL_DOCS OFF CACHE BOOL "" FORCE)
set(CATCH_INSTALL_HELPERS OFF CACHE BOOL "" FORCE)
set_property(GLOBAL PROPERTY CTEST_TARGETS_ADDED 1) #remove Catch2 target spam
add_subdirectory(Catch2)