set( CMAKE_CXX_STANDARD 17 )
set( CMAKE_CXX_STANDARD_REQUIRED ON )
set( CMAKE_CXX_EXTENSIONS OFF )

link_libraries( son8::overglad )
# Add tests ⮟ HERE ⮟ that should NOT use extra warning flags
add_executable( test-include-overglad include/overglad.cxx )
add_test( NAME test-include-overglad COMMAND test-include-overglad )
add_executable( test-include-overglad-v1_1 include/overglad/v1_1.cxx )
add_test( NAME test-include-overglad-v1_1 COMMAND test-include-overglad-v1_1 )
add_executable( test-include-overglad-v1_5 include/overglad/v1_5.cxx )
add_test( NAME test-include-overglad-v1_5 COMMAND test-include-overglad-v1_5 )
add_executable( test-include-overglad-v2_1 include/overglad/v2_1.cxx )
add_test( NAME test-include-overglad-v2_1 COMMAND test-include-overglad-v2_1 )
add_executable( test-include-overglad-v3_3 include/overglad/v3_3.cxx )
add_test( NAME test-include-overglad-v3_3 COMMAND test-include-overglad-v3_3 )
add_executable( test-include-overglad-v4_3 include/overglad/v4_3.cxx )
add_test( NAME test-include-overglad-v4_3 COMMAND test-include-overglad-v4_3 )
add_executable( test-include-overglad-comp include/overglad/comp.cxx )
add_test( NAME test-include-overglad-comp COMMAND test-include-overglad-comp )
add_executable( test-include-overglad-c3_3 include/overglad/c3_3.cxx )
add_test( NAME test-include-overglad-c3_3 COMMAND test-include-overglad-c3_3 )
add_executable( test-include-overglad-c4_3 include/overglad/c4_3.cxx )
add_test( NAME test-include-overglad-c4_3 COMMAND test-include-overglad-c4_3 )


if ( MSVC )
    add_compile_options( /W4 )
else( )
    add_compile_options( -Wall -Wextra -Wpedantic )
endif( )

# Add tests ⮟ HERE ⮟ that SHOULD use extra warning flags
