aux_source_directory(. SOURCES)
add_library(cppxml ${SOURCES})
target_link_libraries(cppxml luajit-5.1)
set_target_properties(cppxml PROPERTIES PREFIX "" SUFFIX ".so")
install(TARGETS cppxml DESTINATION openresty/lualib/resty)
