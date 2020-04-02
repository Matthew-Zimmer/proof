target_include_directories(proof INTERFACE 
	$<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}> 
	$<INSTALL_INTERFACE:include/proof>)

target_include_directories(proof_test PUBLIC 
	$<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}>)

set(headers 
	grammer.hpp)

install(FILES ${headers} DESTINATION include/proof)
