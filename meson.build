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
    cpputest_dep = sp_cpputest.get_variable('lcpp_dep')
    cpputest_inc = sp_cpputest.get_variable('cppu_inc')
    cppu_lib = sp_cpputest.get_variable('libcpputest')
    #cppue_lib = sp_cpputest.get_variable('libcpputestext')
endif

# includes
include = include_directories('include')
priv_includes = [include]
priv_src = ['src/main.cpp']
test_src = ['test/test.cpp',
            'test/ClassName.cpp']

# build the executable
exe = executable('boilerplate', [priv_src,test_src],
        include_directories : [priv_includes, cpputest_inc],
        link_with : [cppu_lib])

