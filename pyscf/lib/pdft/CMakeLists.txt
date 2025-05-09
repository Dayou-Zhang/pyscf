# Build the PDFT library

add_library (clib_pdft SHARED nr_numint.c)
target_link_libraries (clib_pdft dft ${BLAS_LIBRARIES} ${OPENMP_C_PROPERTIES})
set_target_properties (clib_pdft PROPERTIES
    CLEAN_DIRECT_OUTPUT 1
    LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}
    OUTPUT_NAME "pdft")
