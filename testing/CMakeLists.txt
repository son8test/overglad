set( CMAKE_CXX_STANDARD 17 )
set( CMAKE_CXX_STANDARD_REQUIRED ON )
set( CMAKE_CXX_EXTENSIONS OFF )

link_libraries( son8::overglad )
# Add tests ⮟ HERE ⮟ that should NOT use extra warning flags
add_executable( test-include-overglad include/overglad.cxx )
add_test( NAME test-include-overglad COMMAND test-include-overglad )

if ( MSVC )
    add_compile_options( /W4 )
else( )
    add_compile_options( -Wall -Wextra -Wpedantic )
endif( )

# Add tests ⮟ HERE ⮟ that SHOULD use extra warning flags
