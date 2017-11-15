project('CppUTes',
        'cpp',
        version : '1.1.0',
       default_options : ['cpp_std=c++11'])

#include google-test
cpputest = dependency(
                    'CppUTest',
                    required : false)
if cpputest.found()
else
#search for gtest in the subjrojects folder
    sp_cpputest = subproject('cpputest')
    cpputest_dep = sp_cpputest.get_variable('cpputest_dep')
endif

# includes
include = include_directories('include')
priv_includes = [include]
priv_sources = ['source/main.c']

# build the executable
exe = executable('boilerplate', [priv_sources],
        include_directories : priv_includes)

