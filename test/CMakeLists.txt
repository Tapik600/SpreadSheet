cmake_minimum_required(VERSION 3.12)

project(spread_sheet_test LANGUAGES CXX)

aux_source_directory(. tests_src)

add_executable (${PROJECT_NAME} ${tests_src})
target_include_directories(${PROJECT_NAME} PRIVATE spreadsheet)
target_link_libraries(${PROJECT_NAME} spreadsheet)

add_test(${PROJECT_NAME} ${PROJECT_NAME})