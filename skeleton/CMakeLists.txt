add_executable(SkeletonPassBin Skeleton.cpp)

llvm_map_components_to_libnames(
    llvm_libs
    core support passes
)

target_link_libraries(SkeletonPassBin ${llvm_libs})

set_target_properties(SkeletonPassBin PROPERTIES COMPILE_FLAGS "-fno-rtti")
