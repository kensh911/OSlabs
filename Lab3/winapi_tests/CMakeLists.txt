cmake_minimum_required(VERSION 3.10)

# �������� ���� � Catch2
get_filename_component(CATCH_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../include" ABSOLUTE)

# ������� ����������� ���� ��� ������
add_executable(winapi_tests winapi_tests.cpp)

# �������� ���������� � ������������� �������
target_include_directories(winapi_tests PRIVATE ${CATCH_INCLUDE_DIR})

# ������������� ���������� ��� ������
set_target_properties(winapi_tests PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)

# ��������� ����
add_test(NAME WinAPITests COMMAND winapi_tests)