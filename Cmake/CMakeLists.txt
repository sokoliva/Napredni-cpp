cmake_minimum_required(VERSION 3.11)

project(dz_project CXX)
enable_testing()

# Compilation of googletest library #####
include(FetchContent)
FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG     e2239ee6043f73722e7aa812a459f54a28552929  # release-1.11.0
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)
##########################################

add_subdirectory("src")
add_subdirectory("test")
