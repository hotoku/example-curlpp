add_executable(a.out main.cpp)
add_compile_options(-Wall -Wextra -Wpedantic)
set_property(TARGET a.out PROPERTY CXX_STANDARD 11)

target_include_directories(a.out PRIVATE /opt/homebrew/opt/curlpp/include)
target_link_directories(a.out PRIVATE /opt/homebrew/opt/curlpp/lib)
target_link_libraries(a.out curlpp)

target_link_libraries(a.out curl)
