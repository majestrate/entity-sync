
if(WITH_PYBIND)
  add_custom_target(check
    ${CMAKE_COMMAND} -E env PYTHONPATH="$ENV{PYTHONPATH}:${CMAKE_BINARY_DIR}/pybind"
    ${PYTHON_EXECUTABLE} -m pytest ${CMAKE_CURRENT_SOURCE_DIR} -v DEPENDS pyomnom)
endif()
