project(CMakeSecondaryDependencies)

add_library(bar SHARED bar.c)

add_library(foo SHARED foo.c)
target_link_libraries(foo PRIVATE bar)

add_executable(app app.c)
target_link_libraries(app foo)
