cppu_src = [
            'src/CppUTest/CommandLineArguments.cpp',
            'src/CppUTest/CommandLineTestRunner.cpp',
            'src/CppUTest/JUnitTestOutput.cpp',
            'src/CppUTest/MemoryLeakDetector.cpp',
            'src/CppUTest/MemoryLeakWarningPlugin.cpp',
            'src/CppUTest/SimpleMutex.cpp',
            'src/CppUTest/SimpleString.cpp',
            'src/CppUTest/TeamCityTestOutput.cpp',
            'src/CppUTest/TestFailure.cpp',
            'src/CppUTest/TestFilter.cpp',
            'src/CppUTest/TestHarness_c.cpp',
            'src/CppUTest/TestMemoryAllocator.cpp',
            'src/CppUTest/TestOutput.cpp',
            'src/CppUTest/TestPlugin.cpp',
            'src/CppUTest/TestRegistry.cpp',
            'src/CppUTest/TestResult.cpp',
            'src/CppUTest/TestTestingFixture.cpp',
            'src/CppUTest/Utest.cpp',
]

cppue_src = [
            'src/CppUTest/CodeMemoryReportFormatter.cpp',
            'src/CppUTest/IEEE754ExceptionsPlugin.cpp',
            'src/CppUTest/MemoryReportAllocator.cpp',
            'src/CppUTest/MemoryReporterPlugin.cpp',
            'src/CppUTest/MemoryReportFormatter.cpp',
            'src/CppUTest/MockActualCall.cpp',
            'src/CppUTest/MockExpectedCall.cpp',
            'src/CppUTest/MockExpectedCallsList.cpp',
            'src/CppUTest/MockFailure.cpp',
            'src/CppUTest/MockNamedValue.cpp',
            'src/CppUTest/MockSupport.cpp',
            'src/CppUTest/MockSupport_c.cpp',
            'src/CppUTest/MockSupportPlugin.cpp',
            'src/CppUTest/OrderedTest.cpp',
]

cppu_inc = include_directories('include/CppUTest')
cppue_inc = include_directories('include/CppUTestxt')

libcpputest = library(  'libcpputest', cppu_src,
                        include_directories : cppu_inc )
libcpputestext = library(  'libcpputestext', cppue_src,
                        include_directories : cppue_inc )

lcpp_dep = declare_dependency(link_with : ['libcpputest','libcpputestext'],
                    include_directories : ['cppu_inc','cppue_inc'])
