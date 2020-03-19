CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

ADD_SUBDIRECTORY(googletest)

SET(CMAKE_CXX_STANDARD 11)

ADD_EXECUTABLE(c-echo-count
    main.cpp
)

ADD_EXECUTABLE(unit_test
    test.cpp
)

TARGET_LINK_LIBRARIES(unit_test gtest)
TARGET_COMPILE_DEFINITIONS(unit_test PRIVATE gtest_disable_pthreads=ON)
