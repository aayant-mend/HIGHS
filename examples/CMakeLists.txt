if(NOT BUILD_EXAMPLES)
  return()
endif()

if(BUILD_CXX_EXAMPLE)
  file(GLOB CXX_SRCS "*.cpp")
  foreach(FILE_NAME IN LISTS CXX_SRCS)
    add_cxx_test(${FILE_NAME})
  endforeach()
endif()

# if(BUILD_PYTHON_EXAMPLE)
#   file(GLOB PYTHON_SRCS "*.py")
#   foreach(FILE_NAME IN LISTS PYTHON_SRCS)
#     add_python_example(${FILE_NAME})
#   endforeach()
# endif()

if(BUILD_CXX_EXAMPLE)
  file(GLOB C_SRCS "*.c")
  foreach(FILE_NAME IN LISTS C_SRCS)
    add_c_example(${FILE_NAME})
  endforeach()
endif()