cmake_minimum_required(VERSION 3.10)

# ������� ����� ��� �������
find_package(Threads REQUIRED)

# ������� ����������� ����
add_executable(marker_threads marker_threads.cpp)

# ���������� ���������� �������
target_link_libraries(marker_threads PRIVATE Threads::Threads)

# ������������� ���������� ��� ������
set_target_properties(marker_threads PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)