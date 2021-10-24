cmake_minimum_required(VERSION 3.14)

project(qspcplay VERSION 0.1 LANGUAGES CXX)

## Add dependencies

include_directories(src)

find_package(QT NAMES Qt6 COMPONENTS Quick REQUIRED)
find_package(Qt6 COMPONENTS Quick REQUIRED)

## Application

set(PROJECT_SOURCES
    src/test.cpp
)

add_executable(qspcplay
    ${PROJECT_SOURCES}
)

target_link_libraries(qspcplay
  PRIVATE Qt::Quick
)
