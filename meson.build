
project('glad', 'c', version: '4.3-core')

glad_inc = include_directories('include')

libglad = static_library('glad', 
  'src/glad.c',
  include_directories:glad_inc,
  cpp_args: '-ldl',
  install: get_option('install_lib')
)

glad_dep = declare_dependency(
  include_directories:glad_inc,
  link_with: libglad,
)

if get_option('install_headers')
  install_subdir('include/glad', install_dir: 'include')
  install_subdir('include/KHR', install_dir: 'include')
endif

