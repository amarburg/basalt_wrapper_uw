cmake_minimum_required(VERSION 3.10)

project(basalt_wrapper)

# sophus and cereal must be installed or else the generation
# of the basalt-headerTargets.cmake fails

set(SOPHUS_INSTALL ON CACHE BOOL "install sophus")
set(CEREAL_INSTALL ON CACHE BOOL "install cereal")
add_subdirectory(basalt)
