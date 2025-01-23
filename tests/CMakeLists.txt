include(FetchContent)

FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        v1.15.2
)
FetchContent_MakeAvailable(googletest)

add_library(GTest::GTest INTERFACE IMPORTED)
target_link_libraries(GTest::GTest INTERFACE gtest_main)

add_executable(tests 
  "test_main.cpp"
  "pizzas_tests/PizzeriaTest.cpp"
)
target_include_directories(tests PRIVATE mocks)

target_link_libraries(tests
  PRIVATE
  GTest::GTest
  GTest::gmock
  pizzas
)

add_test(tests tests)
