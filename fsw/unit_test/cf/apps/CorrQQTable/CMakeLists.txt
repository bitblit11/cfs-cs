set(TABLE_SET CorrQQTable)

# Build tables for the tests
SET(CMAKE_CXX_ARCHIVE_CREATE "<CMAKE_AR> <OBJECTS> ${CMAKE_CURRENT_BINARY_DIR}")
SET(CMAKE_C_ARCHIVE_CREATE "<CMAKE_AR> <OBJECTS> ${CMAKE_CURRENT_BINARY_DIR}")
add_app(ut_cs_${TABLE_SET}_tablestabl STATIC cs_tablestbl.c)

set_target_properties(ut_cs_${TABLE_SET}_tablestabl PROPERTIES PREFIX "" SUFFIX ".tbl")
