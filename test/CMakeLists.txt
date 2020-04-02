target_sources(proof_test PUBLIC 
    main.cpp)

find_package(ordeal REQUIRED)
target_link_libraries(proof_test PUBLIC ordeal proof)