# Only build CSPARSE if we need to
IF(BUILD_CSPARSE)
  ADD_SUBDIRECTORY(csparse)
ENDIF(BUILD_CSPARSE)

IF (G2O_HAVE_OPENGL)
  ADD_SUBDIRECTORY(freeglut)
ENDIF()

# ----- pybind
set(PYTHON_EXECUTABLE "${Python3_EXECUTABLE}" CACHE FILEPATH "Python executable" FORCE)
add_subdirectory(pybind11)
