file(READ version.txt OLED_VERSION)
message("OLED_VERSION : ${OLED_VERSION}")

# sources
file(GLOB_RECURSE OLED_SOURCES oled/*.*)
add_library(oled ${OLED_SOURCES})

# include dirs
target_include_directories(oled PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# defines
target_compile_definitions(oled PUBLIC -DOLED_VERSION="${OLED_VERSION}")
