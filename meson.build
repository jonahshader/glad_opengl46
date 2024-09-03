project('glad', 'c',
  version : '0.1.0',
  default_options : ['warning_level=3'])

glad_inc = include_directories('include')
glad_src = ['src/glad.c']

glad_lib = static_library('glad',
  glad_src,
  include_directories : glad_inc,
  install : true)

glad_dep = declare_dependency(
  include_directories : glad_inc,
  link_with : glad_lib)

if meson.version().version_compare('>=0.54.0')
  meson.override_dependency('glad', glad_dep)
endif