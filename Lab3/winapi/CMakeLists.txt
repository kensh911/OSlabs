cmake_minimum_required(VERSION 3.10)

# ������� ����������� ����
add_executable(marker_winapi marker_winapi.cpp)

# ������������� ���������� ��� ������
set_target_properties(marker_winapi PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)