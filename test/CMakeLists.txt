function(make_test name)
  add_executable(${name} ${name}.cc)
  target_link_libraries(${name} PRIVATE ${PROJECT_NAME})
  target_compile_options(${name} PRIVATE -Wall -Wextra -Wpedantic)
  add_test(NAME ${name} COMMAND ${name})
endfunction()

make_test(test1)
